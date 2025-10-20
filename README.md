# Medical Appointment No-Shows: Data Cleaning & Preprocessing

## 📖 Project Overview

This project focuses on **cleaning and preprocessing the Medical Appointment No-Shows dataset** from Kaggle. The dataset contains information about patients, their appointments, and whether they showed up. The main objective is to transform the raw data into a clean, analysis-ready dataset suitable for **data analysis, visualization, or modeling**.

---

## 🧹 Steps Performed

### 1. Data Loading
- Imported dataset using `pandas`.
- Displayed initial dataset structure, data types, and sample records.

### 2. Initial Cleaning
- Removed duplicate rows based on `PatientId` and `AppointmentID`.
- Standardized text columns (`Gender`, `Neighbourhood`, `No-show`) as categorical types.
- Converted `DateOfBirth`, `ScheduledDay`, and `AppointmentDay` to datetime objects.
- Ensured numeric columns (`Age`, `WaitingDays`, etc.) have correct integer type.

### 3. Handling Missing and Invalid Values
- Checked for missing values in all columns.
- Removed or corrected invalid entries (e.g., negative ages or waiting days).

### 4. Outlier Detection & Treatment
- Detected outliers using **IQR method** for `Age` and `WaitingDays`.
- **Age**: capped values between 0 and 100.
- **WaitingDays**: capped between 0 and 180 days (or dynamically based on IQR).
- Verified no remaining outliers post-treatment.

### 5. Final Verification
- Checked for missing values and duplicates.
- Generated summary statistics for numeric columns.
- Verified categorical columns are consistent.

### 6. Saving the Cleaned Dataset
- Saved final cleaned dataset as:
  `Medical_Appointment_NoShows_Cleaned_Final_Verified.csv`
- Ready for download and downstream analysis.

---

## 🛠️ Tools & Libraries
- Python 3.x
- Pandas
- NumPy
- Matplotlib & Seaborn (optional, for visualization)
- Google Colab (for execution and file download)

---

## 📂 Dataset
- **Source:** [Kaggle - Medical Appointment No-Shows](https://www.kaggle.com/datasets/joniarroba/noshowappointments)
- **Original Columns Include:**
  - `PatientId`, `AppointmentID`, `Gender`, `ScheduledDay`, `AppointmentDay`, `Age`, `Neighbourhood`, `Scholarship`, `Hipertension`, `Diabetes`, `Alcoholism`, `Handcap`, `SMS_received`, `No-show`

---

## ✅ Key Outcomes
- Fully cleaned and verified dataset.
- No missing values or duplicates.
- Outliers in `Age` and `WaitingDays` handled appropriately.
- Columns have correct **data types** for analysis or modeling.
- Dataset is ready for **data analysis, visualization, or predictive modeling**.

---

## ⚡ Usage
1. Clone the repository.
2. Load the cleaned dataset:

```python
import pandas as pd

df = pd.read_csv('Medical_Appointment_NoShows_Cleaned_Final_Verified.csv')
