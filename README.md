# 🛍️ Customer Segmentation & Behavioral Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Internship](https://img.shields.io/badge/Internship-Elevvo-purple)

## 📌 Project Overview
In the competitive retail landscape, understanding customer behavior is crucial for targeted marketing. This project analyzes the **Mall Customers Dataset** to uncover hidden patterns in shopping habits. 

Moving beyond simple analysis, this project employs a **multi-layered approach**:
1.  **Exploratory Data Analysis (EDA):** To diagnose data health and visualize distributions.
2.  **Heuristic Segmentation:** Applying business logic (median splits) to create baseline segments before modeling.
3.  **Unsupervised Machine Learning:** Using **K-Means Clustering** to scientifically group customers and **DBSCAN** to detect anomalies/outliers.

---

## 📂 Dataset
The dataset contains transactional data of mall customers.
- **Source:** [Kaggle - Mall Customer Segmentation Data](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial-in-python)
- **Attributes:**
    - `CustomerID`: Unique ID.
    - `Gender`: Male/Female.
    - `Age`: Customer's age.
    - `Annual Income (k$)`: Annual income in thousands of dollars.
    - `Spending Score (1-100)`: Score assigned by the mall based on customer behavior and spending nature.

---

## ⚙️ Methodology

### 1. Data Preprocessing & Engineering
- **Cleaning:** Checked for missing values and duplicates.
- **Feature Engineering:** Created categorical bins for Age (`Young`, `Adult`, `Senior`) and Income (`Low`, `Average`, `High`).
- **Scaling:** Applied `StandardScaler` to normalize Income and Spending Score for accurate distance calculations.

### 2. Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Distribution of demographics.
- **Bivariate Analysis:** Investigated the "Spending Cliff" (spending drops significantly after age 40).
- **Correlation Matrix:** Analyzed relationships between variables.

### 3. Heuristic Segmentation (Manual Logic)
Before applying ML, I implemented a logical segmentation based on median splits, dividing customers into 4 quadrants:
- **Target:** High Income, High Spend.
- **Savers:** High Income, Low Spend.
- **Careless:** Low Income, High Spend.
- **Conservative:** Low Income, Low Spend.

### 4. Machine Learning Models
#### A. K-Means Clustering (The Core)
- **Optimal K:** Determined using the **Elbow Method** and **Silhouette Analysis**.
- **Result:** $K=5$ clusters provided the best separation.
- **Profiling:** Clusters were analyzed and labeled with business terms (e.g., "VIP", "Average").

#### B. DBSCAN (Anomaly Detection)
- Used Density-Based Spatial Clustering to identify **Outliers** (Noise) that do not fit into standard clusters.
- **Result:** Detected unique/anomalous behavior patterns that K-Means forced into other groups.

---

## 📊 Key Results (The 5 Tribes)

Based on K-Means Clustering, we identified 5 distinct customer profiles:

| Cluster Name | Description | Strategy Suggestion |
| :--- | :--- | :--- |
| **VIP (High Income, High Spend)** | The most valuable segment. | Exclusive offers, loyalty programs, VIP events. |
| **Savers (High Income, Low Spend)** | Wealthy but cautious. | Quality-focused marketing, "Value for Money" campaigns. |
| **Careless (Low Income, High Spend)** | Younger, aspirational shoppers. | Impulse buy promotions, installment plans, trend-focused ads. |
| **Conservative (Low Income, Low Spend)** | Strict budgeters. | Discount coupons, clearance sales. |
| **Average (Middle Class)** | Moderate income and spend. | Standard promotions, bundle offers. |

---

## 🛠️ Technologies Used
- **Language:** Python
- **Libraries:**
    - `Pandas` & `NumPy` (Data Manipulation)
    - `Matplotlib` & `Seaborn` (Visualization & Custom Aesthetics)
    - `Scikit-Learn` (K-Means, DBSCAN, StandardScaler)
    - `Yellowbrick` (Cluster Visualization)

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/YourUsername/Customer-Segmentation.git](https://github.com/YourUsername/Customer-Segmentation.git)
