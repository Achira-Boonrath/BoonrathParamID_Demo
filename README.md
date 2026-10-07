# Video Results Concerning Simplified Model Parameter Identification for Net-Captured Debris Towing

This repository presents video results concerning the **parameter identification framework** that replaces a computationally intensive net-wrapped space debris model with a simplified **4-Sub-Tether (ST) system**, enabling  efficient long-duration towing simulations to be performed. The framework is described in detail in:

**A. Boonrath, T. Singh, and E. M. Botta, “Identification of parameters for tethered satellite system to emulate net-captured debris towing,” Acta Astronautica, vol. 225, pp. 676–688, 2024. doi: https://doi.org/10.1016/j.actaastro.2024.09.022.**

---

## Computational Challenge & Solution

Simulations of space debris towing in disposal missions using a full-net model produce high-fidelity and  accurate dynamics. However, these simulations necessitate modeling highly complex multi-body interactions:
- **High Computational Cost**: The full-net model comprises over 1000 degrees of freedom and requires **approximately 4.5 hours per towing simulation** on a typical workstation. Since long-duration debris deorbiting studies may necessitate dozens or hundreds of removal simulations, this model is impractical for such applications.
- **Proposed Solution**: Identify equivalent physical properties for a 4-sub-tether model to replicate the high-fidelity dynamics with comparable accuracy, reducing execution time to **less than 4 minutes**, achieving over 60 times speedup. To accomplish this, optimization problems are formulated to minimize the differences between the models’ dynamics, and global optimization algorithms, such as Particle Swarm Optimization, are applied to solve them.

---

## High-Fidelity vs. Simplified Model Simulation Video Comparison

| High-Fidelity Full-Net Towing | Parameter-Identified 4-ST Towing |
| :---: | :---: |
| [[High-Fidelity Full-Net System]](https://github.com/user-attachments/assets/8df70442-1d4f-4e92-8d89-b47e22433246) | [[ST System With Parameters]](https://github.com/user-attachments/assets/14cffe33-ff67-41fc-b90f-aa16763acfaf)|
| *Execution time:* $\sim 4.5\text{ hours}$ | *Execution time:* $< 4\text{ minutes}$ ($>60\times$ speedup) |

**Key Takeaway**: The 4-ST model is capable of preserving the essential relative translational and rotational dynamics of the full-net whilst being much faster to simulate.
