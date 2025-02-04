# Albanian Sign Language Detection with Azure Custom Vision
*A hands-on guide for creating a sign language detection model using Azure Custom Vision.*

---

## Overview
This repository documents the steps for training an **Albanian Sign Language detection model** using Azure Custom Vision. Students will learn to:
1. Upload hand sign images to Azure Custom Vision.
2. Annotate signs with labels.
3. Train and evaluate a model.
4. Export the model for future use.

**Target Audience**: Students participating in the Gjakova Makeathon.

---

## Prerequisites
- An **Azure account** (free trial: https://azure.microsoft.com/free/).
- **20 images** of Albanian hand signs (e.g., letters, numbers).
  - Example: Use photos of participants’ hands or open-source sign language datasets.
- Basic familiarity with Azure services.

---

## Step-by-Step Guide

### 1. Create a Custom Vision Project
1. Go to [Azure Custom Vision](https://www.customvision.ai/).
2. Sign in with your Azure account.
3. Click **New Project**:
   - **Name**: `Albanian-Signs`
   - **Resource**: Select an existing Azure resource or create a new one.
   - **Project Type**: `Object Detection` .
   - **Domains**: `General` or `General (compact)` for easy export.
   - Click **Create Project**.

![Create Project Screenshot](/docs/images/create-project.png)


---

### 2. Upload and Annotate Images
1. Click **Add Images** and upload your 20 Albanian sign images.
2. **Annotate each image**:
   - For object detection: Draw bounding boxes around the hand in each image and assign labels (e.g., "A", "B", "1", "2").


![Annotation Screenshot](/docs/images/annotate.png)

---

### 3. Train the Model
1. Click **Train** at the top of the page.
2. Select **Quick Training** (fast but less accurate) or **Advanced Training** (requires more time/data).
3. Wait for training to complete. Review the performance metrics (precision, recall).

---

### 4. Evaluate and Test
1. Use the **Performance** tab to see precision/recall scores.
2. Test the model with the **Quick Test** feature:
   - Upload a new image to see if the model predicts the correct sign.

![Quick Test Screenshot](/docs/images/test.png)

---

### 5. Export the Model
1. Go to the **Performance** tab.
2. Click **Export** and choose a format:
   - **TensorFlow** (for Android/iOS apps)
   - **ONNX** (for Windows apps)
   - **Dockerfile** (for containers)
3. Save the exported model files for future use.

![Export Model Screenshot](/docs/images/export.png)

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
