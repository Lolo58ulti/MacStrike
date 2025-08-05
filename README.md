# Disclaimer
I cannot guaranty that it will work on your system. This is **HIGHLY experimental** and may even cause your computer to crash. 

I am not responsible for any damage or data loss caused to your device as result of following this guide. Use at your own risk.

This project is not related to any mentioned software companies

**Do not report any issues to [NetEase Games](https://www.neteasegames.com)**
 
For wine related issues, please refer to [WineHQ](winehq.org),

And for KegWorks related issues, please refer to [KegWorks](https://github.com/Kegworks-App/Kegworks).

This project is only for Intel Macs (for now) I will try to update it as soon as possible to include M-Series macs
 
Thanks for your Understanding.

## Requirements
[Homebrew](https://brew.sh) (recommanded for further steps)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Or

[MacPort (Official Website)](https://www.macports.org/install.php)

______________________________
[KegWorks Winery](https://github.com/Kegworks-App/Kegworks)

```bash
brew install --cask --no-quarantine Kegworks-App/kegworks/kegworks
```

Or

```bash
sudo port install kegworks
```
________________________________
[Samba (For NTLM_auth)](https://www.samba.org)

Homebrew (recommanded)

```bash
brew install samba && brew link samba && rm /usr/local/bin/samba_dot_org_smbd && rm /usr/local/bin/winbindd
```

Or

MacPort (not recommanded)

```bash
sudo port install samba
```
_________________________________
[BloodStrike From their official website](https://www.blood-strike.com)

Go to "Developpment tab" -> User Agent and select "Microsoft Edge - Windows"

Then Select "Download on Windows"
__________________________________

## Instruction

Open KegWorks Winery

<img width="516" height="600" alt="Capture d’écran 2025-08-04 à 22 51 50" src="https://github.com/user-attachments/assets/0ffa5a9c-413d-4d39-a0d9-791806a50729" />

Tap the + Icon and Select "WS11Wine10.0_1" then press "Download and Install"

Select "WS11Wine10.0_1" and Press "Update Wrapper" then "Create New Blank Wrapper"

<img width="410" height="337" alt="Capture d’écran 2025-08-05 à 11 50 54" src="https://github.com/user-attachments/assets/233accfc-8017-4f9e-808c-0b3fed48d5a4" />

Name It whatever you want and press Ok.

Once it's done go to launchpad and open the wrapper.

<img width="753" height="437" alt="Capture d’écran 2025-08-05 à 11 56 31" src="https://github.com/user-attachments/assets/59ba33fc-9d19-4a65-ae1b-6a9f683c49f3" />

______________________________

### For DXVK (DirectX to Vulkan)

Check "DirectX to Vulkan translation layer - (DXVK)"

Go to the "Advenced tab"

<img width="753" height="437" alt="Capture d’écran 2025-08-05 à 11 58 20" src="https://github.com/user-attachments/assets/bffc1d2b-2289-4381-991f-7ae72d78c5c5" />

Check MoltenVK - (CodeWeavers version) and MolenVK FastMath.

______________________________

### For Native Wine DX interpreter

<img width="797" height="481" alt="Capture d’écran 2025-08-05 à 12 03 00" src="https://github.com/user-attachments/assets/3680c839-4247-4365-8f8f-91a0fd47c111" />

Go to the "Advanced" tab and check MoltenVK - (CodeWeavers Version) And MoltenVK FastMath

______________________________

### For DXMT (DirectX to Metal)

Download DXMT's DLLs from their [official github releases](https://github.com/3Shain/dxmt)

<img width="988" height="504" alt="Capture d’écran 2025-08-05 à 12 06 39" src="https://github.com/user-attachments/assets/76b43303-686c-43b2-8b5e-34736ecf2bbf" />

Extract It and Open "x86_64-windows"

Copy the DLLs into wine at

```bash
/Users/"YourName"/Applications/Kegworks/"Wrappername.app"/Content/SharedSupport/prefix/drive_c/windows/system32
```

And

```bash
/Users/"YourName"/Applications/Kegworks/"Wrappername.app"/Content/SharedSupport/prefix/drive_c/windows/syswow64
```

(To open the wrapper files, Select your app, right-click and "Show Package Content")

<img width="753" height="437" alt="Capture d’écran 2025-08-05 à 12 14 34" src="https://github.com/user-attachments/assets/94ef9b7a-59ee-4c44-87b3-7a3ba6c8f97c" />

Then in your wrapper config Go to "Tools" Tab and open Config Utility

<img width="522" height="586" alt="Capture d’écran 2025-08-05 à 12 17 03" src="https://github.com/user-attachments/assets/5797e9a6-7f3f-47ad-8700-a059e7aca3d7" />

Go to "Libraries" Put in "New replacement for :" (press add every time)

- d3dcore
- d3d11
- dxgi
- winemetal

Edit every libraries to "Native, Builtin" and apply

______________________________

### Game Related

Download "wmdrmsdk.dll" (You can safely download it from [DLL-files.com](https://www.dll-files.com/wmdrmsdk.dll.html))

Extract it and replace the DLLs in:

```bash
/Users/"YourName"/Applications/Kegworks/"Wrappername.app"/Content/SharedSupport/prefix/drive_c/windows/system32
```

And

```bash
/Users/"YourName"/Applications/Kegworks/"Wrappername.app"/Content/SharedSupport/prefix/drive_c/windows/syswow64
```

(To open the wrapper files, Select your app, right-click and "Show Package Content")

<img width="753" height="437" alt="Capture d’écran 2025-08-05 à 12 14 34" src="https://github.com/user-attachments/assets/94ef9b7a-59ee-4c44-87b3-7a3ba6c8f97c" />

Then in your wrapper config Go to "Tools" Tab and open Config Utility

<img width="522" height="586" alt="Capture d’écran 2025-08-05 à 14 43 25" src="https://github.com/user-attachments/assets/03bf8ad1-97ee-4370-9691-0b32b7e1c26b" />

Go to "Libraries" Put in "New replacement for :"

"wmdrmsdk" and Set it on native

Apply and close.

_____________________________________

## Install the game

Copy Bloodstrike's installer anywhere in

```bash
/Users/"YourName"/applications/Kegworks/"WrapperName"/SharedSupport/prefix/drive_c/Users/Kegworks
```

<img width="1304" height="697" alt="Capture d’écran 2025-08-05 à 14 45 10" src="https://github.com/user-attachments/assets/c389459e-eade-4371-b627-08229388a6af" />

In Open Control Panel from the tool tab and go in "Add/remove Programs"

<img width="568" height="524" alt="Capture d’écran 2025-08-05 à 14 47 02" src="https://github.com/user-attachments/assets/8fe7afc0-190a-446c-beb8-346cf5d2e34c" />

Tap Install at the Top Right

And select the installer.

Then you'll likely to be prompted to install gecko, install it then accept the EULA.

Follows Bloodstrike installation process.

When it installed close any wine windows and go to the "Configuration" tab of KegworksConfig

<img width="753" height="437" alt="Capture d’écran 2025-08-05 à 14 54 13" src="https://github.com/user-attachments/assets/ee398932-f76e-4a72-81d7-221b47fa258d" />

Tap "Browse at the Top-Right and go to:

```bash
/Users/"YourName"/applications/Kegworks/"WrapperName"/SharedSupport/prefix/drive_c/Program Files (x86)/bloodstrike/
```

Then select "launcher.exe".

Tap Test run on the Bottom-Right and let it continue the installation process.

Refuse if you're prompted to install Gecko a second time.

Select your login method and login normally. 

(When safari shows up be sure to uncheck temporarily "Warn when visiting a website using HTTP" in safari settings under the "Security" tab or it will block the login process feel free to re-enable it after logging-in)

Accept the Terms And Conditions.

Close the app, tap no on the log popup, close KegworksConfig.

Start the Game from Launchpad and it should be good to go.

_______________________________

## Bonus

If you want to make it look better,

Simply download the [icon of the game](https://cdn.moogold.com/2023/11/blood-strike.jpg)

Go to the Wrapper's .app

```bash
/Users/"YourName"/applications/kegworks/
```

Right-click it and tap "Get Info"

<img width="343" height="922" alt="Capture d’écran 2025-08-05 à 15 13 29" src="https://github.com/user-attachments/assets/dbad0a5d-7207-4777-ae91-eb2d10769130" />

Drag and Drop the jpg file onto the app icon on the Top-Left

(And if not done already you can name it as exemple "BloodStrike" For easier recognition).
