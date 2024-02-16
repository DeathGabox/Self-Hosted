After using adb for deleting, try to delete from android, something like "insert game here", and list what you can't, that apps you need to force with adb

In your pc, you need to install adb, in arch for example(links lazy) or in windows here(Put Links lazy)

---
Useful Info
- Start Server -> `adb start-server`
- connect adb connect -> `ip:port(5555)`
- Install apk from pc to device with -> `adb install -r apk.apk`
- you can search packet with -> `adb shell pm list package | sort -n | rg "word"`
- Copy files from device to pc ->  `adb pull remote_file source destination`
- Copy files from Notebook to device -> `adb push local_file source destination`
- Start Shell -> `adb shell`

---
Next is install following apps
- [Smarttube](https://github.com/yuliskov/smarttube)
- [LeanKey Keyboard Pro](https://github.com/yuliskov/LeanKeyKeyboard)
- [Projectivy](https://github.com/spocky/miproja1)

---

Now delete all this with `adb shell pm uninstall -k --user 0 package.name` ,except if you using, duh

if you screw some package, re-install with -> `adb shell cmd package install-existing name.package`

Or Disable with `adb shell pm disable-user --user 0 package.name`

If you screw something, revert with `adb shell pm enable package.name`

---

Package Names ^^

Amazon Prime -> `com.amazon.amazonvideo.livingroom`

TV Launcher (Stupids Ads) -> `com.google.android.tvlauncher`

Why you want a Camera?? -> `com.android.camera2`

Xiaomi Music Player -> `com.google.android.music`

Xiaomi Video Player -> `com.google.android.videos`

Teclado en Latin -> `com.google.android.inputmethod.latin`

Input japones -> `com.google.android.inputmethod.japanese`

Google App -> `com.google.android.katniss`

Calendar -> `com.android.providers.calendar`

Contacts -> `com.android.providers.contacts`

Dictionary -> `com.android.providers.userdictionary`

Feedback -> `com.google.android.feedback`

tts -> `com.google.android.tts`

TalkBack -> `com.google.android.marvin.talkback`

Partnersetup -> `com.google.android.partnersetup`

Speech -> `com.google.android.speech.pumpkin`

Sync Calendar -> `com.google.android.syncadapters.calendar`

Sync Contacts -> `com.google.android.syncadapters.contacts`

Bug sender -> `com.google.android.tv.bugreportsender`

Search for printers -> `com.android.printspooler`

HTML Viewer -> `com.android.htmlviewer`

Youtube -> `com.google.android.youtube.tv`

Youtube Music -> `com.google.android.youtube.tvmusic`

TV Channels (Thanks god) -> `com.google.android.tv`

TV Bloatware -> `com.google.android.tvrecommendations`

Google Play Games -> `com.google.android.play.games`

Xiaomi TvBox Launcher i guess -> `com.mitv.tvhome.atv`

Xiaomi Updates -> `com.xiaomi.mitv.updateservice`

Crapware -> `tv.alphonso.alphonso_eula`

Telemetry -> `com.miui.tv.analytics`

MiChannel -> `com.mitv.tvhome.michannel`

Partner -> `com.xiaomi.android.tvsetup.partnercustomizer`

Xiaomi Services -> `mitv.service`

Link to what -> `com.mitv.milinkservice`

Xiaomi Telemetry -> `com.xiaomi.mitv.res`

Download Crapware -> `com.mitv.download.service`

Auto-install crapware -> `android.autoinstalls.config.xioami.mibox3`

---

Useful Links

[Principal Inspiration](https://sites.google.com/site/tweakradje/devices/xiaomi-mi-tv-stick)

Thakyou XDA Devs
