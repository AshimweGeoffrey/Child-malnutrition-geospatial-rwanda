# Geospatial & ML Analysis of Child Malnutrition in Rwanda

Research-oriented system for mapping and predicting district-level child malnutrition risk in Rwanda. This project combines geospatial analysis, statistical profiling, and machine-learning modelling using official NISR datasets to produce actionable, district-level risk scores and interactive visualizations.

Live demo
- Analytics dashboard: https://nisr-hackthon-ak.vercel.app/
- Prediction API: https://nisr-hackthon-ak-p9n3.vercel.app/

What this repo does
- Map spatial hotspots of child malnutrition across Rwanda’s 30 districts.
- Produce district-level analytic dashboards covering nutrition, socioeconomic, and agricultural indicators.
- Train and expose a Python ML model that outputs district malnutrition risk scores.
- Provide frontend tools for interactive visualization and model interpretation.

Research objectives
- Identify spatial clusters of high malnutrition risk.
- Quantify district-level predictors using cleaned and engineered features.
- Build a reproducible ML workflow for district risk classification.
- Deliver a visual interface to support evidence-based policy decisions.

Key outputs
- Hotspot Map: District-level geospatial visualization of stunting and undernutrition.
- Analytics Dashboard: Nutrition, economic, and agricultural indicators with district comparisons.
- ML Model: Random Forest–based pipeline with engineered composite indicators and evaluation metrics.
- Interpretation Tools: Summary reports and model-driven district insights.

Repository structure
- ml_model/ — Training notebooks, preprocessing scripts, feature engineering, reproducible pipelines, and evaluation metrics.
- Nisr-Data_analysis/ — Raw data cleaning, exploratory analysis, provenance notes, and data-preparation scripts used to derive model features.
- nisr-frontend/ — React app for geospatial maps, district analytics, report exports and dashboards.
- react-web-prediction_model/ — Minimal React + TypeScript demo for running quick predictions against the prediction API.

Quick start

Frontend (Analytics Dashboard)
1. cd nisr-frontend
2. npm install
3. npm run dev

Frontend (Prediction Demo)
1. cd react-web-prediction_model
2. npm install
3. npm run dev

ML model (developer guide)
1. cd ml_model
2. python -m venv .venv && source .venv/bin/activate
3. pip install -r requirements.txt
4. Run preprocessing and training notebooks or scripts (see ml_model/README.md for exact commands)

Deployment notes
- The prediction endpoint is deployed serverlessly. The frontend triggers a short warm-up to reduce cold-start latency before redirecting users to the ML interface.
- For productionize: containerize the model service, add a lightweight cache/warm-up layer (e.g., scheduled keep-alive), and enable model versioning with CI/CD for retraining and rollout.

Team
- Ashimwe Geoffrey
- Kamanzi Serge

Joint contributions: data analysis, modelling, frontend development, deployment.

License & contact
- Open-source. For inquiries or collaboration, open an issue in this repository.
