# Scene Understanding Project

A comprehensive computer vision pipeline for advanced scene understanding, including 3D object detection, depth estimation, lane detection, and human pose estimation.

## 🎯 Overview

This project combines multiple state-of-the-art computer vision models to provide a complete scene understanding solution:

- **3D Object Detection**: YOLOv11 with 3D bounding box estimation
- **Depth Estimation**: Depth Anything v2 for monocular depth prediction
- **Lane Detection**: Computer vision-based lane detection for autonomous driving
- **Human Pose Estimation**: VIBE (Video Inference for Human Body Pose and Shape Estimation)

## Project Structure

```
SceneUnderstanding/
├── run.py                 # Main 3D object detection pipeline
├── demo.py               # VIBE human pose estimation demo
├── lane.py               # Lane detection implementation
├── detection_model.py    # YOLOv11 object detection wrapper
├── depth_model.py        # Depth Anything v2 wrapper
├── bbox3d_utils.py       # 3D bounding box estimation utilities
├── models.py             # SMPL models and neural network architectures
├── img_utils.py          # Image processing and transformation utilities
├── utils.py              # General utility functions
├── requirements.txt      # Python dependencies
├── run.sh                # Setup and execution script
└── vehicle_icons/        # Icons for vehicle visualization
    ├── bus_icon.png
    ├── car_icon.png
    └── truck_icon.png
```

### Prerequisites
- Python 3.8+
- CUDA-capable GPU (optional, but recommended)
- FFmpeg (for video processing)

### Setup
1. Clone the repository and navigate to the project directory
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the setup script:
   ```bash
   ./run.sh
   ```

### 3D Object Detection Pipeline
```bash
python run.py
```
This will:
1. Load the input video (`output_videos/Lane_Det.mp4`)
2. Perform object detection and tracking
3. Estimate depth for each detected object
4. Generate 3D bounding boxes
5. Create Bird's Eye View visualization
6. Save output video with 3D annotations