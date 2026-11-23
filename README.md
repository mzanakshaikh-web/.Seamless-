# Seamless 5.0
A music player that never lets a song end abruptly. Developed by Shaikh Mzanak.

## Build
Upload `seamless.zip` to your repo (see `workflow-for-zip-upload.yml`), commit, and download
`Seamless.apk` from **Releases**. The release text says whether the on-device lyrics engine was included.

## Lyrics (on-device)
The app decodes each song and a speech model (whisper.cpp, bundled in the APK) writes out the words with timing.
Results are saved on the phone. Lyrics stored in the song file or as `.lrc` files next to it are used first.
Accuracy on singing and rap over loud music is limited. Online download is optional and off by default.

## Infinity
Next song is preloaded, silent intros/outros are skipped, levels are matched, and the fade keeps headroom
so overlapping loud songs never clip.

## 4.0
- Dark-mode text fixed. Skipping songs no longer cuts audio: every change ramps smoothly and the default blend curve can never clip.
- Reactive beat circle on the player (Settings > Player > Beat circle).
- Lyrics appear while the speech engine is still listening. Engine status is shown in Settings > Lyrics.
- New icon.

## 5.0
- Icon: your own flowing-lines artwork.
- Spotify-style player (Playing from album, title row with Infinity button, thin seek bar, lyrics card).
- 8 reactive circle styles: Bars, Rings, Wave, Dots, Pulse, Starburst, Orbit, Ripple.
- Surface looks: Standard, Matte, Liquid glass, Crystal (Settings > Appearance).
- main.yml in this zip is the paste-ready workflow for .github/workflows/main.yml.
