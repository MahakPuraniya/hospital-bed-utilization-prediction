# 📊 Hospital Bed and Resource Prediction
Hospitals often struggle with inefficient bed utilization, leading to overcrowding, delayed admissions, or underused resources. 
Understanding utilization patterns is critical for capacity planning and operational efficiency.
This project helps healthcare administrators explore hospital bed utilization and staffing shortages under various conditions.
The dashboard is built with Streamlit, providing real-time data views and scenario-based forecasts to support resource planning and preparedness.

## Objective
- Analyze historical hospital bed utilization data
- Identify trends and peak demand periods
- Build a predictive model to forecast bed occupancy

## Dataset
The dataset contains hospital-level bed utilization information including total beds, occupied beds, admissions, and discharges.
Due to data privacy and size, a sample dataset is included for demonstration purposes.

## 🔍 Features
- **Overview section:** Trends on bed usage, COVID admissions (by age and state), staffing issues, and hospital pressure
- **Inpatient Bed Utilization:** Current and predicted state-level bed usage (1–8 week forecast)  
- **Staffing Shortage Status:** Current and future staffing shortage % visualization by state (1–8 week forecast) 
- **Scenario Planning Module:** Simulate changes in season, admission rate, staff shortage, and bed capacity  

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn

## Approach
1. Data cleaning and preprocessing
2. Exploratory data analysis to identify trends
3. Feature engineering
4. Model development and evaluation
   
## 💡 Notes
- Forecast limitations clarified based on COVID-period training data, as a result, changes in everyday conditions like season or admission rate may have limited impact.  
- The application runs in **real-time computation** for faster results.  
- Model `.pkl` files are included for scalability but not currently used due to improved performance with live calculations.  
- For larger datasets in the future, pre-trained models can be re-integrated.

## Key Insights
- Bed occupancy showed clear daily and weekly patterns
- Emergency admissions were a major driver of utilization spikes
- Certain bed types consistently operated near capacity

## Results
The model provided actionable insights that could help hospitals improve capacity planning and reduce bottlenecks during peak demand.

## Evaluation & Future Improvements
# Evaluation
- Current evaluation is based on model accuracy for state-level predictions.
- Real-time adjustments are limited due to COVID-period trained data.

# Future Improvements
- Integrate live hospital bed usage data for more accurate predictions.
- Expand staffing predictions to include role-specific shortages.
- Enhance scenario planning with multi-variable adjustments.

## 🚀 How to Run
1. **Navigate to the project directory**
cd Group4

2. **Install dependencies**
pip install -r requirements.txt

3. **Launch the app**
streamlit run Hospital_UI_Group4.py


