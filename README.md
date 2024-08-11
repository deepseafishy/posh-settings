# Posh Settings

My personal Powershell settings.

## Installation

1. Install Windows Terminal from the Microsoft Store.
2. Install Powershell 7 with `winget install --id Microsoft.Powershell` command in Powershell.
   - Change startup application to Powershell 7 in Settings>Default Profile.
2. Install Oh-My-Posh with `winget install JanDeDobbeleer.OhMyPosh` command in Powershell.
   - Requires admin privilege.
3. Install `PSReadLine` with `Install-Module PSReadLine -Force` command in Powershell.
   - Requires admin privilege.
4. Restart the Windows Terminal.
5. Install custom oh-my-zsh Dieter theme `dieter.omp.json`.
   - Run `cd $env:POSH_THEMES_PATH` and create `dieter.omp.json` in that directory.
6. Install custom Dracula colors from `settings.json`.
   - Open system `settings.json` by going into Settings in Windows Terminal and click `Open JSON file` button on the bottom left corner.
   - Add the contents of this repository's `settings.json` to the color palette settings.
   - Restart the Windows Terminal application after installing the new color palatte.
   - Change the colors in Settings>Windows Powershell>Appearance>Colors.
7. Run `notepad $PROFILE` and add the following lines:
   - `oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/dieter.omp.json" | Invoke-Expression`
   - Run `. $PROFILE` for changes to take effect.
8. (Optional) Disable Powershell banner message.
   - Add `-NoLogo` in Settings>Windows Powershell>CommandLine.
