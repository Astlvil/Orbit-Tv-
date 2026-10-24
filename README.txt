ORBIT TV v2 - build online, install on Skyworth

A. BUILD (computer)
 1. github.com > New repository (Public) > upload ALL files from this zip, then Commit.
    The folder ".github" is hidden on your computer and often skipped by drag-and-drop.
    After uploading, check the repository shows a ".github" folder. If not:
    Add file > Create new file > name it  .github/workflows/build.yml
    and paste the text from build-workflow-copy.txt.
 2. Open the Actions tab and wait for a green tick (5-10 min).
 3. Your APK is on the repository's Releases page as OrbitTV.apk.
    Direct link:  https://github.com/YOUR_NAME/YOUR_REPO/releases/latest/download/OrbitTV.apk

B. INSTALL (TV)
 1. Install the "Downloader" app on the TV.
 2. Settings > Apps > Security & restrictions > Install unknown apps > allow Downloader.
 3. In Downloader enter the direct link, download, press Install, then Open.
 4. Do NOT try to install a .zip. The file must be OrbitTV.apk.
 5. If a different/older Orbit TV is installed, uninstall it first.

C. OPTIONAL: make it the home screen (needs ADB on a computer)
 adb connect TV_IP:5555
 adb shell cmd package set-home-activity com.orbit.tv/.MainActivity
 Undo: adb uninstall com.orbit.tv
