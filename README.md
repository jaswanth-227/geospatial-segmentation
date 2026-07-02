# 🛰️ Geospatial Feature Extraction using Multi-Model Deep Learning

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=28&duration=3500&pause=1000&color=2E9AFE&center=true&vCenter=true&width=900&lines=Geospatial+Feature+Extraction+using+Deep+Learning;Building+%7C+Road+%7C+Water+Segmentation;GIS-Ready+Vector+Generation;IIT+Tirupati+Hackathon+Project" />
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-red?style=for-the-badge&logo=pytorch)
![OpenCV](https://img.shields.io/badge/OpenCV-ComputerVision-green?style=for-the-badge&logo=opencv)
![GeoPandas](https://img.shields.io/badge/GeoPandas-GIS-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-orange?style=for-the-badge)

</p>

---

# 🌍 Overview

This project presents a **production-ready Geospatial AI pipeline** that automatically extracts **Buildings, Roads, Road Centerlines, and Water Bodies** from ultra-high-resolution satellite imagery.

Designed for the **IIT Tirupati Geospatial AI Hackathon**, the system efficiently processes **10K × 20K+ GeoTIFF images** using a memory-efficient tiled inference pipeline and exports predictions into **GIS-compatible vector layers (.gpkg)** for QGIS and ArcGIS.

---

# 🎯 Hackathon Objective

Develop an intelligent geospatial feature extraction framework capable of automating mapping tasks for:

- 🏙 Smart City Planning
- 🛣 Road Network Analysis
- 🌊 Water Resource Monitoring
- 🌍 Environmental Monitoring
- 🛰 Remote Sensing Applications
- 📍 GIS-based Spatial Intelligence

---

# ✨ Key Features

- 🛰 Supports ultra-high-resolution GeoTIFF images (10K × 20K+)
- 🧠 Multi-model Deep Learning architecture
- 🔲 Memory-efficient tiled inference
- 🛣 Automatic road centerline extraction
- 🌊 Water boundary refinement
- 🏢 Building footprint segmentation
- 🗺 Raster-to-Vector GIS conversion
- 📦 GeoPackage (.gpkg) export
- ⚡ Optimized stitching and reconstruction

---

# 🏗 System Architecture

```text
                  GeoTIFF Satellite Image
                           │
                           ▼
                 Tile Generation Engine
                           │
                           ▼
                 Multi-Model Router
     ┌─────────────┬────────────┬────────────┐
     │             │            │            │
Building Model  Road Model  Water Model  Centerline Model
     │             │            │            │
     └─────────────┴────────────┴────────────┘
                           │
                           ▼
                 Post Processing Layer
                           │
                           ▼
          Raster Outputs + GIS Vector Outputs
```

---

# 🧠 Deep Learning Models

| Feature | Model | Purpose |
|---------|--------|----------|
| 🏢 Buildings | UNet | Building Footprint Segmentation |
| 🛣 Roads | DINOv2 | Road Surface Extraction |
| 🌊 Water Bodies | DeepLabV3+ | Water Segmentation |
| 🌊 Water Boundaries | Refinement CNN | Boundary Enhancement |
| 🛣 Road Centerlines | Skeleton CNN | Centerline Extraction |

---

# 📊 Performance

| Task | IoU Score |
|------|-----------|
| 🏢 Building Segmentation | **81%** |
| 🛣 Road Segmentation | **79%** |
| 🌊 Water Segmentation | **82%** |
| 🌊 Water Boundary Extraction | **82%** |
| 🛣 Road Centerline Extraction | **64%** |

---

# ⚙ Workflow

```text
GeoTIFF Image
      │
      ▼
Tile Generation
      │
      ▼
Model Selection
      │
      ▼
Deep Learning Inference
      │
      ▼
Prediction Stitching
      │
      ▼
Morphological Processing
      │
      ▼
Skeletonization
      │
      ▼
Raster-to-Vector Conversion
      │
      ▼
GIS Outputs (.tif + .gpkg)
```

---

# 📂 Project Structure

```text
Geospatial-Segmentation
│
├── data
│   ├── input_images
│   └── outputs
│
├── src
│   ├── model_router.py
│   ├── inference_pipeline.py
│   ├── building_model.py
│   ├── road_model.py
│   ├── water_model.py
│   ├── water_line_model.py
│   ├── road_centerline_model.py
│   └── utils.py
│
├── requirements.txt
├── main.py
└── README.md
```

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/SaiCharan-N/geospatial-segmentation.git

cd geospatial-segmentation
```

Create a virtual environment

```bash
python -m venv venv
```

Activate the environment

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶ Running the Project

```bash
python main.py
```

---

# 📥 Input

Place GeoTIFF satellite images inside

```text
data/input_images/
```

Example

```text
sample.tif
```

---

# 📤 Output

The pipeline automatically generates

```text
building_output.tif

road_output.tif

water_output.tif

road_centerline_output.tif

water_line_output.tif

GIS_Vector_Output.gpkg
```

Compatible with:

- QGIS
- ArcGIS
- GeoPandas
- GDAL

---

# 💡 Technical Highlights

- Sliding Window Inference
- Dynamic Model Routing
- Multi-model Prediction Fusion
- Morphological Refinement
- Skeletonization
- Raster-to-Vector Conversion
- GeoPackage Generation
- Memory Efficient Processing

---

# 🚧 Challenges Addressed

- Processing ultra-high-resolution satellite imagery
- GPU memory optimization
- Spatial consistency across tiles
- Accurate road centerline extraction
- Water boundary refinement
- GIS-compatible vector generation

---

# 🔮 Future Work

- 🌐 Interactive Web GIS Dashboard
- ☁ Cloud Deployment (FastAPI + Docker)
- 📡 Real-Time Satellite Inference API
- 🧭 Road Graph Network Extraction
- ⚡ Batch Processing Pipeline
- 🤖 Foundation Models for Remote Sensing

---

# 👨‍💻 Authors

- **Jaswanth Yadurla**
- **Sai Charan**
- **Geethika**
- **Pradeep**

**Research Areas**

Computer Vision • Deep Learning • Remote Sensing • Geospatial AI • GIS

---

# 🏁 Project Impact

This project demonstrates a scalable geospatial intelligence pipeline capable of transforming raw satellite imagery into structured GIS-ready datasets using specialized deep learning models. The system supports applications in urban planning, transportation analysis, environmental monitoring, and large-scale spatial intelligence.

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!

**Built with ❤️ for the IIT Tirupati Geospatial AI Hackathon**
