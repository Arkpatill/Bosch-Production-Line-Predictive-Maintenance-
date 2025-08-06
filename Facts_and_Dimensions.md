## **Facts and Dimensions Overview**

The diagram below represents the **star schema** used in the Bosch Predictive Maintenance dataset.  
It integrates machine information with telemetry, error logs, failures, and maintenance records to enable comprehensive predictive analysis.

### **Fact Table**
- **PdM_machines** *(Primary Key: machineID)*  
  - **machineID** – Unique identifier for each machine.  
  - **model** – Machine model type (e.g., model1, model2, etc.).  
  - **age** – Age of the machine in years.  
  - **Role:** Central fact table linking to all dimension tables.

---

### **Dimension Tables**
1. **PdM_errors**  
   - **datetime** – Timestamp of error occurrence.  
   - **errorID** – Identifier for the specific error type.  
   - **machineID** – Foreign Key linking to `PdM_machines`.  
   - **Relationship:** Many-to-one with `PdM_machines`.

2. **PdM_failures**  
   - **datetime** – Timestamp of failure.  
   - **failure** – Component that failed (comp1–comp4).  
   - **machineID** – Foreign Key linking to `PdM_machines`.  
   - **Relationship:** Many-to-one with `PdM_machines` and many-to-many with `PdM_maint`.

3. **PdM_maint**  
   - **comp** – Component maintained or replaced.  
   - **datetime** – Maintenance timestamp.  
   - **machineID** – Foreign Key linking to `PdM_machines`.  
   - **Relationship:** Many-to-one with `PdM_machines`; many-to-many with `PdM_failures` and `PdM_errors`.

4. **PdM_telemetry**  
   - **datetime** – Timestamp of telemetry reading.  
   - **machineID** – Foreign Key linking to `PdM_machines`.  
   - **pressure, rotate, vibration, volt** – Sensor readings from the machine.  
   - **Relationship:** Many-to-one with `PdM_machines`.

---

### **Relationship Summary**
- `machineID` is the **Primary Key** in the Fact Table and **Foreign Key** in all Dimensions.  
- **Many-to-One:** All dimension tables connect to the Fact Table.  
- **Many-to-Many:**  
  - `PdM_failures` ↔ `PdM_maint` via `machineID`.  
  - `PdM_errors` ↔ `PdM_maint` via `machineID`.

---

![Facts and Dimension Table](Facts%20and%20Dimmension%20Table.png)
