# Strumline — ukulele tab player for Android

Plays ukulele tabs (G C E A) and scrolls them under a playhead while you play.

- **Tempo mode** scrolls at a set BPM, with optional count-in and metronome.
- **Listen mode** uses the microphone: the tab waits on the highlighted note and moves on each time it hears you pluck or strum. Turn Sensitivity up if it misses notes, down if it skips ahead.
- Tap the tab to play/pause, drag it to scrub, ‹ › step one note.
- Paste your own tabs (four lines starting `A|`, `E|`, `C|`, `G|`); they're saved on the phone.
- The screen stays on while the app is open.

## Get the APK

**Option A, no install needed (GitHub Actions):** push this folder to a GitHub repo. The
`Build APK` workflow runs automatically; open the run under the Actions tab and download
`strumline-apk`. Unzip it and open `app-debug.apk` on your phone (allow "Install unknown apps"
for your browser or file manager when asked).

**Option B, Android Studio:** File → Open → this folder, let Gradle sync, then
Run ▶ with your phone plugged in (USB debugging on), or Build → Build APK(s).

**Option C, command line** (with the Android SDK installed and `ANDROID_HOME` set):
`./gradlew assembleDebug` → `app/build/outputs/apk/debug/app-debug.apk`

## Changing the app

The whole player is one file: `app/src/main/assets/index.html`. Edit it and rebuild.
It's served from `https://appassets.androidplatform.net/` so the microphone is allowed.
