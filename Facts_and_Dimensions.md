## **Facts and Dimensions Overview**

The Bosch Predictive Maintenance dataset is organized in a **star schema** to integrate machine details, telemetry, errors, failures, and maintenance data efficiently.

- **Fact Table:**  
  **PdM_machines** — Contains `machineID` (Primary Key), `model`, and `age`. Acts as the central table connecting to all dimensions.

- **Dimension Tables:**  
  1. **PdM_errors** — Logs errors with `datetime`, `machineID`, and `errorID`.  
  2. **PdM_failures** — Records failures with `datetime`, `machineID`, and `failure` (component failed).  
  3. **PdM_maint** — Tracks maintenance events with `datetime`, `machineID`, and `comp` (component maintained).  
  4. **PdM_telemetry** — Stores telemetry readings (`datetime`, `machineID`, and sensor data like pressure, rotation, vibration, voltage).

- **Relationships:**  
  - `machineID` is the **primary key** in the fact table and a **foreign key** in all dimensions.  
  - **Many-to-One:** All dimension tables link to the fact table.  
  - **Many-to-Many:**  
    - Between `PdM_failures` and `PdM_maint` via `machineID`.  
    - Between `PdM_errors` and `PdM_maint` via `machineID`.

---

![Facts and Dimension Table](Facts%20and%20Dimmension%20Table.png)
