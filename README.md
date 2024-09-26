# Object Detection in Adverse Conditions: Developing a Robust System for Low Light, Rain, and Fog

This project focuses on real-time object detection in adverse weather conditions (e.g., foggy environments) using **YOLOv5** and **OpenCV**. The goal is to detect and track objects efficiently even when visibility is low.

## 🎯 Features

- Real-time object detection using a pre-trained YOLOv5 model.
- Customizable window resizing for better visualization.
- Handles video inputs with dynamic updating and rendering.

## 🛠️ Technologies Used

- [Python](https://www.python.org/)
- [OpenCV](https://opencv.org/)
- [PyTorch](https://pytorch.org/)
- [YOLOv5](https://github.com/ultralytics/yolov5)

## 📋 Requirements

- Python 3.x
- OpenCV
- PyTorch
- YOLOv5 (loaded via Torch Hub)

## ⚡ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo.git
   ```
2. Install the required packages:
   ```bash
   pip install opencv-python torch
   ```

## 🚀 Usage

1. Place your video file (e.g., `foggy_video.mp4`) in the project directory.
2. Run the script:
   ```bash
   python object_detection.py
   ```
3. Press `q` to exit the real-time object detection window.

## 🔑 Key Code Snippets

### Initializing YOLOv5 Model
```python
import torch

model = torch.hub.load('ultralytics/yolov5', 'yolov5s', pretrained=True)
```

### Reading Video and Processing Frames
```python
cap = cv2.VideoCapture('foggy_video.mp4')

while True:
    ret, frame = cap.read()
    if not ret:
        break
    # Object detection code here
```

### Displaying Results
```python
cv2.imshow('Real-time Object Detection', img_bgr)
```

## 📂 Directory Structure

```
/your-repo
│
├── foggy_video.mp4         # Video file for testing
├── object_detection.py     # Main script
└── README.md               # Project documentation
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](../../issues/).

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

