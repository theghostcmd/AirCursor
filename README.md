# 🖐️ Hand Gesture Control System

A software-only virtual mouse that lets you control your PC using **real-time hand gestures through a webcam**. Built with **Python, OpenCV, and MediaPipe**.

> **Control your cursor. Click. Scroll. Interact — without a physical mouse.**

## ✨ Features

### 🖱️ Multi-Mode Interaction

* **MOVE MODE** — Control the cursor using your index finger.
* **SCROLL MODE** — Scroll pages using intuitive hand movement.
* **PAUSED MODE** — Safely suspend all cursor controls.

### 🤏 Gesture Controls

* **Left Click** — Thumb + Index Finger pinch.
* **Right Click** — Thumb + Middle Finger pinch.
* **Cursor Movement** — Raise the index finger and move your hand.
* **Scroll** — Raise Index + Middle fingers (Peace/Victory sign).
* **Pause** — Make a closed fist.
* **Quit** — Press `Q` to safely shut down the application.

### 🛡️ Safety Features

* **Global Kill Switch (`Q`)** — Immediately terminates the application.
* **Auto-Pause** — Pauses control when the hand is lost or FPS becomes too low.
* **Gesture Cooldowns** — Helps prevent accidental repeated clicks.
* **Closed-Fist Safety Mode** — Stops cursor interaction immediately.

### 📊 Visual Dashboard

Displays real-time:

* Current interaction mode
* FPS
* Detected gesture
* Hand tracking status
* Pause state

---

## 🛠️ Technologies

* **Python 3.8+**
* **OpenCV**
* **MediaPipe**
* **PyAutoGUI**
* Webcam-based real-time hand tracking

---

## 📋 Prerequisites

Before running the project, make sure you have:

* Python 3.8 or newer
* A working webcam
* Required Python dependencies
* MediaPipe `hand_landmarker.task` model

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/theghostcmd/AirCursor.git
cd AirCursor
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the MediaPipe Model

The application requires the `hand_landmarker.task` model.

Download it from the official MediaPipe model repository and place it in the project directory.

You can also download it using PowerShell:

```powershell
Invoke-WebRequest -Uri "https://storage.googleapis.com/mediapipe-models/hand_landmarker/hand_landmarker/float16/1/hand_landmarker.task" -OutFile "hand_landmarker.task"
```

### 4. Run the Application

```bash
python main.py
```

---

# ✋ Gesture Guide

## 1. 🖱️ Move Cursor

**Gesture:** Raise your **index finger only** while keeping the other fingers curled.

**Action:** The cursor follows the position of your index fingertip.

**Tip:** Keep your hand inside the webcam's field of view and move smoothly.

---

## 2. 👆 Left Click

**Gesture:** Pinch your **thumb and index finger** together.

**Action:** Performs a left mouse click.

**Requirement:** The fingers must remain within the configured pinch distance for approximately `0.25 seconds` to reduce accidental clicks.

---

## 3. 👉 Right Click

**Gesture:** Pinch your **thumb and middle finger** together.

**Action:** Performs a right mouse click and opens the context menu.

**Requirement:** The gesture must be held for approximately `0.25 seconds`.

---

## 4. ✌️ Scroll Mode

**Gesture:** Raise your **index and middle fingers**.

**Action:** Enters Scroll Mode.

* Move your hand **up** → Scroll up
* Move your hand **down** → Scroll down

**Exit:** Lower your middle finger to return to cursor control.

---

## 5. ✊ Pause / Safety Mode

**Gesture:** Make a **closed fist**.

**Action:** Immediately pauses mouse control.

The application displays the **PAUSED** state so you can safely reposition your hand.

---

## 6. ⌨️ Quit

Press:

```text
Q
```

**Action:** Safely shuts down the application.

---

# ⚙️ Configuration

Customize the system through `config.py`.

Available configuration options include:

```text
SCROLL_SPEED
GESTURE_COOLDOWN
SMOOTHING_FACTOR
```

### `SCROLL_SPEED`

Controls scrolling sensitivity.

### `GESTURE_COOLDOWN`

Controls the minimum time between gesture-triggered actions.

### `SMOOTHING_FACTOR`

Controls cursor stability and reduces unwanted movement caused by small hand-tracking variations.

---

# 🔮 Roadmap

### Version 3

Future improvements may include:

* 🎙️ **Voice Control**

  * Example: `"Computer, open browser"`

* ⌨️ **Air Keyboard**

  * Virtual keyboard input using hand gestures.

* 🖐️ **Custom Gestures**

  * Machine-learning-based personalized gesture recognition.

* 🎯 **Improved Cursor Calibration**

  * Better control across different screen resolutions.

* ⚡ **Performance Optimization**

  * Improved FPS and lower CPU usage.

---

# 👨‍💻 Author

**Mayank Jangra**

Python Developer & Creator of the Hand Gesture Control System.

GitHub: **[@theghostcmd](https://github.com/theghostcmd)**

This project was developed as a **portfolio and computer-vision demonstration project**, exploring real-time hand tracking and human-computer interaction.

---

# 📄 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

## ⭐ Support the Project

If you find this project useful or interesting:

* ⭐ Star the repository
* 🍴 Fork the project
* 🐛 Report bugs
* 💡 Suggest improvements
* 🔧 Contribute to future versions

---

**Built with Python • OpenCV • MediaPipe**

© 2026 **Mayank Jangra**. All rights reserved under the MIT License.
