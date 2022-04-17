# I use browsers without installing them!
Every browsers that I'm using, I never install them as system program files, even if it's preinstalled, I will immediately delete them out and execute only from other updater clients.
> [RIP Edge](https://github.com/AveYo/fox/blob/main/Edge_Removal.bat)...

### Recommended tools
- [henry++'s ChrLauncher](https://github.com/henrypp/chrlauncher) for download and update `Chromium`, also can select other forks to use, include between `sync` and `nosync`, also `clang`, `ungoogled`, or setup as launcher with custom arguments for any browsers.
  > Pleases note that even you want to use the `sync` fork, don't expected it will works like `Google Chrome`, they've limited **Chromium** and other forks to access their **Sync APIs** (and anythings that rely to) until you join back to them! (Indeed, they need you to install **Google Chrome** and keep using it!)
- [UndertakerBen's](https://github.com/UndertakerBen) portable updater of common(ly bloated) browsers...
  - Brave
  - Chrome
  - Firefox
  - Edge (Chromium)
  - Opera (Chromium)

### Tips for setting up any browsers as semi-portable
- If you download some branded browser or want to download common browsers manually without portable tools, make sure that you're downloading `standalone` setup file rather than `stub` because the installer size is only few megabytes or less than that and it doesn't contain all of necessary browser executable and files, only use for download browser program files remotely, then deploy into `%ProgramFiles%` or `%ProgramFiles(x86)%`.
- After that, you can use [7-zip](https://7-zip.org) to exteact all files of its browser setup program, then you can execute them without installing, all of browser profile data will be save at default place of your `%appdata%` or `%localappdata%` or maybe both, unless you've placed some placeholder file to make its browser work as portable mode\*.
  > \* Only for Chrome and/or Chromium-based, as I know.
- For Firefox and any of gecko/goanna/servo based or something, just extract everything inside `core` folder in setup file.
- For any chromium-based browser, you need two steps of extraction.
  1. Extract `chrome.7z` or if it's branded forks, e.g. `Vivaldi`, `Whale`, etc. the name formatting should be `<brand>.7z`
  2. Then move its `chrome-bin` or `<brand>-bin` files inside its folder to anywhere you want.

### Recommendation note for Firefox and any browsers that based on it
Go delete system addons in `/browser/features/*.xpi`, it's not needed unless...
- `doh-rollout@mozilla.org.xpi`: If you wish to use in-browser **DNS-over-HTTPS**, but mind ahead that it will use `Cloudflare` servers at the beginning, however, deleting this will make you no longer use its feature until you bring this **XPI** back!
- ~~`formautofill@mozilla.org.xpi`~~: Well, if you want to save registration form (and also credit cards), but in my opinion, I won't recommended to keep this!
- `pictureinpicture@mozilla.org.xpi`: This should be keep retain, otherwise you cannot view videos in PiP popup (Like Chrome)
- `proxy-failover@mozilla.org.xpi`: Deleting this will prevent "step down" connections to direct or system connections in case if your connections to proxy are failed, however, directly change connection settings still possible.
- `screenshots@mozilla.org.xpi`: In case if you want to make screencap in browser without (Win+)? **Print screen** or want to capture entire page (with scrolling) into single image, keep in mind that it's possible to upload and share your screencap back to Mozilla, safe to remove if you don't want to upload and want to capture screen manually without this assist tool!
- ~~`webcompat@mozilla.org.xpi`~~ and ~~`webcompat-reporter@mozilla.org.xpi`~~: I recommend to not keeping them, even it's legitimately use for report incompatibility sites that won't work for Firefox itself, but their add-ons about this are part of their `Telemetry`, so prefer to remove is better!

### Eligibility of policies configuration

| Browsers / Policy methods  | ADMX (gpedit.msc) | Policies Registry | JSON Distribution |
|----------------------------|-------------------|-------------------|-------------------|
| **Chromium based**         |                   |                   |                   |
| Chrome                     | :o:               | :o:               | :x:               |
| Chromium / Rest of forks\* | :x:               | :o:               | :x:               |
| Brave                      | :x:               | :o:               | :x:               |
| Vivaldi                    | :x:               | :o:               | :x:               |
| Whale                      | :x:               | :o:               | :x:               |
| Opera Chromium (also GX)   | :x:               | :x:               | :x:               |
| **Gecko-based** (Servo)    |                   |                   |                   |
| Firefox                    | :o:               | :o:               | :o:               |
| IceCat / Iceweasel         | :x:               | :o:               | :o:               |
| Librewolf                  | :x:               | :o:               | :o:               |
| Thunderbird (Mail)         | :x:               | :o:               | :o:               |
| **Gecko-based** (Goanna)   |                   |                   |                   |
| Basilisk / Pale Moon       | :x:               | :x:               | :x:               |
| Interlink (Mail)           | :x:               | :x:               | :x:               |

\* e.g. Kinza, Iridium, Iron, Slimjet, etc (Electron apps, RPGMaker MV~MZ and any newer also affected!)

Note: Only `Windows` platform, this won't include remote policy, e.g. Active Directory, Device Policy, etc.

### Browsers download lists
- [Iridium](https://iridiumbrowser.de)
- [Kinza](https://kinza.jp/en)
- [Librewolf](https://gitlab.com/librewolf-community/browser)
- [Naver Whale](https://whale.naver.com/en/download)
- [Slimjet](https://www.slimjet.com/en/dlpage.php)
- Vivaldi [Stable](https://vivaldi.com/download) \/ [Snapshot](https://vivaldi.com/blog/desktop/snapshots)