**# Real-Time Object Tracking in CARLA Simulator using YOLOv9 and DeepSORT**

## **Project Overview**
This project integrates **YOLOv9**, a cutting-edge object detection model, with **DeepSORT**, a real-time multi-object tracking algorithm, within the **CARLA Simulator**. Designed for autonomous driving research, this system detects and tracks multiple objects in dynamic environments, aiding perception and trajectory planning.

## **Key Features**
- **Real-time object detection and tracking** leveraging YOLOv9 and DeepSORT.
- **Seamless CARLA Simulator integration** for testing in realistic urban environments.
- **Optimized for autonomous vehicle applications**, enhancing perception and navigation.

## **Core Technologies**
- **YOLOv9** - Advanced deep learning-based object detection.
- **DeepSORT** - Multi-object tracking with association techniques.
- **CARLA Simulator** - Open-source platform for autonomous driving simulations.
- **OpenCV** - Image processing utilities.
- **PyTorch** - Deep learning framework for model implementation.
- **NumPy** - Efficient numerical computations.


https://github.com/user-attachments/assets/9674d0a0-5c48-40ae-ac3c-88f51a141cef


---
## **Installation Guide**
### **Prerequisites**
- **Python 3.7 or higher**
- **CARLA Simulator (v0.9.11)**

### **Setup Steps**
#### **Step 1: Install CARLA Simulator**
1. Download **CARLA 0.9.11** from the official CARLA releases page.
2. Extract the archive and follow installation steps as per **CARLA’s official documentation**.
3. Navigate to the extracted directory:
   ```bash
   cd CARLA_0.9.11
   ```

#### **Step 2: Clone the Project Repository**
```bash
git clone https://github.com/Lokesh11868/Object-Detection
cd Object-Detection
```

#### **Step 3: Install Dependencies**
```bash
pip install -r requirements.txt
```

## **Usage Instructions**
### **Step 1: Setup Trajectory Planning in CARLA**
1. Copy the trajectory planning script:
   ```bash
   cp planning_trajectory.py CARLA_0.9.11/PythonAPI/examples/
   ```
2. Launch the CARLA Simulator:
   ```bash
   cd CARLA_0.9.11
   ./CarlaUE4.exe
   ./CarlaUE4 -dx11  # (For DirectX 11 mode)
   ```
3. Execute the trajectory planning script:
   ```bash
   cd CARLA_0.9.11/PythonAPI/examples
   python planning_trajectory.py
   ```

### **Step 2: Implement YOLOv9 & DeepSORT Object Tracking**
1. Clone the YOLOv9 repository:
   ```bash
   git clone https://github.com/WongKinYiu/yolov9.git
   cd yolov9
   ```
2. Copy the recorded video from CARLA into the YOLOv9 directory.
3. Add the tracking script to the YOLOv9 directory:
   ```bash
   cp detect_tracking.py yolov9/
   ```
4. Run the object tracking script:
   ```bash
   python detect_tracking.py --weights 'yolov9-c.pt' --source 'video.mp4' --device 'cpu'
   ```

## **Results and Analysis**
- **Generated output video** displaying detected and tracked objects.
- **Trajectory and position data** for further evaluation.
---

This project is a valuable tool for autonomous vehicle research, leveraging state-of-the-art detection and tracking algorithms in a realistic driving simulation environment. 🚗💡

