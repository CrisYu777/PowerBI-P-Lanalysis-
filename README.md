# Casino Gaming Data Analysis with Power BI  
*(Original work from S-Owiti)*  

---

## Purpose  
The purpose of this project is to analyze gambling behaviors and identify trends using Power BI. It demonstrates the ability to manage and visualize data effectively to support **responsible gambling practices**, ensuring well-informed, data-driven decision-making.  

---

## Key Features  
- **Data-Driven Insights**: Enables monthly, quarterly, and annual reporting to internal stakeholders and external regulators.  
- **Trend Analysis**: Identifies patterns in gambling behavior to assist in developing responsible gambling initiatives.  
- **Data Visualization**: Utilizes Power BI to provide clear, actionable visual insights for business improvement.  

---

## Data Sources  
This analysis is based on three key tables:  

1. **Players Table**  
   - **Columns**: `FiscalYear`, `MonthEnding`, `Wagers`, `PromotionalCoupons`, `CancelledWagers`  

2. **Revenue Table**  
   - **Columns**: `FiscalYear`, `MonthEnding`, `OnlineCasinoGamingWinLoss`, `PatronWinnings`, `TotalGrossGamingRevenue`  

3. **Deductions Table**  
   - **Columns**: `FiscalYear`, `MonthEnding`, `Payments`, `PromotionalDeduction`  

---

## Data Model  
- **Players Table (1)** to **Revenue Table (M)**: Linked by `FiscalYear`.  
- **Players Table (1)** to **Deductions Table (M)**: Linked by `MonthEnding`.  
- **Revenue Table (1)** to **Deductions Table (M)**: Linked by `MonthEnding`.  

---

## Key Metrics  

### Total Revenue  
```sql
TotalRevenue = SUM(RevenueTable[TotalGrossGamingRevenue])
```

### Net Revenue  
```sql
NetRevenue = SUM(RevenueTable[TotalGrossGamingRevenue]) - SUM(DeductionsTable[Payments])
```

### Player Activity Trends  
Revenue trends and wager data filtered by player demographics.  

---

## Insights and Visualizations  

### Revenue Trends  
Line charts tracking net revenue over time.  

### Player Behavior Analysis  
Heatmaps and bar charts to analyze peak gambling hours and player activity levels.  

### Deduction Overview  
Gauges and visualizations highlighting promotional deductions and payments affecting profitability.  

---

## Conclusion  
This project highlights the use of Power BI for analyzing and visualizing online casino data. It provides insights that aid in identifying behavioral trends, improving operations, and ensuring compliance with responsible gambling practices. By refining the data and visualizations, the model can adapt to evolving needs, promoting a better understanding of gambling behaviors for stakeholders.
