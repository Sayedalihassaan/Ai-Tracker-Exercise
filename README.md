
# Ai-Tracker-Exercise

This project uses computer vision techniques to track and count push-ups in a video, detect and track people using YOLOv8, and provides real-time feedback with an alarm system. It combines Mediapipe for pose estimation with YOLOv8 for object detection and tracking.

## Features

- **Push-up Counting**: Counts push-ups based on the angle of the arms using Mediapipe's pose estimation.
- **Person Tracking**: Uses YOLOv8 to detect and track people in the video.
- **Real-time Feedback**: Plays an alarm sound when a push-up is detected.
- **Visual Feedback**: Displays detected angles, push-up count, and person tracking IDs on the video feed.

## Requirements

- Python 3.8 or higher
- OpenCV
- Mediapipe
- YOLOv8 (Ultralytics)
- NumPy
- CVZone
- playsound

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/Ai-Tracker-Exercise.git
   cd Ai-Tracker-Exercise
   ```

2. **Install the required packages:**

   ```bash
   pip install opencv-python mediapipe ultralytics numpy cvzone playsound
   ```

3. **Download YOLOv8 model weights:**

   Make sure to download the `yolov8s.pt` weights and place them in the project directory. You can find the weights [here](https://github.com/ultralytics/yolov5/releases).

4. **Prepare your data:**

   - Place your video file (`pushup.mp4`) in the project directory.
   - Make sure the `coco.txt` file with class names is also in the project directory.

5. **Set up the alarm sound:**

   Ensure you have an alarm sound file (`assets_alarm.mp3`) in the project directory or modify the path to an existing sound file.

## Usage

Run the script with:

```bash
python ai_tracker_exercise.py
```

The video window will display the push-up counter, state, and person tracking IDs. Press 'q' to quit the application.

## Code Overview

- **`ai_tracker_exercise.py`**: Main script for tracking push-ups and people. It handles video capture, pose estimation, angle calculation, person detection, tracking, and alarm triggering.
- **`tracker.py`**: Contains the implementation for the `Tracker` class used for person tracking.

## Contributing

Feel free to open issues or submit pull requests to improve the project. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
