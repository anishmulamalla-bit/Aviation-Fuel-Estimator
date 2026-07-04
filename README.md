# Physics-Informed Aircraft Performance & Fuel Burn Estimation Engine

Project Overview
This data science project implements a machine learning pipeline to estimate aircraft thrust demand and environmental performance using real flight state vector data. Rather than relying purely on statistical patterns, this model embeds core aerodynamic engineering principles—specifically the International Standard Atmosphere (ISA) model—to calculate dynamic air density variations across different altitudes.

Key Highlights & Progression
* **Phase 1 (Synthetic Prototyping):** Established baseline model logic using synthetic flight paths to ensure architecture convergence.
* **Phase 2 (High-Fidelity Flight Telemetry Pipeline):** Implemented an engineering data pipeline handling raw state vector telemetry variables (Altitude, Ground Speed, Vertical Rate).
* **Feature Engineering:** Programmed aerodynamic physics equations to map variable dynamic pressure loads ($\frac{1}{2} \rho V^2$) based on atmospheric decay.

Technical Performance
* **Algorithm Used:** Extreme Gradient Boosting (XGBoost Regressor)
* **Mean Absolute Error (MAE):** 100.14 units
* **Model Accuracy ($R^2$ Score):** 99.94%
