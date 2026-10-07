# Simplified Model Parameter Identification for Net-Captured Debris Towing

This repository presents video results concerning the **parameter identification framework** that replaces high-fidelity, computationally intensive net-debris models with a simplified **4-Sub-Tether (ST) system**, enabling computationally efficient long-duration orbital towing simulations. The framework is described in detail in:

**A. Boonrath, T. Singh, and E. M. Botta, “Identification of parameters for tethered satellite system to emulate net-captured debris towing,” Acta Astronautica, vol. 225, pp. 676–688, 2024. doi: https://doi.org/10.1016/j.actaastro.2024.09.022.**

---

## Computational Challenge & Solution

Simulating post-capture debris towing with a full-net model requires modeling complex, multi-body dynamics:
- **Full-Net System Model**: Involves $1000+$ degrees of freedom, requiring **$\sim 4.5$ hours per towing simulation** on a typical workstation. Given that long-duration debris deorbiting studies may require evaluating dozens or hundreds of removal simulations, this model is not practical for such purposes.
- **The Solution**: Identify equivalent physical properties for a 4-sub-tether model so it replicates the high-fidelity dynamics with good accuracy while executing in **$< 4$ minutes ($>60\times$ speedup)**. For this task, I formulated optimization problems to minimize 
differences between the models’ dynamics and applied global optimization algorithms (e.g., Particle Swarm Optimization) to solve the minimization problems. 

---

## High-Fidelity vs. Simplified Model Simulation Video Comparison

| High-Fidelity Full-Net Towing | Parameter-Identified 4-ST Towing |
| :---: | :---: |
| [[High-Fidelity Full-Net System]](https://github.com/user-attachments/assets/8df70442-1d4f-4e92-8d89-b47e22433246) | [[ST System With Parameters]](https://github.com/user-attachments/assets/14cffe33-ff67-41fc-b90f-aa16763acfaf)|
| *Execution time:* $\sim 4.5\text{ hours}$ | *Execution time:* $< 4\text{ minutes}$ ($>60\times$ speedup) |

**Key Takeaway**: The 4-ST model is capable of preserving the essential relative translational and rotational dynamics of the full-net whilst being much faster to simulate.
