# 🎮 Pose-Controlled Game Interface using MediaPipe & OpenCV

This project allows you to control keyboard-based games using **body gestures** detected through a webcam. Leveraging **MediaPipe's pose estimation**, you can move left/right, jump, crouch, and start the game with a clap — all without touching your keyboard!

## 🚀 Features

- ✋ **Clap to Start**: Begin the game by joining your hands (detected as a "clap").
- 👈 👉 **Move Left/Right**: Move based on the position of your shoulders.
- ⬆️ **Jump Detection**: Jump when you rise above a calibrated vertical position.
- ⬇️ **Crouch Detection**: Crouch when you dip below the calibrated position.
- 🖱️ **Auto-click**: Automatically clicks the game window to focus when starting.

## 🧠 Tech Stack

- **Python**
- **OpenCV** for image processing and webcam control
- **MediaPipe** for pose landmark detection
- **PyAutoGUI** for simulating keyboard and mouse input
- **Matplotlib** (optional, for visualization/debugging)

## 🖥️ How it Works

1. **Webcam Feed** is captured using OpenCV.
2. **Pose Estimation** is performed using MediaPipe's `Pose` module.
3. **Key Landmarks** (shoulders, wrists) are used to:
   - Determine if hands are joined
   - Check shoulder positions for left/right movement
   - Detect jump/crouch using the vertical shoulder midpoint
4. **PyAutoGUI** sends keyboard inputs (`left`, `right`, `up`, `down`) to the OS.

## 🎮 Game Controls via Gestures

| Gesture            | Action         |
|--------------------|----------------|
| Hands joined       | Start Game     |
| Shoulders Left     | Move Left      |
| Shoulders Right    | Move Right     |
| Shoulders Center   | No Move        |
| Jump (Shoulders High) | Press `Up` |
| Crouch (Shoulders Low)| Press `Down` |

## 📷 Demo

> *Add a screen recording or GIF here to show it in action.*

## ⚙️ Requirements

- Python 3.7+
- OpenCV
- MediaPipe
- PyAutoGUI
- Matplotlib

Install them via pip:

```bash
pip install opencv-python mediapipe pyautogui matplotlib
