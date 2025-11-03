# YOLOv8 Footfall Detection and Tracking

This project demonstrates a computer vision pipeline for footfall detection — counting and tracking people in video frames using YOLOv8 (by Ultralytics).
It builds upon state-of-the-art object detection and tracking techniques to identify individuals, assign unique IDs, and maintain their identity across frames — enabling applications in retail analytics, crowd monitoring, and smart surveillance.

# 🚀 Features
* Real-time object detection using YOLOv8.

* Person tracking via model.track() from Ultralytics.

* Frame-by-frame identity preservation for accurate footfall counting.

* Support for COCO dataset (person class).

* Visualized detections and confusion matrix for performance evaluation.

# 📂 Project Structure

| Section                                   | Description                                                                            |
| ----------------------------------------- | -------------------------------------------------------------------------------------- |
| **0. Dependencies and Environment Setup** | Installs and imports all necessary Python packages (Ultralytics, Torch, OpenCV, etc.). |
| **1. Dataset Download**                   | Downloads the COCO 2017 dataset (person class only).                                   |
| **2. Model Creation**                     | Initializes YOLOv8 model using Ultralytics API.                                        |
| **3. Predictions and Evaluation**         | Runs inference on test images and visualizes detections, performance on validation data.|                               |
| **4. Tracking on Video**                  | Performs multi-object tracking on sample video input using `model.track()`.            |
                                     

# 🧠 Technical Overview
Under the hood:
* The YOLO model detects objects and assigns bounding boxes with confidence scores.

* The tracking module links detections across frames based on motion prediction and appearance embeddings.

* Even if objects disappear temporarily or overlap, the tracker maintains consistent identities.

This approach is particularly useful for footfall estimation — counting unique individuals who enter or exit a monitored zone.

# 🧾 Acknowledgements

* Project inspired by: [insomnius/person-detection](https://github.com/insomnius/person-detection/tree/master)

* Based on Ultralytics [YOLOv8 Documentation](https://docs.ultralytics.com/modes/train/)
