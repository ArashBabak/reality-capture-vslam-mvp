# 360° Reality Capture & VSLAM Pipeline (MVP)

A modular pipeline designed for processing 360-degree video footage, extracting camera trajectories, and generating interactive 3D spatial visualizations for site monitoring and reality capture.

---

## Overview

This project implements an advanced workflow for converting raw 360-degree video inputs (captured via **Insta360** cameras) into actionable 3D spatial data. By combining **Visual SLAM (vslam)** algorithms, depth estimation models, and WebGL rendering, the system bridges raw spatial recording with browser-based interactive 3D visualization.

*Note: Due to proprietary and company confidentiality policies (Company 333), core proprietary scripts, internal configuration files, and production deployment parameters are omitted from this public repository.*

---
### Interactive 3D Pipeline Demo

<p align="center">


https://github.com/user-attachments/assets/02094497-251a-4c8d-9da8-0becb8e66000

  
</p>

---

## My Role

**Software Developer**

Key contributions and responsibilities:
* **Research & Prototyping:** Conducted technical R&D and built proof-of-concept prototypes for spatial tracking.
* **Pipeline Implementation:** Designed and developed the 360° video processing and conversion workflows.
* **3D Visualization:** Implemented interactive 3D spatial rendering modules using Three.js.
* **Third-Party Integration:** Integrated complex computer vision libraries (Stella-VSLAM) and depth estimation tools.
* **AI-Accelerated Workflow:** Leveraged Cursor AI IDE for rapid prototyping, algorithm optimization, and code refactoring.

---

## Core Capabilities

* **Video Ingestion & Frame Extraction:** Automated processing of panoramic video formats into standardized frames using **FFmpeg**[cite: 18].
* **Spatial Tracking & Mapping:** Integration with **Stella-VSLAM** for camera trajectory extraction and environmental point cloud generation (`map.msg`).
* **Depth Estimation & 3D Reconstruction:** Utilizes deep learning-based depth models (such as **Depth-Anything-V2**) alongside **Open3D** to generate metric depth maps, 3D meshes (`.glb`), and point clouds (`.ply`).
* **Interactive Web Viewer:** Dynamic 3D rendering of spatial environments and camera motion paths using **Three.js**.
* **AI-Assisted Development:** Accelerated R&D, algorithm optimization, and spatial geometry computation powered by **Cursor AI IDE**.

---

## Technology Stack

| Domain | Technologies & Libraries |
| :--- | :--- |
| **Media & Video Processing** | FFmpeg, Insta360 Formats |
| **Computer Vision / SLAM** | Stella-VSLAM, OpenCV |
| **AI / Depth Estimation** | PyTorch, Depth-Anything-V2, Open3D |
| **Web Frontend & 3D** | Three.js, JavaScript, WebGL |
| **Development Workflow** | Cursor AI IDE, Python, Git |

---

## High-Level Architecture

The system follows a sequential multi-stage processing pipeline to transform raw panoramic videos into web-ready 3D experiences:

### 1. Ingestion & Frame Extraction
Raw panoramic video inputs from Insta360 cameras are processed to extract and format high-resolution frame sequences using customized **FFmpeg** workflows[cite: 18, 22, 23].

### 2. VSLAM & Trajectory Mapping
Extracted frames are processed through **Stella-VSLAM** (leveraging custom camera calibration profiles) to estimate camera poses, compute sparse point clouds, and export trajectory logs (`frame-trajectory.txt` and `map.msg`)[cite: 18, 22].

### 3. Depth Estimation & 3D Reconstruction
Using deep learning frameworks (**PyTorch** and **Depth-Anything-V2**) alongside **Open3D**, the pipeline generates metric depth maps and reconstructs 3D assets (`walls_proxy.glb`, `building_mesh.glb`, and `stella-cloud.ply`) for spatial representation[cite: 24, 25].

### 4. Interactive Web Visualization
The final output assets and trajectory coordinates are loaded into a dynamic **Three.js** web viewport, allowing users to navigate through the 3D space interactively[cite: 21].

---




## License & Confidentiality
This repository serves as a portfolio/public demonstration of architecture concepts. Core enterprise implementations and proprietary modules developed for **Engineering Office 333** remain confidential.
