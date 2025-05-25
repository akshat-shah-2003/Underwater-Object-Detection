# 🧭 3D Acoustic Sensor Simulation with Delaunay Triangulation

This repository presents a comprehensive simulation of a **3D acoustic sensor system** designed to reconstruct the surface geometry of an underwater object using **sound wave reflections**, **Doppler shift calculations**, and **Delaunay triangulation**.

The simulation mimics how real-world acoustic sensors detect and process echo signals to determine surface structure and velocity of objects, using a combination of geometric and signal processing principles.

---

## 📦 Components of the Sensor System

### 1. Reconstruction System

- **Function**: Determines the 3D coordinates of reflection points on an object’s surface.
- **Process**:
  - Emits acoustic signals that reflect off the object.
  - Computes the time of flight and direction vector of the reflected signals.
  - Calculates distance based on time of flight and known speed of sound in water.
  - Uses the sensor's known coordinates to find the points of reflection.
- **Output**: A point cloud of 3D coordinates forming the object's surface.
- **Triangulation**: Delaunay triangulation is applied on the point cloud to build an optimal 3D mesh (tetrahedralization), maximizing minimum angles.

### 2. Receiver

- **Function**: Captures the reflected signal and processes:
  - **Frequency Shift Analysis (Doppler Effect)**:  Estimates object velocity
  - **Time of Flight**: Measures time delay of the reflected signal.
  - **Direction Vector**: Calculates direction of arrival and shares with the reconstruction system.

---

## 📁 File

- `DelaunaySimulation (2).ipynb`: Python-based Jupyter Notebook simulating:
  - Point cloud reconstruction from virtual sensors.
  - 3D Delaunay triangulation.
  - Mesh visualization.

---

## 🧰 Dependencies

Install the required libraries using pip:

```bash
pip install numpy scipy matplotlib
