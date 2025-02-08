# Albanian Sign Language Detection with Azure Custom Vision
*A hands-on guide for creating a hand sign detection for the Albanian language using Azure CustomVision*

---

## Overview
This repository documents the steps for training an **Albanian Sign Language detection model** using Azure Custom Vision. The process includes: 
1. Upload hand sign images to Azure Custom Vision.
2. Annotate signs with labels.
3. Train and evaluate a model.
4. Export the model for future use.

**Target Audience**: Students that would like to learn to create AI projects with CustomVision. 

---

## Prerequisites
- An **Azure account** (free trial: https://azure.microsoft.com/free/).
- Basic familiarity with **Azure services**, mainly to create a CognitiveServices resource within a Resource Group. 
- **Images** of Albanian hand signs (e.g., letters, numbers, words).



---

## Step-by-Step Guide

### 1. Create a Custom Vision Project
1. Go to [Azure Custom Vision](https://www.customvision.ai/).
2. Sign in with your Azure account.
3. Click **New Project**:
   - **Name**: `Albanian-Sign-Language-Detection`
   - **Description**:`Custom Vision project for Albanian sign language detection.`
   - **Resource**: Select an existing Azure resource or create a new one (see Prerequisits).
   - **Project Type**: `Object Detection` .
   - **Domains**: `General` or `General (compact)` for easy export.
   - Click **Create Project**.

![Create project screenshot](/docs/images/create-project.png)


---

### 2. Upload images
1. Click **Add Images** and upload your 20 Albanian sign images.

![Upload images screenshot](/docs/images/upload.png)

### 3. Annotate images
1. **Annotate each image**: Draw bounding boxes around the hand in each image and assign labels (e.g., "A", "B", "1", "2").

![Annotation screenshot](/docs/images/annotate.png)

---

### 3. Train the Model
1. Click **Train** at the top of the page.
2. Select **Quick Training** (fast but less accurate) or **Advanced Training** (requires more time/data).
3. Wait for training to complete. Review the performance metrics (precision, recall).

![Train modell screenshot](/docs/images/train-modell.png)

![Review performance screenshot](/docs/images/modell-performance.png)
---

### 4. Evaluate and Test
1. Use the **Performance** tab to see precision/recall scores.
2. Test the model with the **Quick Test** feature:
   - Upload a new image to see if the model predicts the correct sign.

![Quick test screenshot](/docs/images/test.png)

---

### 5. Export the Model
1. Go to the **Performance** tab.
2. Click **Export** and choose a format:
   - **TensorFlow** (for Android/iOS apps)
   - **ONNX** (for Windows apps)
   - **Dockerfile** (for containers)
3. Save the exported model files for future use.

![Export model screenshot](/docs/images/export.png)

---

## Best Practices
- **Data Quality**: Ensure images are well-lit and show hands from multiple angles.
- **Labels**: Use consistent naming (e.g., "Letter_A", "Number_1").
- **Iterate**: Retrain the model with more data if performance is low.

---

## Troubleshooting
- **Poor Model Performance**: Add more images or adjust annotations.
- **Export Errors**: Ensure you selected the `General (compact)` domain during project creation.
- **Tagging Issues**: Double-check labels for typos.

---

## Contributors
- [Halil Radogoshi](https://github.com/halilradogoshi)


---

## License
This project is licensed under [MIT License](LICENSE).
