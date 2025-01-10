# **IoT-Based Traffic Management System 🚦**

## **Overview 🌐**

This project implements an **IoT-based Traffic Management System** that utilizes **ESP32-CAM modules** and **ultrasonic sensors** to dynamically adjust traffic light timings. The system optimizes traffic flow, reduces congestion, and improves safety by making real-time decisions based on the data gathered.

---

## **System Components 🛠️**

- **ESP32-CAM**: Captures real-time traffic images and transmits them to a server over WiFi for further processing.
- **Ultrasonic Sensors**: Measures the distance between vehicles to assess traffic density and flow.
- **ESP32-CAM-MB Programmer**: Programs the ESP32-CAM modules for efficient data collection.

---

## **How It Works 🔄**

### **1. Data Collection 📡**

- **Ultrasonic Sensors** continuously measure the distance between vehicles, generating real-time data.
- **ESP32-CAM Modules** capture images of traffic at regular intervals.
- The data is sent to the server every **30 seconds** via **WiFi** for further processing.

### **2. Data Processing 💻**

- The **Server** processes vehicle distance data to determine traffic density.
- **OpenCV** is used to analyze images captured by the **ESP32-CAM** to count the number of vehicles.

### **3. Traffic Analysis 📊**

- **Sensor data** and **image processing results** are combined to assess traffic congestion.
- Traffic light timings are dynamically adjusted based on **vehicle count** and **density**:
  - **Red**: High density or many vehicles.
  - **Orange**: Moderate density or vehicle count.
  - **Green**: Low density and fewer vehicles.

### **4. Web Interface 🌍**

- Displays real-time traffic data, including **live images** from the **ESP32-CAM**.
- Provides an interface to review **historical traffic data** for analysis and future improvements.

![Dashboard](https://github.com/TheodosiosKatis/Intelligent-Traffic-Management-System/assets/91337898/3d4970e4-996d-4158-b069-6cc576556a07)

---

## **Benefits 💡**

- **Optimized Traffic Flow**: Real-time adjustments to traffic lights reduce congestion and ensure smooth traffic movement.
- **Reduced Emissions 🌱**: By minimizing idle times, the system lowers fuel consumption and reduces pollution.
- **Enhanced Safety 🛡️**: The dynamic control system reduces the likelihood of accidents, improving overall road safety.
- **Better User Experience 👥**: Provides real-time traffic information, enabling informed decision-making for commuters.

---

## **Required Packages for OpenCV Algorithm 📦**

To run the system, the following packages are required for the **OpenCV** algorithm:

- [COCO Names File](https://github.com/pjreddie/darknet/blob/master/data/coco.names)
- [YOLOv3 Weights File](https://github.com/patrick013/Object-Detection---Yolov3/blob/master/model/yolov3.weights)
- [YOLOv3 Configuration File](https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg)

---

## **Technologies Used ⚙️**

- **IoT**: Real-time communication between devices using WiFi (ESP32-CAM).
- **Computer Vision**: Image processing and object detection using OpenCV and YOLOv3.
- **Embedded Systems**: Integration of hardware (ESP32-CAM, ultrasonic sensors) for real-time data capture.
- **Web Development**: Real-time dashboard displaying traffic data.
