# 📊 Hospital Bed and Resource Prediction

**UIC 2025 Spring MSBA Capstone Project - Group4**  

This project helps healthcare administrators explore hospital bed utilization and staffing shortages under various conditions.
The dashboard is built with Streamlit, providing real-time data views and scenario-based forecasts to support resource planning and preparedness.

---

## 🗂️ File Structure
Group4/
├── Code/                      
│   ├── Final Capstone Project Code File.ipynb     # EDA, model training, data preprocessing, and evaluation
│   └── Hospital_UI_Group4.py                      # Main Streamlit application for the interactive dashboard
├── Models/                                        # Pre-trained models, not used in the current UI. The folder is kept for potential scalability.
│   ├── scenario_xgb_model.pkl
│   ├── scenario_state_encoder.pkl
│   └── scenario_staff_model.pkl
├── Data/                                          # Dataset used for analysis and predictions
│   └── COVID-19_Reported_Patient_Impact_and_Hospital_Capacity_by_State_Timeseries__RAW__20250220.csv
├── screenshots/                                   # UI Screenshots for documentation and reference
│   ├── 0-Group4-project-title.png
│   ├── 1-Navigation.png
│   ├── 2-Hospital Bed Utilization Over Time.png
│   ├── 3-Top 10 States by COVID-19 Admissions.png
│   ├── 4-Average Daily COVID-19 Admissions by Age Group.png
│   ├── 5-Top 10 States by Staffing Shortages.png
│   ├── 6-Hospital Burden & Staffing Crisis Breakdown.png
│   ├── 7-Current State-wise Average Bed Utilization.png
│   ├── 8-Predicted State-wise Bed Utilization (Interactive).png
│   ├── 9-Current State-wise Average Staff Shortage %.png
│   ├── 10-Predicted Staff Shortage by State (Interactive).png
│   ├── 11-Scenario Planning - Conditions.png
│   ├── 12-Predicted Bed Utilization by Scenario.png
│   └── 13-Predicted Staffing Shortage by Scenario.png
├── requirements.txt                                # List of dependencies required to run the application
└── README.md                                       # Project documentation with setup and usage instructions

---

## 🔍 Features
- **Overview section:** Trends on bed usage, COVID admissions (by age and state), staffing issues, and hospital pressure
- **Inpatient Bed Utilization:** Current and predicted state-level bed usage (1–8 week forecast)  
- **Staffing Shortage Status:** Current and future staffing shortage % visualization by state (1–8 week forecast) 
- **Scenario Planning Module:** Simulate changes in season, admission rate, staff shortage, and bed capacity  

---

## 🚀 How to Run
1. **Navigate to the project directory**
cd Group4

2. **Install dependencies**
pip install -r requirements.txt

3. **Launch the app**
streamlit run Hospital_UI_Group4.py

---

## 💡 Notes
- Forecast limitations clarified based on COVID-period training data, as a result, changes in everyday conditions like season or admission rate may have limited impact.  
- The application runs in **real-time computation** for faster results.  
- Model `.pkl` files are included for scalability but not currently used due to improved performance with live calculations.  
- For larger datasets in the future, pre-trained models can be re-integrated.

---

## 🖥️ UI Screenshots
Below are some UI snapshots from the live deployment:
![ProjectTitle](./screenshots/0-Group4-project-title.png)
![Nevigation](./screenshots/1-Navigation.png)
![Overview-HospitalBedUtilizationOverTime](./screenshots/2-Hospital Bed Utilization Over Time.png)
![Overview-Top10StatesbyCOVID-19Admissions](./screenshots/3-Top 10 States by COVID-19 Admissions.png)
![Overview-AverageDailyCOVID-19AdmissionsbyAgeGroup](./screenshots/4-Average Daily COVID-19 Admissions by Age Group.png)
![Overview-Top10StatesbyStaffingShortages](./screenshots/5-Top 10 States by Staffing Shortages.png)
![Overview-HospitalBurden&StaffingCrisisBreakdown](./screenshots/6-Hospital Burden & Staffing Crisis Breakdown.png)
![InpatientBedUtilization-CurrentState-wiseAverageBedUtilization](./screenshots/7-Current State-wise Average Bed Utilization.png)
![InpatientBedUtilization-PredictedState-wiseBedUtilization(Interactive)](./screenshots/8-Predicted State-wise Bed Utilization (Interactive).png)
![StaffingShortageStatus-CurrentState-wiseAverageStaffShortage%](./screenshots/9-Current State-wise Average Staff Shortage %.png)
![StaffingShortageStatus-PredictedStaffShortagebyState(Interactive)](./screenshots/10-Predicted Staff Shortage by State (Interactive).png)
![ScenarioPlanning-ScenarioPlanning-Conditions](./screenshots/11-Scenario Planning - Conditionsn.png)
![ScenarioPlanning-PredictedBedUtilizationbyScenario](./screenshots/12-Predicted Bed Utilization by Scenario.png)
![ScenarioPlanning-PredictedStaffingShortagebyScenario](./screenshots/13-Predicted Staffing Shortage by Scenario.png)

---

## Evaluation & Future Improvements
# Evaluation
- Current evaluation is based on model accuracy for state-level predictions.
- Real-time adjustments are limited due to COVID-period trained data.

# Future Improvements
- Integrate live hospital bed usage data for more accurate predictions.
- Expand staffing predictions to include role-specific shortages.
- Enhance scenario planning with multi-variable adjustments.
