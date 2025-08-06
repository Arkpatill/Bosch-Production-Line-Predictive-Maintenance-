<h1 style="font-size:40px;"> Predictive Maintenance for Bosch Production Line using Modern Technologies</h1>

## **Introduction**
This project leverages **Machine Learning (ML)**, **Deep Learning (DL)**, and **Power BI** to **predict failures** in Bosch production line machinery before they occur.  
By analyzing telemetry, maintenance, error, and failure data, the system proactively identifies potential breakdowns, **reduces unplanned downtime**, and **optimizes maintenance schedules**.

---

## **Problem Statement**
In today’s business world, **downtimes and errors** can have a huge impact — causing **financial losses**, **reputation damage**, and **market flow disruptions**.  
This project addresses these challenges with **predictive analytics** and **real-time monitoring**.

---

## **Dataset**
- **Source:** Public Bosch Production Line dataset  
- **Data Includes:**  
  - **Telemetry data:** pressure, rotation, vibration, voltage  
  - **Failure logs:** component-level failures  
  - **Maintenance logs:** replacement history  
  - **Error logs:** timestamps and error IDs  
- **Scope:** 4 machine models, each tagged with a **production line number**  

---

## **Tech Stack**
- **Languages & Libraries:** Python, NumPy, Pandas, Matplotlib, Seaborn, TensorFlow  
- **Visualization:** Power BI  
- **Deployment:** Flask/Django API on AWS / GCP / Azure  

---

## **Methodology**
### **1. Data Preprocessing & Cleaning**
- Missing value handling  
- Feature engineering from telemetry & failure data  
- Data normalization & scaling  

### **2. Model Development**
- **Deep Learning Models:**  
  - LSTM for sequential time-series prediction  
  - Dense Sequential networks for classification  

### **3. Evaluation**
- **Metrics:** ROC Curve, AUC Score, Model Accuracy  

### **4. Visualization**
- Interactive **Power BI dashboards** for:  
  - Failure analysis  
  - Vibration covariance  
  - Time-series failure trends  
  - Component-level breakdowns  

### **5. Deployment**
- Hosted on **Flask/Django API**, integrated with cloud infrastructure for **real-time predictions**  

---

## **Results**
- **ROC Curve:** Achieved an AUC of *0.75*  
- **Decisions & Insights:**  
  1. **Vibration–Failure Link:** Machines with sustained vibration above ~76 units show a higher probability of imminent failure — proactive maintenance should be scheduled in such cases.  
  2. **Model Reliability:** Model 3 exhibits the highest failure and error count; prioritizing inspections and redesign for this model can reduce downtime significantly.  
  3. **Component Vulnerability:** Failures are concentrated in specific components (comp1–comp4) with identifiable time-series patterns — staggered maintenance schedules can preempt peak failure months.  
  4. **Operational Age Impact:** Older machines (average age ~12 years) demonstrate a higher variance in failure rate; targeted replacements or overhauls can improve overall production line stability.  
- **Dashboard:** Delivered real-time, interactive insights into production health, including failure vs. error distribution, time-series patterns, vibration covariance, and component-level analysis.

---



## **Visuals**

![ROC Curve](ROC%20Curve%20.png)  
![Confusion Matrix](Confusion%20Matrix%20.png)  
 
![Facts and Dimmension Table](Facts%20and%20Dimmension%20Table%20.png)  

![Failure Vs Error](Failure%20Vs%20Error%20.png)  
![Interactive Features Understanding](Interactive%20Features%20Understanding%20.png)  

![Time-Series Failure Analysis](Time-Series%20Failure%20Analysis%20.png)  

## How to Run

### 1. Clone Repository
```bash
git clone https://github.com/Arkpatill/Bosch-Production-Line-Predictive-Maintenance-.git







---


