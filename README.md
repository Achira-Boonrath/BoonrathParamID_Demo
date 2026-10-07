# Sub-Tether Model Parameter Identification for Net-Captured Debris Towing

This repository presents video results for the **parameter identification framework** that replaces high-fidelity, computationally intensive net-debris models with a simplified **4-Sub-Tether (ST) system**, enabling long-duration orbital towing simulations.

---

## Motivation & Computational Challenge

Simulating post-capture debris towing with a full-net model requires modeling complex, multi-body dynamics:
- **Full-Net System Model**: Involves $1000+$ degrees of freedom, requiring approximately **$\sim 4.5\text{ hours}$ per towing simulation** on a typical workstation. Given that long-duration debris deorbiting studies may require evaluating dozens or hundreds of removal simulations, this model is not practical for such purposes.
- **The Solution**: Identify equivalent physical properties for a 4-sub-tether model so it replicates the high-fidelity dynamics with good accuracy while executing in **$< 4\text{ minutes}$ ($>60\times$ speedup)**.

---

## High-Fidelity vs. Simplified Model Video Comparison

| High-Fidelity Full-Net Towing | Parameter-Identified 4-ST Towing |
| :---: | :---: |
| [![High-Fidelity Full-Net System](../assets/thumbnails/high-fidelity_full-net_system_thumb.jpg)](<../src/High-Fidelity Full-Net System.mp4>) | [![ST System With Parameters](../assets/thumbnails/st_system_with_parameters_obtained_from_the_parameter_identification_framework_thumb.jpg)](<../src/ST System With Parameters Obtained From the Parameter Identification Framework.mp4>) |
| *Execution time: $\sim 4.5\text{ hours}$* | *Execution time: $< 4\text{ minutes}$ ($>60\times$ speedup)* |

