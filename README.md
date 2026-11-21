# Automated Industrial Assembly Monitoring System for Defect Detection

## 📌 Project Overview

The **Automated Industrial Assembly Monitoring System** is a machine vision-based project designed to identify missing and incorrectly placed components in assembled electronic boards.

Traditional industrial inspection relies heavily on manual checking, which can be time-consuming and prone to human errors. This project uses deep learning and object detection techniques to automate the inspection process.

The system uses the **YOLOv8 object detection model** to identify components on a Raspberry Pi motherboard and detect missing components through image analysis.

## 🎯 Objectives

- Automate the inspection of assembled electronic components.
- Detect missing or incorrectly positioned components.
- Reduce dependency on manual inspection.
- Identify components using YOLOv8 object detection.
- Generate visual outputs highlighting detected and missing components.
- Improve consistency and efficiency in quality inspection.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| YOLOv8 | Object detection |
| OpenCV | Image processing |
| Pandas | Data handling |
| NumPy | Numerical operations |
| YAML | Dataset configuration |
| Google Colab | Model development and training |
| Raspberry Pi 4 Model B | Target hardware represented in the project |

## ⚙️ Project Workflow

The project follows these major stages:

1. **Dataset Collection:** Images of Raspberry Pi motherboards containing normal and defective assembly conditions are collected.

2. **Data Annotation:** Components are labelled using bounding boxes and annotations are prepared in YOLO format.

3. **Image Preprocessing:** Images are resized to 320 × 320 pixels, noise reduction is applied, and pixel values are normalized.

4. **Model Training:** The YOLOv8n model is trained using the prepared dataset with transfer learning.

5. **Object Detection:** The trained model identifies components and generates bounding boxes, class labels, and confidence scores.

6. **Missing Component Identification:** Detected components are compared against the expected component list and their predefined positions.

7. **Result Visualization:** Present components are highlighted using green bounding boxes, while missing components are highlighted using red bounding boxes.

8. **Output Generation:** The system displays an annotated image and prints detected and missing component information in the console.

## 🔍 Implementation Modules

### 1. Prototype Shape Detection

A prototype was initially developed using six geometric shapes:

- Circle
- Square
- Triangle
- Rectangle
- Pentagon
- Hexagon

This phase was used to validate the object detection and missing-object identification workflow.

### 2. Raspberry Pi Component Detection

The second phase applies the detection approach to Raspberry Pi motherboard images.

The system identifies ten key component categories, including:

- USB Ports
- Ethernet Port
- HDMI Ports
- GPIO Header
- Main Chip
- RAM Chip

The detected components are checked against the expected component layout to identify missing parts.

### 3. Defect Detection and Visualization

The system analyses the detection results and identifies missing components.

- **Green Bounding Box:** Component detected successfully.
- **Red Bounding Box:** Expected component is missing.

The final output includes an annotated image and a console report.

## 📊 Model Performance

The trained YOLOv8 model achieved the following evaluation results, as reported in the project report:

| Evaluation Metric | Result |
|---|---:|
| mAP@50 | 95.2% |
| mAP@50–95 | 92.6% |
| Training Epochs | 20 |
| Batch Size | 16 |
| Input Image Size | 320 × 320 |

## 🧪 Testing

The system was evaluated using multiple test scenarios, including:

- Normal component detection.
- Missing component detection.
- Multiple missing components.
- Component position verification.
- Low-confidence detection cases.
- Annotated image generation.
- Console output verification.

The project report records seven successful end-to-end test cases.

## ⚠️ Current Limitations

- The current implementation processes static images.
- Detection performance can be affected by changes in lighting and image quality.
- Similar-looking components may occasionally produce false detections.
- Live camera and conveyor belt integration have not yet been implemented.
- Real-time inference latency has not been formally benchmarked.

## 🚀 Future Enhancements

- Integrate a live camera feed for continuous inspection.
- Implement real-time defect detection.
- Integrate the system with industrial conveyor belts.
- Generate automatic alerts for defective assemblies.
- Improve model performance using larger and more diverse datasets.
- Explore deployment on edge devices.

## 👩‍💻 Project Contributors

- Madhumitha S
- Sivagami G

**Project Guide:** Mr. Damodaram Jeevan Kumar  
Assistant Professor, Department of Computer Science and Engineering

**Institution:** Sri Chandrasekharendra Saraswathi Viswa Mahavidyalaya (SCSVMV)

**Project Type:** Creative and Innovative Project (CIP) – 2026

---

## 📄 Project Documentation

The project report contains detailed information about the literature survey, system architecture, implementation, testing methodology, experimental graphs, and results.

