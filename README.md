# Physics-Informed Aircraft Performance & Fuel Burn Estimation Engine

Project Overview
This data science project implements an end-to-end machine learning pipeline to estimate aircraft thrust demand and environmental performance using flight state vector data. Rather than relying purely on statistical patterns, this model embeds core aerodynamic engineering principles—specifically the International Standard Atmosphere (ISA) model—to calculate dynamic air density variations across differing altitudes.

Data Pipeline, Cleaning & EDA
Before training the predictive model, a rigorous data preparation and exploratory phase was executed:
* **Data Ingestion:** Ingested raw state vector telemetry data streams containing real-world flight variables like latitude, longitude, barometric altitude, ground speed, and vertical rates.
* **Data Cleaning & Handling Signal Drops:** Identified and removed real-world transponder anomalies, sensor noise, and temporary radar tracking dropouts (`NaN` values) to ensure data integrity.
* **Exploratory Data Analysis (EDA):** Analyzed the joint distributions of velocity and altitude to map out different aircraft behaviors across core flight phases (takeoff climbs, cruise altitudes, and descents).
* **Physics-Informed Feature Engineering:** Programmed aerodynamic physics equations to map variable dynamic pressure loads ($\frac{1}{2} \rho V^2$) by dynamically calculating atmospheric air density decay based on altitude.

Technical Performance
* **Algorithm Used:** Extreme Gradient Boosting (XGBoost Regressor)
* **Mean Absolute Error (MAE):** 100.14 units
* **Model Accuracy ($R^2$ Score):** 99.94%

Project Progression
1. **Phase 1 (Synthetic Prototyping):** Established baseline model logic using a controlled synthetic flight formula to ensure convergence.
2. **Phase 2 (High-Fidelity Telemetry Integration):** Upgraded the architecture to parse complex state vectors, transitioning from synthetic rules to actual physics-informed telemetry analysis.
