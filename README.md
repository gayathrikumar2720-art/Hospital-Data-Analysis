# Hospital Data Dashboard (Power BI)

An interactive **Power BI dashboard** that analyses hospital data to show patient admissions, department performance, and billing trends.

## **Project Overview**

| Detail | Information |
|---|---|
| Tool | Microsoft Power BI Desktop |
| Dataset | `hospital_data.csv` |
| Data type | Anonymized / dummy data (no real patient details) |
| Goal | Help hospital management understand patients and revenue |

## **Key Features**

- KPI cards: Total Patients, Total Revenue, Average Stay, Average Bill
- Patients by department (bar chart)
- Monthly admission trend (line chart)
- Gender and age group split (pie / donut chart)
- Slicers to filter by department, gender, and date

## **Steps Followed**

| Step | Work done |
|---|---|
| 1. Import | Loaded the CSV into Power BI |
| 2. Clean | Used Power Query to fix data types, remove duplicates and handle blanks |
| 3. Model | Created a date column and calculated fields |
| 4. Measures | Wrote DAX measures |
| 5. Visualise | Built charts and the dashboard layout |

## **Sample DAX Measures**

```dax
Total Patients = COUNT(hospital_data[patient_id])

Total Revenue = SUM(hospital_data[bill_amount])

Average Bill = AVERAGE(hospital_data[bill_amount])

Avg Stay Days =
AVERAGEX(
    hospital_data,
    DATEDIFF(hospital_data[admission_date], hospital_data[discharge_date], DAY)
)
```

## **Dashboard Preview**

![Dashboard](images/dashboard.png)

## **Key Insights**

*(Fill this in after finishing your dashboard.)*

- [Example: Cardiology has the highest number of patients]
- [Example: Revenue is highest in March]

## **Folder Structure**

```
hospital-powerbi-project/
├── data/          → hospital_data.csv
├── dashboard/     → hospital_dashboard.pbix
├── images/        → dashboard.png
└── README.md
```

## **Author**

**Gayathri**
Aspiring Data Analyst | Power BI | SQL | Python
