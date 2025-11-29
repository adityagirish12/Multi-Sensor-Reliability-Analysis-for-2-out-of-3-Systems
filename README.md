# Multi-Sensor Reliability Analysis for 2-out-of-3 Systems

A summarized explanation of how each part of the analysis was performed, the formulas used (only referenced by name), and the results obtained.

## Component Reliability Analysis
**How it was done:**  
- LiDAR reliability was computed using the *Weibull reliability function*.  
- Camera reliability was computed using the *Exponential reliability function*.  
- Radar reliability was computed using the *Normal distribution survival function*.  
- Reliability at 5,000 hours was calculated by plugging time into each model.

**Result:**  
LiDAR remained the most reliable at long durations, Camera showed moderate reliability, and Radar declined the fastest.

## Mean Time to Failure (MTTF)
**How it was done:**  
- LiDAR MTTF was calculated using the *Weibull mean lifetime formula*.  
- Camera MTTF was computed using the *Exponential mean lifetime expression*.  
- Radar MTTF was estimated using the *Normal distribution expectation*.

**Result:**  
LiDAR had the highest MTTF, Camera was moderate, and Radar had the lowest due to larger spread in lifetimes.

## Bayesian Detection Analysis
**How it was done:**  
- The *Law of Total Probability* was used to find the overall chance of correct detection by combining detection probabilities under all conditions.  
- *Bayes’ Theorem* was then used to find the probability of severe conditions given a correct detection.

**Result:**  
Correct detections were highly likely overall, but the likelihood that a correct detection was caused by severe conditions was relatively low.

## 2-out-of-3 System Reliability
**How it was done:**  
- For identical sensors, the *standard 2-out-of-3 system reliability formula* was applied to each sensor type.  
- For mixed sensors, system reliability was computed by evaluating all combinations where at least two sensors survive, using the *joint survival probability method*.

**Result:**  
A three-LiDAR system had the highest reliability, followed by mixed systems, then Camera-only, and Radar-only was the least reliable.

## Sensitivity Analysis
**How it was done:**  
- LiDAR improvement was modeled by adjusting its parameters in the *Weibull model*.  
- Camera improvement was simulated by lowering its rate parameter in the *Exponential model*.  
- Radar improvement was tested by reducing its spread in the *Normal distribution model*.  
- All upgrades were re-evaluated through the same component calculations and system-level 2-out-of-3 method.

**Result:**  
LiDAR upgrades produced the biggest improvement, Camera upgrades gave moderate enhancement, and Radar upgrades had smaller but noticeable benefits.

## Final Conclusion
LiDAR consistently outperforms the other two sensors in reliability, lifetime, and system-level performance. A 2-out-of-3 LiDAR setup is the optimal configuration, while mixed systems offer a balanced alternative. Hardware upgrades—especially for LiDAR—can significantly boost reliability.
