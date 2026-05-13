# 🚗 Smart Car Parking Detection System

An **AI-powered Smart Parking Management System** built with **YOLOv8** and **Gradio**, capable of detecting available and occupied parking spaces from images and videos — with intelligent recommendations based on distance from entrance.

---

## 🎯 Features

- 🔍 **Real-time Parking Space Detection** using YOLOv8 custom trained model
- 🖼️ **Image & Video Support** — upload any parking lot photo or video
- 📍 **Click-to-Set Entrance** — user defines entrance location on the image
- 📏 **Distance-Based Recommendations** — suggests nearest available spot to entrance
- 🗺️ **Visual Parking Map** — color-coded layout (green = free, red = occupied)
- 🤖 **DBSCAN Clustering** — groups nearby detections for accurate space mapping
- 🌐 **Gradio Web Interface** — clean, interactive browser-based UI

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **YOLOv8 (Ultralytics)** | Parking space object detection |
| **Gradio** | Web-based interactive UI |
| **OpenCV** | Image & video processing |
| **DBSCAN (Scikit-learn)** | Spatial clustering of detections |
| **Matplotlib** | Visual parking map generation |
| **Google Colab** | Training & deployment environment |

---

## 📁 Project Structure

```
Car-Parking-Detection-YOLO/
├── car_parking_system.ipynb   # Main notebook (full implementation)
├── best.pt                    # YOLOv8 trained weights (not included - see below)
└── README.md                  # Project documentation
```

---

## ⚙️ How to Run

### 1. Clone the repo
```bash
git clone https://github.com/your-username/Car-Parking-Detection-YOLO.git
```

### 2. Install dependencies
```bash
pip install gradio ultralytics opencv-python scipy scikit-learn matplotlib
```

### 3. Add your trained model
Place your `best.pt` (YOLOv8 weights) in the project directory and update the path:
```python
model_path = 'best.pt'
```

### 4. Run the notebook
Open in **Google Colab** or **Jupyter Notebook** and run all cells.

### 5. Access the UI
A **Gradio link** will be generated — open it in your browser to use the system.

---

## 🧠 How It Works

1. **Upload** a parking lot image or video
2. **Click** on the image to mark the entrance location
3. **YOLOv8** detects all parking spaces and classifies them as free or occupied
4. **DBSCAN clustering** removes duplicate detections
5. System **recommends the nearest free spot** to the entrance
6. A **visual parking map** is generated showing the full layout

---

## 📌 Note on Model Weights

The trained model file (`best.pt`) is **not included** in this repository due to file size limits. You can:
- Train your own YOLOv8 model on a parking dataset (e.g., PKLot dataset)
- Or contact the author for the weights file

---

## 👨‍💻 Author

**Abdullah**  
BS Artificial Intelligence — University of Management and Technology (UMT)
