# YOLO26 Pose Estimation with White COCO Skeleton

A computer vision project that uses **YOLO26s-Pose**, OpenCV, and Python to detect human body keypoints in a video and visualize the COCO skeleton using white lines and keypoints on a black background.

## Features

- Human pose estimation using YOLO26s-Pose.
- Detection of 17 COCO body keypoints.
- White skeleton lines and white keypoints.
- Black background for clear visualization.
- Processes input videos frame by frame.
- Exports the annotated video in MP4 format.
- Supports multiple people in a frame.

## Demo

**Output Video:** https://drive.google.com/drive/folders/1f8Aab5QH4POkAFyXk0DJlODuMZ1qafiK?usp=sharing

## Technologies Used

- Python
- Ultralytics YOLO26
- OpenCV
- NumPy
- COCO Keypoint Format

## Installation

Install the required dependencies:

```bash
pip install ultralytics opencv-python numpy
```

## Model

The project uses the pretrained YOLO26 small pose model:

```python
from ultralytics import YOLO

model = YOLO("yolo26s-pose.pt")
```

The model weights are downloaded automatically when needed.

## How It Works

1. Load the input video using OpenCV.
2. Read each video frame.
3. Detect human body keypoints using YOLO26s-Pose.
4. Extract the 17 COCO keypoints for each detected person.
5. Connect the keypoints using the COCO skeleton structure.
6. Draw white lines and white keypoints on a black background.
7. Save the processed frames into an MP4 video.

## Configuration

Update the video paths according to your environment:

```python
video_path = "/content/input_data.mp4"
output_path = "/content/output_pose.mp4"
```

The paths above are intended for Google Colab. For local execution, use paths to files on your computer.

## Output

The generated video contains:

- A solid black background.
- White skeletal connections.
- White circular keypoints.
- No original video background or bounding boxes.

The exported video is saved as `output_pose.mp4`.

## Applications

- Human pose analysis
- Sports movement visualization
- Fitness and exercise analysis
- Computer vision experimentation
- Human motion tracking research

## Future Improvements

- Real-time pose estimation.
- Joint-angle calculation.
- Exercise repetition counting.
- Pose-based activity recognition.
- Motion analysis and tracking across frames.

## License

This project uses the Ultralytics YOLO framework. Review the [Ultralytics licensing information](https://www.ultralytics.com/license) before distributing or using it commercially.
