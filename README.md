# Real-Time Motion Detection System 🚀

A lightweight Python application that detects moving objects in a live video stream using OpenCV. It utilizes Gaussian blurring and frame differencing to identify changes in the environment and highlights moving objects with bounding boxes.

## 🛠️ Features
- **Real-time Detection**: Processes live camera feed with minimal latency.
- **Dynamic Thresholding**: Uses Binary Thresholding and Dilation to reduce noise.
- **Contour Analysis**: Filters small movements (noise) by setting a minimum area threshold.
- **Visual Feedback**: Displays "Normal" or "Moving Object Detected" status directly on the video feed.

## 📸 How it Works
1. **Background Subtraction**: The first frame captured is used as a baseline.
2. **Preprocessing**: Frames are converted to grayscale and blurred to remove high-frequency noise.
3. **Absolute Difference**: The system calculates the difference between the baseline and the current frame.
4. **Contour Mapping**: If the difference exceeds a threshold, a bounding box is drawn around the movement.

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- A working webcam

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Motion-Detection-OpenCV.git](https://github.com/YOUR_USERNAME/Motion-Detection-OpenCV.git)
   cd Motion-Detection-OpenCV
2. Install dependencies:

Bash
pip install opencv-python imutils
Usage
Run the script:

Bash
python main.py
Press 'q' to exit the application.

📝 Configuration
You can adjust the sensitivity by modifying these variables in main.py:

area = 500: Increase this value to ignore smaller objects (like pets or moving curtains).

cv2.GaussianBlur(..., (21, 21), 0): Adjust the kernel size to change blurring intensity.

⚖️ License
Distributed under the MIT License. See LICENSE for more information.


---

## 📦 requirements.txt
Create this file so others can install your dependencies easily:
```text
opencv-python
imutils
