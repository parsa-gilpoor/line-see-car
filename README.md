
# Lane Detection Using OpenCV

This project implements a simple lane detection algorithm using OpenCV. The algorithm processes video frames to detect lane lines on the road by applying edge detection, a region of interest, and Hough Line Transformation.

## Features
- Reads video input.
- Applies edge detection using Canny Edge Detector.
- Detects lane lines using Hough Line Transformation.
- Averages multiple detected lines for more stable lane lines.
- Shows the detected lane lines overlaid on the original video.

## Requirements
- Python 3.x
- OpenCV
- NumPy

You can install the necessary libraries by running:
```bash
pip install opencv-python numpy
```

## How It Works

1. **Video Input**: The video is loaded using `cv2.VideoCapture()`.
2. **Preprocessing**:
    - The video frames are resized to make processing faster.
    - Frames are converted to grayscale.
    - Gaussian blur is applied to reduce noise.
3. **Edge Detection**: Canny Edge Detection is used to detect the edges in the frame.
4. **Region of Interest**: A triangular region where lane lines are expected is defined, and the rest of the image is masked out.
5. **Lane Detection**: The Hough Line Transformation detects lines in the image. Lines are divided into left and right lanes based on their slope.
6. **Drawing Lines**: Detected lines are averaged and drawn on the frame.

## How to Run

1. Place your video file in the project folder (replace `1232.mp4` with your video name).
2. Run the Python script.

```bash
python lane_detection.py
```

## Future Improvements
- Enhance lane detection in curved roads.
- Improve handling for different lighting conditions.
- Add lane departure warning feature.

## License
This project is open source and available under the [MIT License](LICENSE).
