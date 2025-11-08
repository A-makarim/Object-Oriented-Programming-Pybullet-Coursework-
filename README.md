# OOP Project

This repository contains code for:
1. **Generating grasp data** using PyBullet simulations for two object types (**cuboid** or **cylinder**).
2. **Classifying** those grasps (using a **Random Forest** model).
3. **Visualizing** the resulting data in various plots and heatmaps.

---
## **Key Files**

- **`main.py`**  
  - **Top-level** script to either **generate new data** or **classify** existing data.
  - Runs a PyBullet **GUI** so you can see the simulation (when generating new data).

- **`train_model.py`**  
  - Trains a **Random Forest** classifier on either cuboid or cylinder data.
  - Saves the model in `models/` and updates the CSV with predictions.

- **`evaluate.py`**  
  - Optional evaluator logic (e.g., threshold-based success).

- **`robots/gripper.py`**  
  - Contains the `BaseGripper`, `PR2Gripper`, `CustomGripper` classes for PyBullet gripper control.

- **`plots/`**  
  - Python scripts to visualize or analyze results (e.g., heatmaps, confusion matrices, 3D scatter).

- **`data/`**  
  - Where CSV files of generated grasps are stored (e.g., `grasp_data_cuboid.csv`) plus updated CSVs with predictions (e.g. `updated_grasp_data_cuboid_with_predictions.csv`).

- **`models/`**  
  - Contains the trained Random Forest models (e.g. `cuboid_grasp_model.pkl`).

---

## **Installation and Requirements**

1. **Create** and **activate** a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate or on Windows: venv\Scripts\activate

2. Install dependencies:
   ```bash
   pip install -r requirements.txt


