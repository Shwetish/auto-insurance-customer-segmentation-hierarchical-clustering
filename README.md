# auto-insurance-customer-segmentation-hierarchical-clustering
Customer segmentation and risk profiling for auto insurance policyholders (Autoinsurance.csv) using hierarchical clustering on mixed-type encoded data.
# Auto Insurance Customer Segmentation using Hierarchical Clustering

## 1. Business Problem
### 1.1. Business Objective
To analyze auto insurance policyholder details (`Autoinsurance.csv`), combining demographic, coverage, and claim history data using hierarchical clustering. This enables insurance companies to create customized risk tiers and personalized insurance bundles.
### 1.2. Constraints
* Dataset contains mixed data types (categorical policy types and continuous claim amounts), requiring rigorous preprocessing.
* Outliers in claim payouts need handling to prevent distortion.

## 2. Data Dictionary
*(Note: Tailor based on dataset features)*
| Feature Name | Data Type | Description |
| --- | --- | --- |
| `Customer` | String | Customer ID / Policy number |
| `State` | Categorical | State of residence |
| `Customer Lifetime Value` | Numerical | Projected revenue from the customer |
| `Response` | Categorical | Customer response to marketing campaigns |
| `Coverage` | Categorical | Type of insurance coverage (Basic, Extended, Premium) |
| `EmploymentStatus` | Categorical | Employment status of the policyholder |
| `Monthly Premium Auto` | Numerical | Monthly auto insurance premium amount |
| `Total Claim Amount` | Numerical | Total claim payout amount |

## 3. Data Pre-processing
* **Data Cleaning:** Checked for duplicates, missing values, and corrected data types.
* **Encoding:** Converted categorical attributes (like `Coverage`, `EmploymentStatus`, and `State`) into numeric columns using dummy variables or label encoding.
* **Normalization:** Applied standard scaling on numerical features (`Monthly Premium Auto`, `Total Claim Amount`, `Customer Lifetime Value`).

## 4. Exploratory Data Analysis (EDA)
* **Summary:** Distribution of customer lifetime values and claim amounts.
* **Univariate Analysis:** Count plots for coverage levels and histograms for premium amounts.
* **Bivariate Analysis:** Scatter plots exploring relationship between monthly premiums and total claim amounts across customer segments.

## 5. Model Building
* **5.1 Scaled Data:** Constructed hierarchical clustering models experimenting with different linkage methods (Ward and Complete).
* **5.2 Dendrogram:** Visualized agglomerative hierarchical trees using dendrograms.
* **5.3 Validation & Insights:** Extracted cluster labels to profile distinct customer tiers (e.g., "Low-Risk Premium Customers" vs. "High-Claim Frequency Policyholders").

## 6. Business Benefits & Impact
* Smarter risk assessment and dynamic pricing models based on verified customer clusters.
* Enhanced cross-selling and up-selling strategies for high-value policyholders.
