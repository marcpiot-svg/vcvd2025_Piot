# Tyre Force Simulation (Pacejka Magic Formula)

This project simulates vehicle tyre forces (**Fx** and **Fy**) using the **Pacejka Magic Formula** with **Combined Slip** logic.

It is designed to analyze how longitudinal slip ($\kappa$) affects lateral forces and vice-versa, iterating over multiple vertical loads ($F_z$) including a specific load derived from the vehicle's mass.

## 📋 Features

* **Combined Slip Model:** Calculates theoretical slip $\sigma$ to accurately distribute forces vectorially.
* **Physics Compliance:** Uses `scipy.constants` for gravity ($g$) to ensure precision.
* **Dynamic Load Calculation:** Automatically derives the nominal vertical load ($F_z$) based on vehicle mass ($m=1200kg$), assuming equal weight distribution ($F_z = \frac{m \cdot g}{4}$).
* **Data-Driven:** Reads Pacejka coefficients dynamically from a CSV file.
* **Visualization:** Generates a comparative Matplotlib graph for $F_x$ (braking/traction) and $F_y$ (cornering).

## 🛠️ Prerequisites

You need **Python 3.x** and the following scientific libraries:

* `numpy`
* `pandas`
* `matplotlib`
* `scipy` (Required for physical constants)

Install them via pip:

```bash
pip install numpy pandas matplotlib scipy
