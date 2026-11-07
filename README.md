[README.txt](https://github.com/user-attachments/files/34509614/README.txt)
LAPTOP MIRROR (desktop app): laptop screen -> phone over USB cable, phone touch controls the laptop.

WINDOWS APP (no installs needed, ffmpeg + adb are bundled)
 1. Create a free GitHub repo, upload ALL files of this folder (keep the .github folder).
 2. Actions tab > "Build Windows app" (about 3 min) > Artifacts > download LaptopMirror-Windows > unzip.
 3. Run LaptopMirror.exe.
 Phone: Developer options > USB debugging ON; install the Screen Mirror APK; plug the cable, accept the prompt.
 Then: phone app > Receive, laptop app > START. Touch the phone = mouse on the laptop.

MAC / LINUX (run from source)
 pip install pyautogui ; install ffmpeg + adb ; python laptop_app.py
 Mac: allow Screen Recording for Terminal. Linux: X11 session (not Wayland).

QUALITY: "Fast (low lag)" 720p-ish, "Balanced" 1080p 15 Mbps, "Sharp" 1080p 25 Mbps. Uses the GPU encoder when available.
The app waits and reconnects by itself if you unplug or reopen Receive.
