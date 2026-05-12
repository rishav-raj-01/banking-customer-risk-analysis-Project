# Banking Customer Risk Analysis
A credit risk analysis project built on the Give Me Some Credit dataset from Kaggle. The goal was to explore what borrower characteristics are associated with loan defaults and segment borrowers into risk groups.

### **Dataset**
Give Me Some Credit — Kaggle Competition Dataset
Link: https://www.kaggle.com/competitions/GiveMeSomeCredit/data


### **What I did**

* Cleaned the dataset — handled missing values in MonthlyIncome and NumberOfDependents, removed invalid ages, capped revolving utilization outliers, and replaced sentinel values (96/98) in past-due columns
* Engineered new features like TotalDelinquencies, IncomePerDependent, and a FICO-inspired credit score proxy scaled to the 300–850 range
* Explored key risk drivers through visualizations — age bands, utilization tiers, income quartiles, delinquency counts
* Built a correlation heatmap to see which features are most related to default
* Created a simple rule-based borrower segmentation: Premium, Standard, Marginal, Watch List, and Subprime
* Generated a risk matrix showing default rates across Risk Tier × Credit Utilization combinations


### **Key Findings**

* Delinquency history is the strongest signal — even one 30-day late payment noticeably increases default probability. Borrowers with 3+ events show 40–70% default rates vs the 6.7% baseline.
* Credit utilization above 80% is a red flag — borrowers in this range default at 3–5x the portfolio average.
* Younger borrowers (18–35) carry higher risk — likely due to shorter credit history and less income stability, not bad intent.
* Score < 580 + Utilization > 80% is a danger zone — this combination produces very high default rates relative to the rest of the portfolio.
* Income alone is a weak predictor — high earners with high debt obligations can be just as risky as low-income borrowers. DTI is more informative.


### **Tech Stack**

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* SciPy

Rishav Raj
