# Banking on Android Open Source Project (AOSP)

Banking apps detect unsecure environments, and here I document how to bypass them in custom ROM's

## Setup

0. unlocked bootloader & orangefox recovery
1. Install LineageOS
2. Spoof device signature with [MagiskHide Props Config](https://github.com/Magisk-Modules-Repo/MagiskHidePropsConf)
3. hide custom rom props with [this](https://github.com/Magisk-Modules-Alt-Repo/ezme-nodebug) module, reset them with [this](https://github.com/Magisk-Modules-Alt-Repo/sensitive_props)
4. install [shamiko](https://github.com/LSPosed/LSPosed.github.io/releases)
5. [safetynet fix](https://github.com/Displax/safetynet-fix)
6. (optional) edit additional build.prop entries that may have rom name with [this](https://github.com/Magisk-Modules-Repo/MagiskHidePropsConf) 
7. [mindthegapps](https://wiki.lineageos.org/gapps) / microg [sateynetAPI](https://github.com/microg/GmsCore/issues/1875)
8. Add Google play Services, Google play store, google services framework and google play protect to denylist
9. hide magisk, freeze the app (android 13 inbuilt), or use [appmanager](https://github.com/MuntashirAkon/AppManager)
10. can use work profile using [shelter](https://gitea.angry.im/PeterCxy/Shelter)

## Specific hiding

* [InitRcHider](https://forum.xda-developers.com/t/module-initrchider.4369285/)
* [unregular partition mounting](https://github.com/Magisk-Modules-Alt-Repo/magisk_overlayfs)
* bootloader / hardware attestation TODO

## Microg & Playstore

https://github.com/microg/GmsCore/wiki/Implementation-Status

https://gitlab.com/Nanolx/NanoDroid

## Magisk Forks

[Magisk Delta](https://github.com/HuskyDG/magisk-files/blob/main/intro.md)

## Debugging

[WADB](https://github.com/RikkaApps/WADB)

## Widewine

liboemcryptodisabler module 

## GrapheneOS

https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/

https://grapheneos.org/articles/attestation-compatibility-guide

## Tests

* [Play integrety api checker](https://play.google.com/store/apps/details?id=gr.nikolasspyr.integritycheck)
* [yasnac](https://github.com/RikkaW/YASNAC)
* [Ruru (Applist detector)](https://github.com/byxiaorun/Ruru)
* [Momo](https://t.me/magiskalpha/529)

## Debug & logging

[logcat reader](https://github.com/darshanparajuli/LogcatReader)
[Toast source](https://play.google.com/store/apps/details?id=pl.revanmj.toastsource&hl=en_US)
[Developer assitant](https://play.google.com/store/apps/details?id=com.appsisle.developerassistant&hl=en_US&gl=US)

## Apps hiding

1. [Lsposed](https://github.com/LSPosed/LSPosed)
2. [android faker](https://forum.xda-developers.com/t/app-xposed-8-1-12-android-faker-a-module-for-spoof-your-device.4284233/)
3. [hidemyapp list](https://github.com/Dr-TSNG/Hide-My-Applist)
4. [xprivacylua](https://github.com/M66B/XPrivacyLua)

## Current Target App

[Payzapp](https://play.google.com/store/apps/details?id=com.hdfcbank.payzapp&hl=en&gl=US) | hdfc privsec [report](https://github.com/PrivSec-dev/banking-apps-compat-report/issues/138)

Payzap runs once can't verify number/(loading) then this toast.

```
Your device bootloader is unlocked or verified boot state is unverified. You cannot use this application.
```

Nothing in logs

ruru -> sees xprivacylua somehow

yasnac -> basic integrety pass

play integrety api checker -> everything is red

**Momo**

![momo](https://github.com/lepras/bankingAOSP/assets/109689648/db0d25e7-1a91-4062-bfe7-df99dd1708ca)

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
