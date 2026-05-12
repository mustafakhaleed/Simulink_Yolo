# YOLOv8 Object Detection Pipeline in Simulink

This repository features a high-level engineering implementation of a **YOLOv8** deep learning model integrated directly into **Simulink** using the **ONNX** framework. The project demonstrates a complete end-to-end computer vision pipeline, from raw camera input to real-time object classification and grading.

## 🚀 System Architecture
The model is structured into a streamlined four-stage pipeline as shown in the block diagram:

1.  **Image Pre-processing:**
    * **Rapoo Camera MJPG:** Captures live video at 640x480 resolution.
    * **LetterBox Block:** Resizes and pads images to maintain aspect ratio for the neural network.
2.  **Deep Learning Inference:**
    * **ONNX Model Predict:** Executes the YOLOv8 model via the Open Neural Network Exchange (ONNX) format for cross-platform compatibility.
3.  **Post-processing (YoloPost):**
    * Decodes raw model outputs into **Bounding Boxes**, **Confidence Scores**, and **Class IDs**.
    * Rescales coordinates back to the original image dimensions.
4.  **Output & Logic:**
    * **Visualization:** Overlays detection results on the live video feed.
    * **Grading Logic:** Categorizes detected objects into specific industrial grades (e.g., Grade_1, Grade_2, Agwa) based on class and confidence.

## 🛠️ Key Features
* **Real-time Deployment:** Optimized for live inference within the MATLAB/Simulink environment.
* **Industrial Application:** Designed for automated quality control and sorting lines.
* **Framework Agnostic:** Uses ONNX to leverage high-performance models without requiring native training environments.

## 📂 Repository Contents
* `NewModelSimFor5Grades.slx`: The primary Simulink model file.
* `Sample_Result.png`: A demonstration of the detection output.
* `LICENSE`: MIT License information.

## 🏁 Quick Start
1. **Clone the repo:**
   ```bash
   git clone [https://github.com/mustafakhaleed/Simulink_Yolo.git](https://github.com/mustafakhaleed/Simulink_Yolo.git)
