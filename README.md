# RealAndoridBot

[![RAB Video Demo](https://img.youtube.com/vi/wtpJ9_av-qc/0.jpg)](https://www.youtube.com/watch?v=wtpJ9_av-qc)

## Changelog
### RAB 1.06
- Added Pokemon Inventory Mangement. RAB will now auto keep or release pokemon in your bag when it is full
- New options for Pokemon Inventory Mangement are `enable_poke_management`, `manage_poke_on_start`, `inventory_iv` and `stop_check_at`. Please check config.example.yaml and update your exising config accordingly.
- `keep_strong_shadow` and `keep_legendary` options added under catch

[Changelog History](https://github.com/MerlionRock/RealAndroidBot/blob/master/Changelog.md)

## Discord
Join our [Discord Channel](https://discord.gg/HZXCzDXXJJ)

## Features
- Auto Catch
- Auto Keep or Transfer base on IV (100 or PvP)
- Auto Select Berries
- Auto Select Balls
- Auto Clear Quests
- Auto Hatch
- Auto Item management
- (NEW) Auto Pokemon Bag management
- Auto Team Rocket Battle (HAL & Polygon# Only)
- Catch Shiny that 3rd Party App Found (Polygon# Only)
- Integration with Telegram feed to allow PvP/100IV Snipe (Not Live Yet)
- Integration with Telegram feed to allow Shiny Checking (Not Live Yet)
- Non rooted support with PGSharp Free or Paid version (**NO NOT USE IT ON MAIN ACCOUNT**)

## Phone Requirements
1. Rooted (Optional)
2. Your phone must be able to run Pokemon Go if it's rooted
3. USB Debugging Enabled ([Under Developer Options](https://developer.android.com/studio/debug/dev-options))
4. Recommended phone with Screen Resolution 1080 x 1920 and above
5. Recommended 4GB RAM and above
6. Recommended Snapdragon 625 and above

## Setting up USB Debugging mode option
1. Launch the Settings application on your phone.
2. Tap the About Phone option generally near the bottom of the list.
3. Then tap the Build Number option 7 times to enable Developer Mode. You will see a toast message when it is done.
4. Now go back to the main Settings screen and you should see a new Developer Options menu you can access.
5. Go in there and enable the USB Debugging mode option. Some Phones will have Install via USB option and USB debugging (Security settings) options or any options that's related simulating input, enable them too.

## Additional Apps needed and their settings

1. (Optional) Install [Pokemod or HAL](https://pokemod.dev/) or [Polygon#](https://discord.gg/QURp9gA) or [PGSharp](https://www.pgsharp.com/) Please set the correct client settings in config file
2. (Pokemod, HAL and Polygon# Only) GPS Joystick, unlock version. Download from their [official website](http://gpsjoystick.theappninjas.com/faq/) 
- (Pokemod, HAL Only) Create/download a GPX Route and run it in background. Make sure joystick are hidden from view.
- (PGSharp Paid Only) Create/download a GPX Route and run it. Do not hide PGSharp. Move joystick away from location that will block text.
- (Polygon#) Just spoof to a location with lot's of pokestops. RAB will handle the rest.
- (Pokemod and HAL Only) Recommended Speed 7km per hour or less
3. (Optional, if your phone's resolution is more than 1920 x 1080) Go to playstore and download Easy DPI Changer (or https://www.apkmirror.com/apk/chornerman_studio/easy-dpi-changer-root/), resize your phone to 1080 x 1920, reset it when you are not running the script. (**Update**: The bot now auto change your phone size. However, it's handy to have this app installed in case the bot is unable to reset back your phone to orginal screen resolution.)
4. Your Pokemon Go Game MUST BE English
5. When running the scripts at your computer, the following app/services must be running on your phone
- GPS Joystick (Not needed for PGSharp)
- (optional) Pokemod, HAL, Polygon# or PGSharp
- Pokemon Go
   
## Pokemod/HAL Support

### Settings
- (Pokemod) IV Display format --> Toast | (HAL) Enable Toasts
- (Pokemod) IV Display Information --> verbose | (HAL) Toast verbosity --> Informative
- Toast Location/Position --> Top

### Enable Modules
- Enable Prefect Throw
- Enable Skip Encounter Intro
- Enable Show Encounter IV (Enable Toasts in Settings)
- Replace Names with IVs in Encounters

### Disable Modules
- Disable Replace Names with IVs in Encounters
- Disable Block Non-Shiny Encounters 
- Disable Mass Transfer any Pokémon (To prevent accident transfer of your fav lengenary Pokemon)

### Optional Modules
- Team Rocket Blastoff (HAL Only)
- Instant Spin
- Instant Catch and Transfer on Catch (HAL Only) (When Transfer on Catch is enabled, the bot will not be able to prevent PvP eligible Pokemon from being transfered)

*Enable or disable the modules in config.yaml accordingly*

## Polygon# Enhancer Support

- Instant catch is not recommended to be disabled for Polygon#, settings related to keeping Pokemon in config will not apply to Polygon#
- Note that RAB will attempt to gather a few information from Polygon# first before starting to catch Pokemon. As such you might see RAB attempt to spin pokestops continously for a few mintues before catching. It is normal.

### Advanced
- Enable `Send data to custom backend`
- Set backend IP Address to the IP of the machine that you are running RAB
- How to find your machine's IP Guide [Windows](https://www.wikihow.com/Check-a-Computer-IP-Address) | [Mac](https://www.hellotech.com/guide/for/how-to-find-ip-address-on-mac)
- Enter a port number that you set in config. Default 5120. If you are using more than one device, each device must have their own config and with their own port number set.
- Encounter nameplates format `{default} LVL{lvl}\nIV{prc0}% {ivs}`
- Pokemon panel nameplate format `{default}`

## PGSharp Support

### Settings for Free Version
- Spoofing Enabled
- Hide PGSharp Enabled
- Enhanced Throw on Excellent and Curved
- Tap to `Teleport` Enabled. By default this option is tap to walk, it will not work for free version. Please change to Tap to Teleport
- Set a location with the Map or enter coordinates 

### Settings for Paid Version
- Spoofing Enabled
- Hide PGSharp Disabled, move joystick to somewhere that wont block the screen
- Enhanced Throw on Excellent and Curved throw is preferred for faster catching
- Tap to `Walk` or `Teleport` Disabled. 
- `Inventory IV` Enabled
- `Encounter IV` Enabled
- `Quick Catch` Optional. Set `transfer on catch` to true in RAB config if you set this option to true.
- The rest of options are optional
- Then click on PGSharp's icon and choose either auto walk or GPX route (this option is in map)

*Enable or disable the modules in config.yaml accordingly*

## PC/MAC/LINUX Requirements

## Install Tesseract

### Mac User
1. Install via Homebrew (https://brew.sh/)
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
2. Install Tesseract
```
brew install tesseract (install homebrew if you have not)
```

### Linux
```sudo apt-get install tesseract-ocr```

### Windows
- Install from [tesseract](https://github.com/UB-Mannheim/tesseract/wiki)
- [Full Installation Instructions](https://tesseract-ocr.github.io/tessdoc/Home.html)
- Note down your installation path. Example `c:\Program Files\Tesseract-OCR\`
- On your Windows search bar type `env`, click on Edit the system environment variables
- Under Advance click Environment Variables, select path, click edit, click new and enter the Tesseract installation path that you note down in pervious step.
- Restart your windows
- After restart, run `tesseract -v` in PowerShell or Command Prompt. The bot will not work if this step is not done correctly.


*To test if you have successfully install Tesseract, run "tesseract -v" at your OS's terminal/command prompt/power shell. The bot will only works if Tesseract is installed correctly*

## Install ADB

### Mac User

1. Using Terminal, install homebrew if you do not have it
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
2. Install adb
```
brew cask install android-platform-tools
```
3. Connect your device to your mac and run the following to see if it can detect your device
```
adb devices
```

### Windows User/Linux

Follow this Guide, follow the instructions for Windows/Linux
1. [Install ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/)

Then set your ADB to PATH system variable, follow this [guide](https://www.xda-developers.com/adb-fastboot-any-directory-windows-linux/)

## Install Git And Build Tools for C++ (Windows User Only)
### For Windows

Follow the 2 links below to install Git and Build Tools

1. [Install Git](https://www.computerhope.com/issues/ch001927.htm)
2. Install [C++ Build Tools](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16) 

## Setting up the project
1. (Windows Only) Start --> Windows Powershell (expand the folder) --> Right click, run as Administrator. Type `cd c:\`
   - 1.1 (Ubuntu/Linux) Open terminal and type: `cd ~/`
2. (Windows Only) Type `python3` in Powershell, this will bring up Window store and will install Python 3 to your system
3. (Windows Only) `Set-ExecutionPolicy RemoteSigned` Enter Y to allow execution of scripts
4. (Mac and Linux) Install Python 3.7 or later (https://www.python.org/downloads/)
5. `git clone --recursive https://github.com/MerlionRock/RealAndroidBot.git`
6. `python3 -m venv RealAndroidBot`
7. (Mac and Linux) `source RealAndroidBot/bin/activate` (Windows) `RealAndroidBot\Scripts\activate`
8. `cd RealAndroidBot`
9. Copy config.example.yaml to rab/config.yaml and configure it.
10. `pip install -r requirements.txt`
11. `cd rab`
12. Setup your phone according to app requirements as instructed above and run all required apps on phone
13. Make sure your Pokemon Go is at map page and **zoomed out to the max**.
14. Make sure your device are connected to your machine, run this command
   `python run.py`
15. Allow installation of automator on your Phone
16. To run multiple devices, first run adb devices to get all your device ID connected to your computer
17. Then run each command on their own terminal/shell console
    `python run.py --device-id YOUR_DEVICE_ID`
18. To use a different config file (good for multiple devices setup) run
    `python run.py --device-id YOUR_DEVICE_ID --config-filename YOUR_CONFIG_FILE_NAME`
19. Ctrl + C to terminate the program (you might have to do it more than once)
20. Whenever you want to run the scripts again, remember to run Step 7 first follow by (mac/linux) `cd RealAndroidBot/rab` or (Windows) `cd RealAndroidBot\rab`
21. To update your files from github repo, type `git pull`

## Disclaimer
©2016 Niantic, Inc. ©2016 Pokémon. ©1995–2016 Nintendo / Creatures Inc. / GAME FREAK inc. © 2016 Pokémon/Nintendo Pokémon and Pokémon character names are trademarks of Nintendo. Other trademarks are the property of their respective owners.
[Privacy Policy](http://www.pokemon.com/us/privacy-policy/)

[RealAndroidBot](https://github.com/MerlionRock/RealAndroidBot) is intended for academic purposes and should not be used to play the game *PokemonGo* as it is unfair to the community. Use the bot **at your own risk**.
