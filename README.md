# Random Forest Multi-Regression Model Demo

This repository contains a demo environment for serving a machine learning model using FastAPI.

**Note:**  
This demo is a part of my main project [EnergyTariffAdvisor](https://github.com/GannaUK/EnergyTariffAdvisor).  
For full context, usage examples, and integration, please refer to the main repository.

## Archive Contents

The archive `rf_demo_env.zip` contains the following files:
- `model.pkl` — Trained Random Forest multi-regression model (accepts 119 features from a questionnaire and returns an array of 48 intervals: a predicted consumption profile).
- `requirements.txt` — Python dependencies for running the API.
- `rest_api.py` — Main FastAPI application for model inference.
- `run_api.py` — Script to launch the FastAPI server.


## Model Description

- **Type**: Random Forest Multi-Regression
- **Input**: 119 features (from a user questionnaire)
- **Output**: Array of 48 intervals (predicted consumption profile)

## How to Use

1. Extract the archive:
   ```
   unzip rf_demo_env.zip
   cd rf_demo_env
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the FastAPI application:
   ```
   python run_api.py
   ```

4. The API will be available at `http://localhost:8001`.

## Example Request

Send a POST request to the `/predict` endpoint with a JSON body containing 119 feature values.

```json
{
  "features": [/* 119 feature values here */]
}
```

The response will be a JSON with an array of 48 predicted intervals.
