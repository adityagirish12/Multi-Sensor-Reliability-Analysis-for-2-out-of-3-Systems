# Multi-Sensor Reliability Analysis for 2-out-of-3 Systems

A comprehensive reliability analysis of LiDAR, Camera, and Radar sensors using Weibull, Exponential, and Normal lifetime models, including system-level 2-out-of-3 redundancy modeling, Bayesian detection analysis, and sensitivity evaluation of hardware upgrades. 

---

## 📌 Overview

This project models and compares the reliability of three autonomous-vehicle sensor types:

- **LiDAR** – modeled with a **Weibull** lifetime distribution  
- **Camera** – modeled with an **Exponential** lifetime distribution  
- **Radar** – modeled with a **Normal** lifetime distribution  

It then evaluates **system reliability** for different 2-out-of-3 (2oo3) architectures and studies how **hardware upgrades** affect overall system performance.

---

## 🎯 Key Objectives

- Compute **component reliability** at 5,000 hours and **Mean Time to Failure (MTTF)** for each sensor.
- Use **Bayes’ Theorem** to estimate the probability of severe conditions given a correct detection.
- Derive and apply the **2-out-of-3 system reliability formula**:
  \[
  R_\text{sys} = 3R^2 - 2R^3
  \]
- Evaluate different configurations:
  - Three LiDAR
  - Three Camera
  - Three Radar
  - Mixed (LiDAR + Camera + Radar)
- Perform **sensitivity analysis** on hardware upgrades (e.g., increased LiDAR lifetime, reduced Camera failure rate, reduced Radar variance).

---

## 🧮 Methods & Models

**Distributions**

- **LiDAR**: Weibull \( R_L(t) = e^{-(t / \eta)^\beta} \)
- **Camera**: Exponential \( R_C(t) = e^{-\lambda t} \)
- **Radar**: Normal \( R_R(t) = 1 - \Phi\left(\frac{t - \mu}{\sigma}\right) \)

**Bayesian Analysis**

- Uses **Law of Total Probability** and **Bayes’ Theorem** to compute:
  - \( P(\text{Correct Detection}) \)
  - \( P(\text{Severe} \mid \text{Correct Detection}) \)

**System-Level Modeling**

- 2-out-of-3 rule: system succeeds if at least two sensors are operational.
- Handles both **identical** and **mixed-type** sensor configurations.

**Sensitivity Analysis**

- LiDAR: +20% increase in characteristic life \( \eta \)
- Camera: −15% decrease in failure rate \( \lambda \)
- Radar: −25% reduction in variance \( \sigma^2 \)


