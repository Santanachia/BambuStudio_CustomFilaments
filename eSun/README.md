# eSun Filament Profiles

This folder contains JSON profile files for eSun filaments organized by printer model.

## Source

Original profiles downloaded from: [eSUN support](https://www.esun3d.com/zldownload_catalog/3d-printing-settings/)

## Important Note

⚠️ **These are NOT ready-to-import `.bbsflmt` files!**

The files in this folder are **partial profile definitions** that inherit from Bambu Lab's base profiles. They contain only the modifications specific to eSun filaments.

## Structure

Profiles are organized by printer model:
- `A1/` - Bambu Lab A1 profiles
- `A1 Mini/` - Bambu Lab A1 mini profiles
- `H2D/` - Bambu Lab H2D profiles
- `H2S/` - Bambu Lab H2S profiles
- `P1P/` - Bambu Lab P1P profiles
- `P1S/` - Bambu Lab P1S profiles
- `P2S/` - Bambu Lab P2S profiles
- `X1/` - Bambu Lab X1 profiles
- `X1C/` - Bambu Lab X1 Carbon profiles

## How to Use These Files

See the [comprehensive import guide](../docs/how-to-import.md#method-2-import-individual-json-profile-files) for detailed instructions on using JSON profile files, including:
- Manual parameter entry (recommended)
- Direct JSON file import (advanced)
- Understanding file types and structure
- Troubleshooting common issues

## Ready-to-Import Profiles

If you need ready-to-import `.bbsflmt` files, check the `Filament bundle/` subfolder. These files have been manually created and tested.

## Available eSun Filament Types

The following eSun filament types are available in this repository:

### PLA Variants
- PLA Basic, PLA+, PLA-HS (High Speed)
- PLA-CF (Carbon Fiber), PLA-LW (Light Weight)
- PLA-Silk, PLA-Matte, PLA-Marble
- PLA-Clear, PLA-Metal, PLA-Magic CL
- PLA-SS (Stainless Steel look), PLA-UV Rock

### PETG Variants
- PETG Basic, PETG, PETG+HS
- PETG-CF (Carbon Fiber), PETG-Matte
- PETG-ESD (Anti-static)

### Engineering Materials
- ABS, ABS+, ABS+HS
- ABS+CF, ABS+GF (Glass Fiber), ABS-ESD
- ASA, ASA+
- PA (Nylon), PA-CF, PA12, PA12+CF
- PC (Polycarbonate), PC-HT

### Flexible Materials
- TPU-95A, TPU-64D, TPU-85A, TPU-90A
- TPU-LW (Light Weight)
- TPE-83A, TPE-LW
- PEBA, PEBA-90A

### Other
- PET, PET-CF, PET Luminous

## Source

These profiles are community-contributed and based on official eSun recommendations and user testing.

## Contributing

If you have successfully created and tested `.bbsflmt` bundles for eSun filaments, please contribute them. See the main repository [Pull Request template](../.github/pull_request_template.md) for guidelines.
