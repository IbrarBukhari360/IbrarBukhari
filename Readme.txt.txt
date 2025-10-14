 Pakistan Analysis Dashboard – Power BI Report

 Overview
The Pakistan Analysis v1.0 dashboard provides a complete performance analysis of debt collection and customer contact operations for the Pakistan region.  
It tracks **payments, collector productivity, contact rates, targets, and recovery KPIs** across teams, agents, and banks.

This report is part of the organization's data-driven decision framework, built to monitor and enhance collection efficiency, payment growth, and field performance.

---

 Objectives
- Measure **monthly and year-to-date payments** against targets.
- Evaluate **agent performance** and team-wise contribution.
- Analyze **contactable vs non-contactable accounts** and call quality.
- Track **allocation vs recovery rates**, **field visits**, and **skip trace outcomes**.
- Provide **real-time management insights** with interactive filters and visuals.

---

 Tools & Technologies
- Power BI Desktop**
- Power Query (ETL)**
- DAX (for KPI calculations and trend measures)**
- SQL (for backend data preparation)**
- Excel (supporting datasets and validation)**

---

 Key Insights
 Payments Overview
- Target:** 440K | **Achieved:** 416K  
- Best Month:** 611.98K (Jul 2025)  
- YTD Payments:** 4.43M  
- Growth:** 15.29% YoY

 Team Performance
| Team Lead | Total Payment | % Achieved | Remarks |
| Zohaib Jan | 42.0K | 75% | Above Target |
| Khurram Khokhar | 21.5K | 86% | Slightly Below Target |

Top Collectors
| Agent | Total Payment (YTD) | Rank |
| Jawad Shah | 732K | ⭐ #1 |
| Azeem Ali | 539K | ⭐ #2 |
| Farhan Ahmed | 532K | ⭐ #3 |

Contact Performance
- Contactable CIFs: 1,015 / 13,882 allocations  
- Accounts Worked: 2,825  
- Right Party Contacts: 104  
- Avg Time Spent per CIF: 00:14:08

 Field Visits
- Total Visits: 79 | Completed: 33 (42%)  
- Major Banks: Rak Woff, Deem Finance, Emirates NBD


DAX Measures (Examples)
Some of the key DAX measures used:

 DAX
Payments YTD =
CALCULATE(
    SUM(Payments[payment_amount]),
    DATESYTD('Date'[Date])
)

Target Achieved % =
DIVIDE(
    [Total Payments],
    [Monthly Target],
    0
)

Growth YoY =
DIVIDE(
    [Payments YTD] - [Payments YTD LY],
    [Payments YTD LY],
    0
)
