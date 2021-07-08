# dp701 theme for IDA Pro
Dark theme inspired by Visual Studio

# Preview

![](screenshots/theme-preview.png)

# Requirements

- IDA Pro version  **7.3** or newer
- Installed **Segoe UI** and **Consolas** fonts

# Installation

## Install theme

- Copy the contents of `theme/*` into the IDA directory `themes/*`
- Start IDA and select the theme by to the screen resolution in `Options > Colors...`

## Change fonts

The font is already set in the theme file, but there is a bug in the IDA that resets the parameters from the `CSS` for fonts.

Solution: set the font (**Consolas**) for the disassembler window in `Options > Font...`.  or apply [reg](https://wiki.winehq.org/Regedit) file (for Windows):

```ini
Windows Registry Editor Version 5.00

; Delete IDA fonts configuration
[-HKEY_CURRENT_USER\SOFTWARE\Hex-Rays\IDA\Font]
```

## Optional for Windows 10

This methods works only for **Windows 10**.

### Change color of active and inactive title bars

These options will change your desktop window settings.

- Apply the [reg](https://wiki.winehq.org/Regedit) file:

  ```ini
  Windows Registry Editor Version 5.00
  
  ; Automatically Pick a Color from your Background
  [HKEY_CURRENT_USER\Control Panel\Desktop]
  "AutoColorization"=dword:00000000
  ; Active/Inactive Window Title Bar
  [HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\DWM]
  "AccentColor"=dword:ff302d2d
  "AccentColorInactive"=dword:ff494949
  ; Show accent color on the following surfaces
  ; Start, taskbar, and action center
  [HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Themes\Personalize]
  "ColorPrevalence"=dword:00000001
  ; Title bars
  [HKEY_CURRENT_USER\Software\Microsoft\Windows\DWM]
  "ColorPrevalence"=dword:00000001
  ```

# More screenshots

A little more screenshots

## Colors

![](screenshots/colors-preview.png)

## Debug

![](screenshots/debug-preview.png)

## Hex

![](screenshots/hex-preview.png)

## Options

![](screenshots/options-preview.png)

# Why is dp701?

Codename of the project is **d**ark **p**roject, **701** is the number of attempts to create it :smile:

