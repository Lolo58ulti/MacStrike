# Disclaimer / Legal Disclaimer
I cannot guaranty that it will work on your system. This is **HIGHLY experimental** and may even cause your computer to crash. 

I am not responsible for any damage or data loss caused to your device as result of following this guide. Use at your own risk.

This project is not related to any mentioned software companies

**Do not report any issues to [NetEase Games](https://www.neteasegames.com)**
 
For wine related issues, please refer to [WineHQ](winehq.org),

And for KegWorks related issues, please refer to [KegWorks](https://github.com/Kegworks-App/Kegworks).
 
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

Tap the + Icon and Select 
