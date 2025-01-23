# Predictive Analysis for Manufacturing Operations

This repository contains the implementation of a predictive analysis API designed for manufacturing workflows. The API utilizes machine learning to forecast machine downtime or production defects, enabling better decision-making and operational efficiency.

## Features
- **Data Upload:** Upload manufacturing data via a POST endpoint.
- **Model Training:** Train a Random Forest model with fine-tuning using Optuna and get performance metrics like accuracy and F1-score.
- **Prediction:** Make predictions using JSON input and receive results, including confidence scores, in JSON format.

## Technologies Used
- **Backend Framework:** FastAPI
- **Machine Learning:** scikit-learn (Random Forest)
- **Hyperparameter Tuning:** Optuna
- **Data Preprocessing:** Numpy, pandas, and StandardScaler
- **Testing Tools:** requests module 

## Setup Instructions

### Prerequisites
Ensure you have the following installed:
- Python 3.8 or later
- pip (Python package manager)



### Endpoints
1. **Predict:** POST `/predict`
   - Accepts JSON input (e.g., `{ "Temperature": 80, "Run_Time": 120 }`) and returns predictions (e.g., `{ "Downtime": "Yes", "Confidence": 0.85 }`).

### Example Request
**Input Example:**
```bash
data = {
    "SupplierQuality":86.648534	 ,
    "DefectRate": 3.121492,
    "QualityScore": 63.463494	,
    "MaintenanceHours":9  ,
    "DowntimePercentage": 0.052343,
    "SafetyIncidents":1 ,
    "EnergyConsumption": 2419.616785,	
}
```
Response:
```json
{
  "Downtime": "Yes",
  "Confidence": 0.85
}
```

## Project Structure
- `app.py`: Contains the API implementation.
- `predictive_analysis.ipynb`: Includes the ML model training and prediction logic with Random Forest and Optuna.
- `test.py`: Sample dataset for testing.
- `final_random_forest_model.pkl`: Trained Predictive model.
- `Scaler.pkl`: Scaling Attribute.

## Testing
Use tools like request module to test the API endpoints locally. Ensure the server is running before making requests.

## Acknowledgments
- Dataset sources: Kaggle .
- Frameworks and libraries: numpy , pandas , FastAPI, scikit-learn, Optuna , requests.

---
Feel free to contribute or open issues for any questions or enhancements!
