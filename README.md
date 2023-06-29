# Banking on Android Open Source Project (AOSP)

Banking apps detect unsecure environments, and here I document how to bypass them in custom ROM's

## Setup

0. orangefox recovery & unlocked bootloader
1. Install LineageOS
2. Spoof device signature with [MagiskHide Props Config](https://github.com/Magisk-Modules-Repo/MagiskHidePropsConf)
3. hide custom rom props with [this](https://github.com/Magisk-Modules-Alt-Repo/ezme-nodebug) module, reset them with [this](https://github.com/Magisk-Modules-Alt-Repo/sensitive_props)
4. install [shamiko](https://github.com/LSPosed/LSPosed.github.io/releases)
5. [safetynet fix](https://github.com/Displax/safetynet-fix)
6. edit additional build.prop entries that may have rom name with [this](https://github.com/Magisk-Modules-Repo/MagiskHidePropsConf) 
7. [mindthegapps](https://wiki.lineageos.org/gapps)
8. Add Google play Services, Google play store, google services framework and google play protect to denylist
9. hide magisk, freeze the app (android 13 inbuilt)

## Lsposed

[Hide My App List](https://github.com/Dr-TSNG/Hide-My-Applist)

## Debugging

[WADB](https://github.com/RikkaApps/WADB)

## Widewine

liboemcryptodisabler module 

## Tests

* [Play integrety api checker](https://play.google.com/store/apps/details?id=gr.nikolasspyr.integritycheck)
* [yasnac](https://github.com/RikkaW/YASNAC)
* [Ruru (Applist detector)](https://github.com/byxiaorun/Ruru)

## Current Target App

[Payzapp](https://play.google.com/store/apps/details?id=com.hdfcbank.payzapp&hl=en&gl=US)

## References

* https://forum.xda-developers.com/t/hide-root-magisk-lsposed-and-pass-safetynet-on-any-rom-on-redmi-k20-pro.4552467/
* https://github.com/freeload101/Java-Android-Magisk-Burp-Objection-Root-Emulator-Easy
