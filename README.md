# 🛫 Safety Braking Distance Estimation

## Introduction

In modern aviation and transportation, accurate **braking distance estimation** is a cornerstone of operational safety. These systems provide critical data to pilots and automated flight controllers to prevent runway overruns and ensure landing precision.

As **Neural Networks** become the standard for handling these complex, non-linear calculations, this project provides a framework to verify their performance and ensure they meet rigorous safety standards.

---

## 🛩️ Case Study: Cessna 172 Skyhawk

This repository specifically targets the **Cessna 172 Skyhawk**, the most successful and mass-produced aircraft in history.

* **History:** In production since 1956 with over 44,000 units built.
* **The Challenge:** Estimating the "ground roll" (the distance required to stop after touchdown) involves a complex interplay of air density, aircraft weight, touchdown speed, and braking friction.
* **Objective:** Transitioning from manual lookup tables to robust, neural-network-based estimations.

---

## ✨ Features

* **Neural Network Architectures:** Pre-configured models optimized for braking dynamics.
* **Safety Verification:** Scripts to test model robustness against edge-case flight conditions.
* **Cessna 172 Dynamics:** A dedicated data generation engine tailored to the Skyhawk's performance profile.

---

## 🛠️ Installation

This project uses `pyproject.toml` for modern dependency management.

### 🚀 Quick Start (Recommended)

Install the package directly into your environment using `pip`:

```bash
pip install git+https://github.com/ducoffeM/safety_braking_distance_estimation.git

```

### 👩‍💻 Developer Setup

If you want to modify the source code or run the internal scripts:

```bash
git clone https://github.com/ducoffeM/safety_braking_distance_estimation.git
cd safety_braking_distance_estimation
pip install -e .

```

---

## 📊 Usage

You can easily generate synthetic flight data to train or validate your own models using the built-in generator:

```python
from cesna import generate_cesna_dataset

# Generate 100 random flight samples (features and target distances)
X, Y = generate_cesna_dataset(N=100)

print(f"Generated {len(X)} samples for Cessna 172 braking analysis.")

```


## License

[Insert License Type, e.g., MIT]