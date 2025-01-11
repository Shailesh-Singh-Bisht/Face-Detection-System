# Face Detection System

A YOLOv8-based AI solution for detecting faces in real-time. This system is designed for applications like monitoring, video processing, and facial data analysis.

## Features
- Real-time detection of faces in images and videos.
- Dataset augmentation for diverse scenarios, ensuring robust performance.
- Scalable design for integration into larger systems.

## Setup Instructions
1. **Open the Notebook**: Download and open the notebook on Google Colab.
2. **Connect to GPU Runtime**: Ensure GPU runtime is enabled in Google Colab for faster performance.
3. **Upload Input Files**:
   - Go to the file section in Colab and upload a video or image you want to test the model on.
   - Move the uploaded file to the `/content/ManualTestingData` folder.
4. **Update Prediction Command**:
   - Modify the following code snippet in the notebook:
     ```python
     weightsPath="/content/FaceDetection/runs/detect/train/weights"
     !yolo task=detect mode=predict model={weightsPath}/best.pt conf=.25 source='/content/ManualTestingData/InputVideo.mp4' save=True
     ```
   - Replace `InputVideo.mp4` with the name of your uploaded video or image.
5. **Run Predictions**:
   - Execute the code to generate predictions on your test files.
6. **Download Output**:
   - Use the final code cell in the notebook to download the annotated video.

## Technologies Used
- Python
- YOLOv8
- Roboflow
- OpenCV
- Google Colab

## Results
- Example detections are saved as videos with annotated bounding boxes.
- Performance metrics (e.g., confusion matrix and results.csv) are generated after training.

## Tested Video Result
View an example of the tested video output here:  
[Download Tested Video](https://drive.google.com/file/d/152Bky8uulnQoTyM-FHJC4kMDZ6ARdlsn/view?usp=sharing)

## Requirements
- **Google Colab**: GPU-enabled runtime for training and testing.
- **Dataset**: Use Roboflow or upload a pre-labeled face detection dataset.
- **YOLOv8 Framework**: For training and predictions.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgments
- [YOLOv8](https://ultralytics.com/yolov8)
- [Roboflow](https://roboflow.com/)
- Google Colab
