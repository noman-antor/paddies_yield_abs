# 🌾 Paddies Yield

**Paddies Yield** is a machine learning-based prediction system integrated with a RESTful FastAPI backend. The system is designed to assist agricultural planning by analyzing soil quality, seasonal factors, and land area to optimize rice production in various districts of Bangladesh.

---

## 📌 Table of Contents

- [📖 Project Overview](#-project-overview)
- [🚀 Functionalities](#-functionalities)
  - [Soil Ingredients Test](#soil-ingredients-test)
  - [Region Based Maximum Production](#region-based-maximum-production)
  - [Fertilizer/Pesticide Recommendation](#-fertilizerpesticide-recommendation)
- [🎥 Demo Video ](#-demo-video)
- [🛠 Tech Stack](#-tech-stack)
- [🧹 Data Preprocessing](#-data-preprocessing)
- [📌 Model Selection](#-model-selection)
  - [🧪 Soil Ingredient Test](#-soil-ingredient-test)
  - [🗺️ Region Based Maximum Production](#region-based-maximum-production)
  - [🌿 Fertilizer/Pesticide Recommendation](#-fertilizerpesticide-recommendation)

---

## 📖 Project Overview

**Paddies Yield** aims to support decision-making in agriculture by:
- Predicting the concentration of soil nutrients (Nitrogen, Phosphorus, Potassium - NPK) from input data for a particular crop type
- Estimating the maximum possible paddy yield for a given district in Bangladesh based on season and land area.
- Recommending the amount of fertilizer and pesticide required to achieve the maximum predicted yield.

This project leverages real agricultural and environmental datasets and integrates data science with domain expertise in crop production.

---

## 🚀 Functionalities

- Data Validation: Pydantic
- Networking Package: dio: ^5.4.0

### Soil Ingredients Test
---
- Endpoint: `POST localhost:8050/soil_test`
- Input Format

  <img src="assets/ss2.jpg" alt="preview" width="300">
 
- Output Format

  <img src="assets/ss3.jpg" alt="preview" width="300">

### Region Based Maximum Production
---
- Endpoint: `POST localhost:8050/product_predict`
- Input Format

  <img src="assets/ss4.jpg" alt="preview" width="300">  
- Output Format

  <img src="assets/ss6.jpg" alt="preview" width="300">

### Fertilizer/Pesticide Recommendation 
---
- endpoint: `POST localhost:8050/fertil_predict`
- Input Format

   <img src="assets/ss7.jpg" alt="preview" width="300">
- Output Format

   <img src="assets/ss8.jpg" alt="preview" width="300">

---

## 🎥 Demo Video 
[Click here to watch full application](https://drive.google.com/file/d/1Or7wS_EG-0u5zYQWcEdlrTYJ365a3uq4/view?usp=sharing)

---

## 🛠 Tech Stack

- **Language:** Python 3.11.7, Dart
- **Libraries:** Scikit-learn, Pandas, Numpy 
- **API Framework:** FastAPI
- **Frontend Framework:** Flutter  
- **Server:** Uvicorn  
- **Others:** Pydantic, JSON, Swagger UI

---

## 🧹 Data Preprocessing

- Missing data imputation
- Outlier detection and removal
- Conversion of categorical features (e.g., season, district)

## 📌 Model Selection

Models were evaluated for multiple sub-tasks:

### 🧪 Soil Ingredient Test  
---
**Model Used:** `RandomForestRegressor`  
- Predicts the portion of Nitrogen (N), Phosphorus (P), and Potassium (K) in the soil based on input soil characteristics.
- Train-test split: `80/20`

  ![Soil Ingredient Prediction](assets/soil_ingredient_test.png)

### 🗺️ Region Based Maximum Production 
---
**Model Used:** `RandomForestRegressor`  
- Estimates the maximum potential paddy production for a district in Bangladesh given land area and season.
- Train-test split: `80/20`

  ![Region Yield Prediction](assets/region_maximum_production.png)

### 🌿 Fertilizer/Pesticide Recommendation 
---
**Model Used:** `RandomForestRegressor` 
- Recommends the quantity of fertilizer and pesticide required to reach the predicted maximum yield.
- Train-test split: `80/20`

  ![Fertilizer Recommendation](assets/fertilizer&pesticides.png)

---




