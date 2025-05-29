# 🔋 Battery Health Prediction using EIS – NASA Dataset

This project explores how batteries degrade over time by analyzing NASA's public Li-ion battery dataset. It combines data visualization and machine learning to understand and predict battery capacity using Electrochemical Impedance Spectroscopy (EIS) data.

---

## 📂 Dataset

- Source: [NASA Battery Dataset (Kaggle)](https://www.kaggle.com/datasets/patrickfleith/nasa-battery-dataset)
- Includes 7500+ `.csv` files with:
  - Impedance measurements (EIS)
  - Charge/discharge logs
  - Metadata: battery ID, temperature, cycle count, etc.

---

## ✅ Tasks

### 🟦 Task (a): EIS 3D Plot
- Created a 3D scatter plot of Re(Z) vs Im(Z) vs Cycle Count
- Shows how internal impedance changes as the battery ages

### 🟨 Task (b): Incremental Capacity Analysis (dQ/dV)
- Estimated capacity from current × time
- Computed `dQ/dV` vs Voltage and plotted it across cycles
- Helps visualize how charge profiles shift with aging

### 🟥 Task (c): ML Model for Capacity Prediction
- Merged impedance data with known capacity
- Used `Re`, `Rct`, and temperature as features
- Trained `RandomForestRegressor` with `GridSearchCV` tuning
- Achieved **R² Score: 0.74**, **MAE: 0.26** (on synthetic targets)

---

## 🧠 Tech Stack

- **Python 3** – Jupyter Notebook
- `pandas`, `numpy` – Data processing
- `matplotlib`, `mpl_toolkits` – 3D visualization
- `scikit-learn` – Model training & tuning

---

## 📊 Results

| Metric         | Score     |
|----------------|-----------|
| R² Score       | 0.7433 ✅ |
| MAE            | 0.2666    |

The model successfully predicted battery capacity from impedance signatures, even on synthetic data, showcasing the potential of EIS for battery health estimation.

---

## 📘 Explanation for Beginners

> Think of the battery like a sponge. EIS tells us how much it "pushes back" when we poke it with tiny electric signals. The more it resists or wobbles, the more we know about its age and health. We used this reaction data to teach a machine how to guess how much energy is left inside!

---

## 📌 Author

**Aswinthmani V**  
AI/ML Intern at AppSynergies  
[LinkedIn](https://www.linkedin.com/in/aswinthmani-v-ab6852240/) | [GitHub](https://github.com/Aswinthmani2003)

---

## 📄 License

MIT License – feel free to fork and build upon this work.
