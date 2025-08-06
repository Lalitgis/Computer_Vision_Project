````markdown
# 🌍 GeoAI & Computer Vision Project

This repository contains a collection of GeoAI and computer vision experiments focused on two core tasks:

- **🏙️ Building Detection** — Identifying and segmenting built structures from satellite or aerial imagery for applications in urban mapping, planning, and disaster management.
- **🌱 Weed Detection** — Detecting invasive plant species in agricultural fields using drone/UAV imagery to enable targeted weeding and precision agriculture.

Both tasks utilize deep learning, geospatial data, and image processing techniques integrated within a reproducible workflow.

---

## 🔍 Project Objectives

### 1. Building Detection
- Detect buildings in remote and urban areas.
- Compare model performance across different geographies.
- Evaluate the use of various satellite and drone imagery resolutions.
- Output: Shapefiles/raster masks for integration into GIS software (e.g., QGIS, ArcGIS).

### 2. Weed Detection
- Segment weeds from crops in drone imagery.
- Enable field-specific weed coverage estimation.
- Integrate detection with variable-rate application maps for automated precision spraying.

---

## 🧠 Models & Tools

| Task              | Model Used         | Framework     | Notes |
|-------------------|--------------------|----------------|-------|
| Building Detection| U-Net, YOLOv8       | PyTorch, Ultralytics | Fine-tuned on public datasets and custom-labeled imagery |
| Weed Detection    | DeepLabv3+, YOLOv5  | PyTorch, OpenCV | Trained on multispectral UAV imagery |

---

## 🗃️ Datasets

- **Building Detection:**
  - [SpaceNet](https://spacenet.ai)
  - Custom-labeled imagery from DJI drones
  - Google Earth snapshots (aligned via QGIS)

- **Weed Detection:**
  - UAV images captured from experimental plots
  - Labels created using Labelme and Roboflow
  - NDVI/NDRE layers used in multispectral analysis

---

## 🛠️ Installation

```bash
# Clone the repo
git clone https://github.com/your-username/geoai-computer-vision.git
cd geoai-computer-vision

# Create environment (recommended)
conda create -n geoai python=3.10
conda activate geoai

# Install dependencies
pip install -r requirements.txt
````

---

## 🚀 How to Use

### Building Detection

```bash
python detect_buildings.py --img data/test_image.jpg --weights models/building_yolov8.pt
```

### Weed Detection

```bash
python detect_weeds.py --folder data/uav_images --weights models/weed_yolov5.pt
```

Results will be saved in the `outputs/` directory with shapefiles and annotated overlays.

---

## 🧪 Evaluation Metrics

* **IoU (Intersection over Union)**
* **F1 Score**
* **Precision & Recall**
* **mAP\@0.5** for YOLO models

---

## 🗺️ Integration with GIS

* All outputs can be exported as:

  * `.tif` raster masks
  * `.shp` shapefiles for vector use
* Compatible with **QGIS**, **ArcGIS**, and **Google Earth Engine**

---

## 🧑‍💻 Author

**Lalit BC**
Data Analyst & GIS Expert
🌐 [LinkedIn](https://www.linkedin.com/in/lalitbc) | 🛰️ Co-founder at Map Mentors | ✉️ [lalitbc@example.com](mailto:lalitbc@example.com)

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## 🙌 Acknowledgements

* [SpaceNet](https://spacenet.ai/)
* [Roboflow](https://roboflow.com/)
* [Labelme](https://github.com/wkentaro/labelme)
* [Ultralytics YOLO](https://github.com/ultralytics/yolov5)

```
