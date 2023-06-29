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
7. [mindthegapps](https://wiki.lineageos.org/gapps) / microg [sateynetAPI](https://github.com/microg/GmsCore/issues/1875)
8. Add Google play Services, Google play store, google services framework and google play protect to denylist
9. hide magisk, freeze the app (android 13 inbuilt)

## Microg & Playstore

https://github.com/microg/GmsCore/wiki/Implementation-Status

https://gitlab.com/Nanolx/NanoDroid

## Magisk Forks

[Magisk Delta](https://github.com/HuskyDG/magisk-files/blob/main/intro.md)

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

## Tricks

```
1. Installing and activating the app on rom with gapps
2. Backing up app+data using neobackup
3. Wiping the phone, flashing clean rom
4. Restoring the app from the backup there
```

## News / Changelog

Hardware Attestation
2023-06-07 UTC

https://developer.android.com/training/articles/security-key-attestation

## References

* https://forum.xda-developers.com/t/hide-root-magisk-lsposed-and-pass-safetynet-on-any-rom-on-redmi-k20-pro.4552467/
* https://github.com/freeload101/Java-Android-Magisk-Burp-Objection-Root-Emulator-Easy
