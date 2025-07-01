📄 Player Re-Identification Report
🔍 Objective

To identify and track football players across video frames using object detection (YOLOv8) and object tracking (DeepSORT). The goal was to maintain consistent IDs for players even when they leave and re-enter the frame.
🎯 Final Result

    train and tested using YOLOv8 + DeepSORT.

    imported the video to roboflow and selected 5frame per second so 76frames,next manually annotated each and added more by some resize, blur and augmentation.

    exported 178 manually annotated and augmented images from Roboflow.

    Three different output videos included:

        output_videoyolov8x.mp4

        output_with_5frame_per_sec.mp4

        output_with_extra_augmented_data_and_deepsort.mp4

🧠 Approach & Methodology

    Data Preparation

        Extracted frames from video at 5 fps.

        Annotated using Roboflow (classes: players, goal_keeper, ball, refree).

        Augmented using Roboflow tools.

        Split into train/valid/test sets costumized(153,15,10).

    Model Training

        Trained custom YOLOv8n model on CPU (Intel i5, 8GB RAM).

        20 epochs used to balance training time and performance.

    Player Re-Identification

        Used DeepSORT for multi-object tracking.

        Assigned somewhat consistent IDs to players across frames.

        Integrated YOLOv8 detections as inputs to DeepSORT.

⚙️ Files Included
File / Folder	Description
first_approach.ipynb	YOLOv8x-based object detection
training_and_testing.ipynb	Final custom-trained model + DeepSORT integration
runs/	YOLOv8 training outputs
input_video/	Source video used for training/test
output_*.mp4	Final prediction videos
requirements.txt	Dependencies
biswajit_ml_resume.pdf	My updated resume
🧪 Techniques Tried

    Compared different YOLO versions (yolov8n, yolov8x)

    Used Roboflow augmentation: Resize, Crop, Flip

    Fine-tuned confidence threshold and NMS

    Attempted ball and goalkeeper detection (with partial success)

🧱 Challenges Faced

    Limited RAM/CPU made training slow (no GPU)

    Difficult to track ball and goalkeeper due to small sample size


✅  Next Steps (if more time)

    Improve class balance and annotate more ball samples

    try using better model like yolov8x for training