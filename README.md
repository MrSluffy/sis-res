# Substratum Icons Special A11 (resources used)

 - layout
 - drawable
 - dimens
 - integer
 - color

## Create your own Module to used S.I.S in your favorite android 11 custom roms 
- For educational purposes only
- I'm no responsible for any damage on your device. Do this at on your own risk*

## Step 0: PRECONFIGURATIONS!
Install/Used Apktool for PC [here](https://ibotpeaches.github.io/Apktool/)

for mobile `ApkToolX by AndroBlack` [arm7](https://androidfilehost.com/?fid=4349826312261827487) [arm64](https://androidfilehost.com/?fid=4349826312261827488)
Zarchiever.apk [here](https://play.google.com/store/apps/details?id=ru.zdevs.zarchiver)
vrtheme [XDA](https://forum.xda-developers.com/t/mod-magisk-android-11-addon-features-for-pixel-devices-pixel-4a-thread.4215069/), [github](https://github.com/ElTifo/CustomSettingsForDevs/tree/Pixel4a/app/src/mods) 

`ApkToolX Requirements`
- Your rom should permissive [here](https://t.me/permissiver/2)
- BusyBox NDK (Optional) [repo](https://github.com/Magisk-Modules-Repo/busybox-ndk)
- Root [Magisk](https://github.com/topjohnwu/Magisk/releases)


##  Installing Apktool X in Mobile
Install Apktool X like normal application apk
after installing it will ask again to install .Install once again

Open ApktoolX then go to Settings

*Check/tick Add Apktool and Option flags
*Install OpenJDK 

See Sreenshot for references
<img src="https://github.com/MrSluffy/sis-res/blob/A11/Screenshot_20210327-091326_Apktool_X.png?raw=true">

- Now Importing framework in Apktool X
- Go to system folder -> framework -> framework-res.apk
- click framework-res.apk and choose import as framework
- done

## Decompiling / Recompiling SystemUI

- Make a folder in your sdcard and name it as `Mod`
- using [root explorer](https://rootexplorer.co/download-apk/) copy your SystemUI.apk in created Mod folder
```
/system/system_ext/priv-app/SystemUI
```
- Now open Apktool X goto Mod folder
- Click SystemUI.apk Choose Decompile res
- Using [TextEditor](https://play.google.com/store/apps/details?id=com.rhmsoft.edit) open sdcard/Mod/SystemUI_src/res/values/styles.xml 

```
Search this styles

<style name="Keyguard.ImageButton.NumPadDelete" parent="@android:style/Widget.ImageButton">

you will see duplicate attribute which is

<item name="android:src">@drawable/ic_backspace_black_24dp</item>

delete that line

See for reference
==========================================
from this

    <style name="Keyguard.ImageButton.NumPadDelete" parent="@android:style/Widget.ImageButton">
        <item name="android:paddingBottom">11.0sp</item>
        <item name="android:src">@drawable/ic_backspace_black_24dp</item>
        <item name="android:src">@drawable/ic_backspace_black_24dp</item>
        <item name="android:tint">@color/pin_delete_color</item>
        <item name="android:tintMode">src_in</item>
    </style>
    
    to This 

        <style name="Keyguard.ImageButton.NumPadDelete" parent="@android:style/Widget.ImageButton">
        <item name="android:paddingBottom">11.0sp</item>
        <item name="android:src">@drawable/ic_backspace_black_24dp</item>
        <item name="android:tint">@color/pin_delete_color</item>
        <item name="android:tintMode">src_in</item>
    </style>

==========================================

and Same with 

<style name="TextAppearance.NotificationImportanceApp" parent="@style/TextAppearance">

<style name="TextAppearance.NotificationImportanceChannel" parent="@style/TextAppearance">
  
<style name="TextAppearance.NotificationImportanceChannelGroup" parent="@style/TextAppearance">

Delete the duplicated attribute 

```
- Now Open Apktool X and tap SystemUI_src and choose Recompile


## Create Module to Support S.I.S

You already learn Decompiling and Recompiling SystemUI 
- Now to create S.I.S Module
- In my provided files 
- in `toMerge` folder , Copy layout and drawable folder and paste it to your SystemUI_src/res/HERE
- in `toCompare` Compare S.I.S layout to your SystemUI_src
```
How to properly compare:
open 2 files

file 1: a file from the "ToCompare" folder
file 2: a file with the same name from your /res/layout folder

search for "Compare start" in the "ToCompare" file
check if your file looks the same as the "ToCompare" file

do this until you reach "Compare stop"



Repeat for all files in the "ToCompare" folder
 ```
*Note Compare not Replace!
- Now Recompile!

## Replacing
- In your Zarchiever
- Open SystemUI_src.apk
- and all the modified res copy and replace it inside the 
- S.I.SvrTheme[MAGISK].zip vrtheme/system/system_ext/priv-app/SystemUI/Systemui.apk/res/HERE folder
- now install your S.I.SvrTheme[MAGISK].zip in your Magisk
- And Enjoy [S.I.S A11](https://t.me/sluffy_icons)


# [Credits & Thanks](https://telegra.ph/Credits-And-Thank-08-16)
