# 🏙 An R Analysis of Toronto Short-Term Rentals

## 📌 Project Overview

This project investigates the key factors influencing nightly Airbnb prices in Toronto using publicly available data from the **Inside Airbnb (September 2025 release)**.

The analysis applies statistical modeling and exploratory data analysis techniques to understand how listing characteristics and neighbourhood demand impact price variation.

---

## 🎯 Research Question

> To what extent do accommodation capacity, review ratings, and neighbourhood demand explain variation in nightly Airbnb prices in Toronto?

---

## 📊 Key Findings

- 📈 Each additional guest capacity is associated with approximately **22% higher nightly price**
- ⭐ A one-point increase in review rating corresponds to roughly **20% higher price**
- 📍 Listings in **low-demand neighbourhoods charge ~48% less** than comparable listings in high-demand areas
- 📐 The model explains approximately **50% of price variation (R² ≈ 0.49)**

These results demonstrate the combined importance of property size, perceived quality, and location in short-term rental pricing.

---

## 🧠 Methodology

### 1️⃣ Data Preparation

- Filtered active listings with valid price and review data  
- Parsed currency fields into numeric format  
- Created neighbourhood demand groups using average review activity  
- Applied log transformation to price to address right-skewness  

### 2️⃣ Statistical Modeling

Multiple Linear Regression:

**Response variable:**  
- Log-transformed nightly price  

**Predictors:**  
- Accommodation capacity  
- Review scores rating  
- Neighbourhood demand group (High / Middle / Low)  

### 3️⃣ Model Diagnostics

- Residual vs Fitted analysis  
- Normal Q-Q plots  
- Scale-location checks  
- Leverage and influence analysis  

### 4️⃣ Hypothesis Testing

- Welch two-sample t-test comparing High vs Low demand neighbourhoods  
- Confirmed statistically significant price differences  

---

## 📈 Model Performance

| Metric | Value |
|--------|--------|
| R² | 0.494 |
| Adjusted R² | 0.493 |
| Residual Std. Error | 0.512 |
| F-statistic | 3062.41 |
| p-value | < 0.001 |

---

## 📁 Repository Structure

---

## 🛠 Tools & Technologies

- R  
- tidyverse  
- ggplot2  
- broom  
- Quarto  
- Git / GitHub 

---

## ⚠ Limitations

- Selection bias (active listings only)  
- Potential non-independence of listings  
- Omitted variable bias (amenities, room type, proximity)  
- Moderate deviation from normality in residual tails  

---

## 🚀 Future Improvements

- Include additional predictors (amenities, room type, distance to downtown)  
- Apply cross-validation for out-of-sample evaluation  
- Compare alternative models (LASSO, Ridge, Random Forest)  
- Incorporate spatial modeling techniques  

---

## 📚 Data Source

Inside Airbnb  
http://insideairbnb.com  

---

## ✍ Acknowledgment

OpenAI’s ChatGPT was used to assist with code debugging and formatting support.  
All statistical analysis, interpretation, and modeling decisions were conducted independently.
