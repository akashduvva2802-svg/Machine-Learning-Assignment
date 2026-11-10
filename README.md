## CFD Mixing Tank – Suspension Quality Prediction

**Dataset:** Kaggle "Computational Fluid Dynamics: Mixing Tank" – 1,014 CFD simulations of solid-liquid stirred vessels (impeller design, speed, densities, viscosity, solid fraction).
**Prediction target:** Y = RSD/100, a mixing-quality measure (lower = better suspension). Models were trained on Design 1 (534 samples).
**Models:** Linear Regression (baseline) and Support Vector Regression with an RBF kernel.
**Results:** Linear Regression test R² = 0.07 (RMSE 0.163); SVR test R² = 0.72 (RMSE 0.089). As a well-mixed/poorly-mixed classifier (RSD ≤ 20%), SVR reached 91% accuracy versus 59% for Linear Regression. 5-fold CV confirmed the same picture (SVR R² ≈ 0.72).
**What I learned:** The physics is strongly non-linear, so a linear model underfits badly while an RBF kernel captures it. A model trained on one tank design does not transfer reliably to other designs.
