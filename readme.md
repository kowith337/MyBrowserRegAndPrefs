# I use browsers without installing them!
Every browsers that I'm using, I never install them as system program files, even if it's preinstalled, I will immediately delete them out and execute only from other updater clients.
> [RIP Edge](https://github.com/AveYo/fox/blob/main/Edge_Removal.bat)...

### Recommended tools
- [henry++'s ChrLauncher](https://github.com/henrypp/chrlauncher) for download and update `Chromium`, also can select other forks to use, include between `sync` and `nosync`, also `ungoogled`, or setup as launcher with custom arguments for any browsers.
  > Pleases note that even you want to use the `sync` fork, don't expected it will works like `Google Chrome`, they've limited **Chromium** and other forks to access their **Sync APIs** (and anythings that rely to) until you join back to them! (Indeed, they need you to install **Google Chrome** and using it!)
- [UndertakerBen's](https://github.com/UndertakerBen) portable updater of common(ly bloated) browsers...
  - [Brave](https://github.com/UndertakerBen/PorBraveUpd)
  - [Chrome](https://github.com/UndertakerBen/PorChromeUpd)
  - [Firefox](https://github.com/UndertakerBen/PorFirefoxUpd)
  - [Edge (Chromium)](https://github.com/UndertakerBen/PorEdgeUpd)
  - [Opera (Chromium)](https://github.com/UndertakerBen/PorOperaUpd)

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
- `doh-rollout@mozilla.org.xpi`: If you wish to use in-browser **DNS-over-HTTPS**, but mind ahead that it will use **`Cloudflare-backend`** Mozilla servers at the beginning and it's doesn't use the same IP address of `Cloudflare` itself, however, deleting this will make you no longer use its feature for older version approx less than 100 until you bring this **XPI** back!
- ~~`formautofill@mozilla.org.xpi`~~: Well, if you want to _save registration form_ **(and also credit cards)**, but in my opinion, I won't recommended to keep this!
- `pictureinpicture@mozilla.org.xpi`: This should be keep retain, otherwise you cannot view videos in PiP popup (Like Chrome)
- ~~`proxy-failover@mozilla.org.xpi`~~: Deleting this will possibly prevent "step down" connections to direct or system connections in case if your connections to proxy are failed, however, directly change connection settings still possible.
- `screenshots@mozilla.org.xpi`: In case if you want to make screencap in browser without (Win+)? **Print screen** or want to capture entire page (with scrolling) into single image, keep in mind that _it's possible to upload and share your screencap_ back to `Mozilla`, safe to remove if you don't want to upload and want to capture screen manually without this assist tool!
- ~~`webcompat@mozilla.org.xpi`~~ and ~~`webcompat-reporter@mozilla.org.xpi`~~: I recommend to not keeping them, even it's legitimately use for report incompatibility sites that won't work for Firefox itself _(because **Chromium** were dominated the world's browser standard nowadays)_, but their add-ons about this are part of their `Telemetry`, so prefer to remove is better!

### Eligibility of policies configuration

|--------------------------------------------|-------------------|-------------------|-------------------|
| Browsers / Policy methods                  | ADMX (gpedit.msc) | Policies Registry | JSON Distribution |
|--------------------------------------------|-------------------|-------------------|-------------------|
| **Chromium based**                         |                   |                   |                   |
| Chrome                                     | :o:               | :o:               | :x:               |
| Chromium\*                                 | :x:               | :o:               | :x:               |
| Brave                                      | :x:               | :o:               | :x:               |
| Vivaldi                                    | :x:               | :o:               | :x:               |
| Whale                                      | :x:               | :o:               | :x:               |
| Opera Chromium (also GX)                   | :x:               | :x:               | :x:               |
| **Gecko-based** (Post Gecko \/ Servo)      |                   |                   |                   |
| Firefox                                    | :o:               | :o:               | :o:               |
| Librewolf                                  | :x:               | :o:               | :o:               |
| Mercury                                    | :x:               | :o:               | :o:               |
| Thunderbird (E-mail client)                | :x:               | :o:               | :o:               |
| ~~IceCat~~ (Outdated)                      | :x:               | :o:               | :o:               |
| ~~Iceweasel~~ (Outdated)                   | :x:               | :o:               | :o:               |
| **Gecko-based** (Pre-servo XUL \/ Goanna ) |                   |                   |                   |
| Basilisk / Pale Moon                       | :x:               | :x:               | :x:               |
| Interlink (E-mail client)                  | :x:               | :x:               | :x:               |
|--------------------------------------------|-------------------|-------------------|-------------------|

\* May include any of forks, e.g. Kinza, Iridium, Iron, Slimjet, Yandex, etc. Also all apps that based on Electron \[e.g. Discord, Telegram, Visual Studio Code\/VSCodium\], Games that use RPGMaker MV\/MZ engine and any newer also affected!

Note:
  1. Table list mean that each browsers will read policies within separate location according to each branded browser name.
  2. Only `Windows` platform, this won't include remote policy, e.g. Active Directory, Device Policy, etc.

### Browsers download lists
- [Iridium](https://iridiumbrowser.de)
- [Librewolf](https://gitlab.com/librewolf-community/browser)
- [Mercury](https://github.com/Alex313031/Mercury)
- Nonfree
  >- Vivaldi [Stable](https://vivaldi.com/download) \/ [Snapshot](https://vivaldi.com/blog/desktop/snapshots)
  >- [~~Naver Whale~~](https://whale.naver.com/en/download) _Communicate to Naver services from the beginning and every each sessions_
- Outdated
  >- [~~Kinza~~](https://kinza.jp/en)

### FYI / Reminder / Todo
- Brave Tor? **No!**
  - And also its search engine, I won't recommended it until they've allow users who turned off WebSocket and/or ServiceWorker eligible to use!
- [Spyware Watchdog Browser Lists](https://spyware.neocities.org/articles/index.html)
- `https://digdeeper.her.st/ghost/liftingtheveil.html`
- **Ungoogled Chromium** is the one and only Chromium browser that not attempt to connect to somewhere else, unless you've starting to browse the web or depend on extension that you've installed to...
  - e.g. Install [uBlock Origin](https://github.com/gorhill/uBlock) will be fetch filterlists automatically and cause browser make some requests before you go!
- `Naver Whale` will become **useless browser** because it will falsely detected as no internet available if you've blocked `Google` DNS IP address both IPv4 and IPv6, this may include blocking `CloudFlare` and `Google` DoH endpoint, too!
- ~~The final version of Kinza (since 2021/05/10) is based on Chromium 89, and **it's outdated now!** But I'm aware against `sec-ch-ua`, so I resist to use any higher than this if this browser still maintaining...~~
  > Update that access to Kinza website is now redirected to Dayz instead, seems like this browser are now end of life, farewell.
- Any registry or group policy configured to Chrome and/or Chromium-based browsers will be trigger an organisation mode, it will make DoH unconfigurable and I don't know this will cause DoH permanently off or not? Otherwise you can configure manually via regedit or group policy, if your device are not under any real organisations.
- To surviving against client hints of any post-88 Chrome\/Chromium, you need to put `--disable-features=UserAgentClientHint` within launch argument, I think certain good forks of Chromium that respect privacy enough (e.g. [Iridium](https://iridiumbrowser.de), [Ungoogled Chromium](https://github.com/macchrome/winchrome)) should apply out-of-box by default because detecting and exposing real browser environment data (such as OS, Browser brand, Version, CPU bits, etc.) could be dangerous, even though they trying to claim that it just use for security purpose, but I'll never believe them anyway!
  > Alternatively, use the [uazo's Bromite fork](https://github.com/uazo/bromite-buildtools) that heavily disabled client hints without adding the commands above!
- Not many branded chromium forks are add the function that delete everything once all browser windows are closed, but sad to say it's potentially have range from **high** to **extreme** of spyware behaviour...
- _Opera_ is **extremely high** bad behaviour, must use as disposable browser for low-data proxying. (their `VPN` {they've named that instead of **proxy**} is so slow, no matter about which regions you've selected to!)
  - It's very bad while using search engine, too! even you've install uBO and enabled `allow extension for search engine` doesn't mean it's work, esp. I've tested with [ASTLW](https://github.com/kowith337/PersonalFilterListCollection/tree/master/filterlist/other/SurvivedTrackingLinkWarning.txt) filterlist and found that it didn't prevent me against tracked parameters for selected default search engine!
  > Of course, Opera didn't give any ability to users to set another user-customised default search and remove any stock engine, it's too shame!!!

- - - - -