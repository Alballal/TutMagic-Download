<p align="center"><img src="docs/images/logo.png" alt="TutMagic logo" width="200"></p>

# TutMagic — Hand Gesture Control for Windows

Control your mouse and presentations with hand gestures through your webcam. **Portable: no installation, no Python, no internet needed.**

> صدقة جارية على روح ابى وحبيبي محمود البلال

**Version 0.6.0** · Windows 10/11 (64-bit) · English & Arabic interface · Free to use

![TutMagic dashboard](docs/images/dashboard.jpg)

## Download and run

1. Go to the [**Releases**](../../releases) page and download the portable ZIP (`TutMagic … Windows Portable.zip`).
2. Right-click the ZIP → **Extract All**, and move the folder somewhere permanent (for example *Documents*). Do not run it from inside the ZIP, and keep `TutMagic.exe` together with its `_internal` folder.
3. Double-click **`TutMagic.exe`**.
4. If Windows SmartScreen shows *"Windows protected your PC"*, the app is new and not code-signed. If you trust the source, click **More info → Run anyway**. Do not disable Windows protection.
5. Click **Connect camera** (allow desktop apps to use the camera in *Settings → Privacy & security → Camera* if asked).
6. Choose **Mouse control** or **Presentation**, open your hand in front of the camera, then click **Enable control** or press **F8**.

Stop at any time with **F8**, or by showing an open palm. Moving the real mouse into a screen corner is an emergency stop.

For a step-by-step interactive guide with screenshots, open [`TutMagic_Guide.html`](TutMagic_Guide.html) in your browser (Arabic).

## Gestures at a glance

| Gesture | Mouse mode | Presentation mode |
|---|---|---|
| Thumb + index pinch | Click · hold to drag | Play / pause (Space) |
| Index finger up | Move the cursor | Red laser pointer |
| Index + middle fingers | Scroll up / down | Sweep sideways to change slide |
| Thumb + middle pinch | Right click | — |
| Index pointing right / left | Move the cursor | Next / previous slide |
| Thumb up / down | — | Volume up / down |
| Open palm | **Stop control** | **Stop control** |

All gestures are customisable in **Gesture bindings**. **Gesture studio** shows animated references.

![Gesture studio](docs/images/gesture-studio.jpg)

## Features

- Webcam hand tracking with MediaPipe, processed locally on your computer.
- Steady pointer (speed-adaptive smoothing) and accurate clicks.
- Mouse mode: move, click, drag, right click, scroll.
- Presentation mode: slides, laser pointer, volume, media control.
- Custom gestures, settings import/export, tray icon, global shortcut, on-screen status badge.
- Pinch calibration and camera search in **Preferences**.

![Preferences](docs/images/preferences.jpg)

## Privacy

Camera frames are processed on your device and are never sent anywhere by TutMagic. Settings and logs are stored in `%LOCALAPPDATA%\TutMagic` (`settings.json`, `app.log`). To remove everything, delete the app folder and that folder.

## Troubleshooting

| Problem | What to do |
|---|---|
| Does not start / missing file error | Extract the whole ZIP; `_internal` must sit next to `TutMagic.exe`. If a DLL is reported missing, install *Microsoft Visual C++ Redistributable (x64)*. |
| File removed by antivirus | Restore it from quarantine or re-download; unsigned new apps are sometimes flagged. |
| Camera black or not opening | Check camera privacy settings, close Teams/Zoom, then use **Preferences → Find cameras**. |
| F8 does nothing | Another app may use it (or press **Fn**). Change it in **Preferences**. |
| Commands ignored in some apps | Windows blocks input into windows running as administrator; run TutMagic the same way. |
| Jittery pointer / hard clicks | Improve lighting; adjust sliders or use **Calibrate pinch**. |

## Documentation

- [Arabic guide / الشرح بالعربية](README_AR.md)
- [License](LICENSE.txt)

## License

**TutMagic Free-Use License** © 2026 Abdelrahman Mahmoud Al-Ballal. Free to use, including at work. Selling, modifying and redistributing modified copies are not permitted; you may share the unmodified complete package free of charge. See [LICENSE.txt](LICENSE.txt). Versions before 0.6.0 were released under the MIT License. Third-party components (MediaPipe, OpenCV, NumPy, Pillow, pystray, etc.) keep their own licenses, included in the app's `THIRD_PARTY_LICENSES` folder.
