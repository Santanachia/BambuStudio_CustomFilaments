# How to Import Filament Profiles in Bambu Studio

This guide covers different methods of importing filament profiles into Bambu Studio, including ready-to-import `.bbsflmt` bundles and individual JSON files.

---

## Method 1: Import `.bbsflmt` Bundle Files (Recommended)

This method is the easiest and works for KINGROON profiles and some eSun profiles from the `Filament bundle/` folder.

### Step 1: Open Import Dialog

Click on the filament icon in Bambu Studio and select the "Import" option.

![Step 1](Step%201.png)

### Step 2: Select Files

Choose the `.bbsflmt` files you want to import from your file system.

![Step 2](Step%202.png)

### Step 3: Adjust Printer Settings

Configure printer-specific settings as needed for your setup.

![Step 3](Step%203.png)

### Step 4: Configure Project Settings

Set project-specific parameters to match your printing requirements.

![Step 4](Step%204.png)

### Notes

- You can import multiple `.bbsflmt` files at once
- Each profile bundle may contain settings for multiple printer models
- After import, profiles will appear in your filament list
- You can edit imported profiles to fine-tune them for your specific needs

---

## Method 2: Import Individual JSON Profile Files

Most eSun profiles in this repository are provided as individual JSON files organized by printer model. These files contain **partial profile definitions** that inherit from Bambu Lab's base profiles.

⚠️ **Important:** These JSON files contain only the modifications specific to the filament brand and inherit from base Bambu Lab profiles.

### Direct JSON Import

Bambu Studio supports importing JSON files directly, just like `.bbsflmt` bundles:

1. **Open Import Dialog** - Click the filament icon in Bambu Studio and select "Import"

2. **Select JSON Files** - Choose the JSON file(s) you want to import:
   - **Filament.json** - For filament-specific settings
   - **Process.json** - For print process settings (if available)
   
3. **Complete Import** - The profile will be imported and will inherit settings from the base profile specified in the `inherits` field

4. **Verify Settings** - After import, check that the profile works correctly with your printer

**Notes:**
- You can import JSON files individually or in batches
- The imported profile will appear in the appropriate list (filament/process/printer)
- Make sure to import the correct JSON file for your specific printer model

### Alternative: Manual Parameter Entry

If you prefer more control or want to understand the changes:

1. Open Bambu Studio
2. Select a base filament profile similar to the one you want to use (e.g., "Bambu PLA Silk" for eSun PLA-Silk)
3. Open the JSON file for your printer model in a text editor
4. Manually adjust the parameters shown in the JSON file in Bambu Studio's interface
5. Save as a new custom profile with a descriptive name

**Advantages:**
- You understand exactly what parameters are being changed
- More control over the final profile
- Can combine settings from multiple sources

### Understanding JSON File Types

Each filament may have up to three types of JSON files:

- **`[Name] Filament.json`** - Filament-specific settings (temperatures, flow rates, fan speeds, etc.)
- **`[Name] Process.json`** - Print process settings (layer heights, speeds, acceleration, etc.)
- **`[Name] Printer.json`** - Printer-specific adjustments (rare, only when filament requires printer modifications)

### Example: Manual Import Process

Let's say you want to use an eSun PLA+ profile:

1. Find the file: `eSun/P1P/P1P eSUN PLA+ Filament.json`
2. Open it and note the key parameters:
   ```json
   {
     "nozzle_temperature": ["220"],
     "hot_plate_temp": ["60"],
     "filament_flow_ratio": ["0.98"],
     ...
   }
   ```
3. In Bambu Studio, duplicate a base PLA profile
4. Rename it to "eSun PLA+ @P1P"
5. Update the parameters to match the JSON file
6. Save the profile

---

## Troubleshooting

### `.bbsflmt` file won't import
- Ensure you're using a compatible version of Bambu Studio
- Check that the file isn't corrupted (it should be a valid ZIP archive)
- Try importing a single profile first before multiple ones

### JSON files don't appear after copying
- Make sure you placed them in the correct directory
- Verify Bambu Studio was completely closed before copying files
- Check that file names match the expected pattern
- Ensure JSON files are valid (use a JSON validator)

### Profile appears but with wrong settings
- The JSON file may be a partial definition that requires a base profile
- Manually verify and adjust settings after import
- Compare with working profiles of the same material type

---

## Converting Between Formats

If you need to convert JSON files to `.bbsflmt` bundles or vice versa:

1. **JSON to `.bbsflmt`:** Create a complete profile in Bambu Studio, then export it as a bundle
2. **`.bbsflmt` to JSON:** Extract the `.bbsflmt` file (it's a ZIP archive) to access individual JSON files

For automated conversion, see the `generate_bbsflmt.py` script in the repository (note: currently only generates from complete JSON profiles).

