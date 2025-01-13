# **Detect Corner Mark on Device and Image Quality**

## **Overview**
This project leverages Machine Learning to confirm whether an image captures the corner marks of a smartphone screen and evaluates the quality of the captured image. The purpose is to assess the quality of the smartphone screen as represented in the image. 

Initially, the project used object detection with OpenCV. However, to enable online usage and embed the model in an application, the approach was transitioned to object classification using TensorFlow Lite (TFLite). The TFLite model classifies images to identify:
- Whether all corners of the smartphone are visible.
- The quality of the captured image.

---

## **Table of Contents**
1. [Features](#features)  
2. [Technologies Used](#technologies-used)  
3. [Prerequisites](#prerequisites)  
4. [Installation](#installation)  
5. [Usage](#usage)  

---

## **Features**
- Machine Learning-based image classification.  
- Determines whether an image captures all corners of a smartphone screen.  
- Evaluates the quality of the captured image.  
- Lightweight TFLite model optimized for Android applications.  

---

## **Technologies Used**
- **Programming Languages**: Python, Java/Kotlin (for Android).  
- **Libraries/Frameworks**:  
  - OpenCV (for initial development).  
  - TensorFlow Lite (for model deployment).  

---

## **Prerequisites**
- Android Studio installed on your system.  
- Basic knowledge of Machine Learning and Android app development.  
- TensorFlow Lite interpreter for running the TFLite model in the Android app.  

---

## **Installation**
1. Clone the repository:  
   ```bash
   git clone https://github.com/hwangzie/Detect-Corner-Mark-on-Device-and-Image-Quality.git
   cd yourprojectname
   ```
2. Add the TFLite model to your project:  
   Place the `.tflite` file in the `assets` folder of your Android app.  
3. Update your app's dependencies to include the TensorFlow Lite runtime.  
   ```gradle
   implementation 'org.tensorflow:tensorflow-lite:2.x.x'
   ```
4. Build and run the app on an Android device.  

---

## **Usage**
1. Place the TFLite model in the `assets` folder of your Android app.  
2. Use the TensorFlow Lite interpreter to classify images and determine:  
   - Whether the image shows all four corners of the smartphone screen.  
   - The quality of the captured image.  
3. Example workflow:
   - Capture an image of the smartphone screen.
   - Process the image using the embedded TFLite model.
   - Display the classification result within the app.  
