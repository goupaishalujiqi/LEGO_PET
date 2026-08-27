# LEGO_PET

A LEGO-style Shiba Inu pet for the Codex App.

乐柴是一只适用于 Codex App 的积木玩具风格柴犬。它会摇尾眨眼、四脚小跑、歪头抬爪、原地转圈庆祝，并在阻塞时趴下。

## Files

```text
lechai/
├── pet.json
└── spritesheet.webp
```

The spritesheet uses the Codex v2 pet format: 8 columns × 11 rows, 192 × 208 pixels per cell, with 16 look directions.

## Install

### Codex App

1. Download or clone this repository.
2. Open **Codex → Settings → Pets → Custom pets**.
3. Choose **Open folder**.
4. Copy the `lechai` folder into the opened pets directory.
5. Return to Codex, select **Refresh**, then choose **Lechai**.

### Terminal (macOS or Linux)

```bash
git clone https://github.com/goupaishalujiqi/LEGO_PET.git
mkdir -p "${CODEX_HOME:-$HOME/.codex}/pets/lechai"
cp -R LEGO_PET/lechai/. "${CODEX_HOME:-$HOME/.codex}/pets/lechai/"
```

### Windows PowerShell

```powershell
git clone https://github.com/goupaishalujiqi/LEGO_PET.git
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME ".codex" }
$petDir = Join-Path $codexHome "pets\lechai"
New-Item -ItemType Directory -Force $petDir | Out-Null
Copy-Item ".\LEGO_PET\lechai\*" $petDir -Recurse -Force
```

## Pet format

- `id`: `lechai`
- `spriteVersionNumber`: `2`
- Atlas size: `1536 × 2288`
- Cell size: `192 × 208`

No text or logos are embedded in the pet artwork.
