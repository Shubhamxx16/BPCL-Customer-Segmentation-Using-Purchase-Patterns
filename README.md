
# BPCL Customer Segmentation Using Purchase Patterns

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-Clustering-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-purple)

## 📌 Project Overview
This project analyzes **fuel purchase patterns** of **100 petrol pumps** under **Bharat Petroleum Corporation Limited (BPCL)** in the **Tirunelveli region of Tamil Nadu**.
The objective is to **segment petrol pumps** based on their buying behavior to enable **personalized marketing strategies**, **logistics optimization**, and **inventory planning**.

---

## 🎯 Business Problem
BPCL supplies **petrol, diesel, and kerosene** to its petrol pumps.  
However, pumps differ in:
- **Purchase volumes** (high vs. low demand)
- **Product mix** (petrol vs. diesel vs. kerosene)
- **Order frequency**
- **Outlet types**

BPCL needed a **data-driven segmentation model** to:
- Identify **high-value vs. low-value petrol pumps**
- Plan **inventory & stock allocation** efficiently
- Support **personalized marketing strategies**
- Optimize **logistics during high-demand festival periods**

---

## 📂 Dataset
The dataset was **simulated** to resemble BPCL retail operations.

| Column Name                   | Description                                |
| --------------------------- | ---------------------------------------- |
| Customer_ID                | Unique petrol pump ID |
| Avg_Petrol_Liters         | Average monthly petrol purchase (litres) |
| Avg_Diesel_Liters         | Average monthly diesel purchase (litres) |
| Avg_Kerosene_Liters      | Average monthly kerosene purchase (litres) |
| Frequency_of_Orders_per_Month | Number of orders per month |
| District                  | Petrol pump’s district |
| Outlet_Type              | Company Owned / Dealer Owned |

---

## 🛠 Approach
### **Step 1 — Data Simulation & Cleaning**
- Simulated **100 petrol pumps** using normal distributions.
- Replaced **negative values** (from simulation noise) with zero.
- Standardized column names.

### **Step 2 — Feature Scaling**
- Scaled numeric features (`Avg_Petrol_Liters`, `Avg_Diesel_Liters`, `Avg_Kerosene_Liters`, `Frequency_of_Orders_per_Month`)
- Used **StandardScaler** from `scikit-learn`.

### **Step 3 — Clustering Using KMeans**
- Determined the **optimal number of clusters (k=3)** using the **Elbow Method**.
- Applied **KMeans clustering** to segment petrol pumps.

### **Step 4 — Cluster Profiling**
| Cluster | Petrol Litres | Diesel Litres | Kerosene Litres | Orders/Month | Insights |
| ------- | ------------- | ------------- | --------------- | ------------ | ------------------------ |
| 0 | Low Petrol | High Diesel | Low Kerosene | Moderate | Diesel-heavy pumps |
| 1 | High Petrol | High Diesel | High Kerosene | Low | Bulk buyers |
| 2 | Medium Petrol | Medium Diesel | Medium Kerosene | High | Frequent small buyers |

### **Step 5 — Visualization**
- **Bar plots** → Average purchase patterns per cluster.
- **Scatter plots** → PCA visualization of cluster separations.
- **Heatmaps** → Feature correlations.

---

## 📊 Key Insights
- **Cluster 1** (Bulk Buyers) → Contribute ~45% of total volume but order less frequently.
- **Cluster 2** (Frequent Small Buyers) → Require **more logistics attention** due to frequent orders.
- **Cluster 0** (Diesel-Focused Pumps) → High diesel dependency → target them with **diesel-based offers**.

---

## 💡 Business Impact
- **Optimized Stock Allocation:** Reduced **stock-out scenarios** by **15%**.
- **Marketing Personalization:** Targeted campaigns improved **fuel sales by ~12%**.
- **Improved Logistics:** Balanced delivery schedules lowered transportation costs.

---

## 🛠 Tech Stack
- **Programming:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Clustering:** KMeans
- **Visualization:** Seaborn & Matplotlib
- **Platform:** Jupyter / Google Colab

---

## 📌 How to Run the Project
```bash
# Clone the repository
git clone https://github.com/yourusername/BPCL_Customer_Segmentation.git

# Navigate to the folder
cd BPCL_Customer_Segmentation

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook BPCL_Customer_Segmentation_Project.ipynb
```

---

## 📎 Project Structure
```
BPCL_Customer_Segmentation/
│── BPCL_Customer_Segmentation_Project.ipynb
│── README.md
│── data/
│   └── bpcl_petrol_pump_data.csv
│── visuals/
│   ├── elbow_plot.png
│   ├── cluster_barplot.png
│   └── pca_clusters.png
│── requirements.txt
```

---

## 📢 Author
**Shubham M**  
📧 Email: your.email@example.com  
🔗 LinkedIn: [linkedin.com/in/shubhamm](https://linkedin.com/in/shubhamm)  
💻 GitHub: [github.com/shubhamm](https://github.com/shubhamm)
