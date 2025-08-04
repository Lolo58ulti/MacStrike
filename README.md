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

[MacPort Official Website](https://www.macports.org/install.php)

[KegWorks Winery](https://github.com/Kegworks-App/Kegworks)

```bash
brew install --cask --no-quarantine Kegworks-App/kegworks/kegworks
```

Or

```bash
sudo port install kegworks
```

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

