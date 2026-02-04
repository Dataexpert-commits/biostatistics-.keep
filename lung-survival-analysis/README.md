# Lung Cancer Survival Analysis (Kaplan–Meier & Cox Proportional Hazards)

This project performs a biostatistical survival analysis using the `lung` dataset from the **survival** package in R. The analysis evaluates time-to-event outcomes in patients with advanced lung cancer using Kaplan–Meier curves, log-rank tests, Cox proportional hazards models, and proportional hazards diagnostics.

---

## 📌 Objectives

- Estimate survival probabilities using **Kaplan–Meier curves**
- Compare survival between patient groups (sex, age categories)
- Fit and interpret a **Cox proportional hazards model**
- Evaluate hazard ratios (HR) and their confidence intervals
- Test the **proportional hazards assumption** using Schoenfeld residuals

---

## 🧪 Methods Used

### **1. Kaplan–Meier Survival Estimation**
- Created survival objects using `Surv()`
- Estimated curves using `survfit()`
- Compared groups using log-rank tests
- Visualized curves with confidence intervals and risk tables

### **2. Cox Proportional Hazards Modeling**
- Modeled the effect of sex and age on survival time
- Interpreted hazard ratios using `broom::tidy()`
- Evaluated statistical significance and confidence intervals

### **3. PH Assumption Check**
- Used `cox.zph()` to test the proportional hazards assumption
- Visualized residuals using `ggcoxzph()`

---

## 📈 Key Findings 

- **Sex differences:**  
  Kaplan–Meier curves typically show survival differences between males and females, supported by log-rank test p-values.

- **Age impact:**  
  Older patients often have higher hazard (shorter survival), reflected by HR > 1 in the Cox model.

- **Model validity:**  
  Schoenfeld residuals often indicate no major violations of the proportional hazards assumption.

---

## 🛠️ Technologies Used

- **R**  
- `survival`  
- `survminer`  
- `tidyverse`  
- `broom`

---

## 📂 Folder Structure
- biostatistics/
- lung-survival-analysis/
- notebooks/
- lung-survival-analysis.Rmd
= data/
- src/
- README.md


---

## 🚀 How to Run the Analysis

1. Install required packages:
[```r
install.packages(c("survival", "survminer", "tidyverse", "broom"))}
2. Open the .Rmd file in RStudio
3. Run all chunks or click Knit → HTML

## 📦 Dataset
This project uses the built-in lung dataset from the survival package:
data("lung", package = "survival")

No external data download is required



