# UrbanEV: Charging Network Stress Test

**UrbanEV** is a discrete event simulation project that models the capacity and resilience of public electric vehicle (EV) charging infrastructure. Using empirical data from Shenzhen, China, the project simulates charging station behavior to predict network performance under various adoption scenarios.

## 📌 Project Overview

This study utilizes the **UrbanEV** dataset (Sep 2022 – Feb 2023) to model charging behavior across 1,682 public stations. By using **Python** and **SimPy**, the project transforms historical occupancy and duration data into a stochastic simulation to evaluate:
* **Grid Resilience:** How well the current infrastructure handles demand.
* **Stress Testing:** The impact of mass EV adoption and reduced home charging availability on public stations.
* **Service Quality:** Metrics on successful charging sessions versus "lost customers" (failed sessions due to full capacity).

## 🚀 Key Features

* **Data-Driven Simulation:** Calibrated using real-world occupancy (arrival rates) and session duration (service times) data.
* **Stochastic Modeling:**
    * **Arrivals:** Modeled using a Poisson distribution derived from hourly occupancy weights.
    * **Service Times:** Modeled using a Gaussian distribution based on actual charging durations.
* **Scenario Analysis:** Compares current sustainable usage against a critical future stress test.

## 📊 Scenarios Modeled

The simulation compares two distinct grid load environments:

| Scenario | Description | Parameters |
| :--- | :--- | :--- |
| **A: Sustainable Present** | Represents the current "Early Adopter" phase where most users have private garages. | **12%** EV Adoption<br>**82%** Home Charging |
| **B: Critical Future** | A stress test simulating mass adoption in dense urban areas with limited private infrastructure. | **70%** EV Adoption<br>**10%** Home Charging |

## 🛠️ Technologies & Requirements

The project is built using Python. Key libraries include:

* `simpy` (Discrete event simulation)
* `pandas` (Data manipulation)
* `numpy` (Numerical operations)
* `matplotlib` (Data visualization)

### Installation

To run this project, ensure you have the required packages installed:

```bash
pip install simpy pandas numpy matplotlib
