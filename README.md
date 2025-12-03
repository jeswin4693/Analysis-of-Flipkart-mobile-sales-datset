# Analysis-of-Flipkart-mobile-sales-datset

# 📱 Flipkart Mobile Phones Dataset – Analysis & Insights

A complete data cleaning + EDA project

## 📝 **Project Overview**

This project focuses on analyzing a dataset of **mobile phones listed on Flipkart**, one of India's largest online marketplaces.
The goal is **NOT** to build machine learning models but to:

* Understand the dataset in depth
* Clean and preprocess the data
* Perform **descriptive statistics**
* Explore the data through **interactive visualizations**
* Discover meaningful insights
* Create a foundation for dashboard-style analysis

This project is ideal for **beginners in data analytics**, showcasing a real-world retail dataset with price, rating, discount, brand, and storage parameters.

---

# 📁 **Dataset Description**

### **Total Rows:** 3006

### **Total Columns:** 12

### **Missing Values:** 0 (after cleaning)

The dataset contains mobile phone listings scraped from Flipkart.
It includes brand-level, price-level, hardware-level, and discount-based information.

---

## 🔍 **Column-by-Column Explanation (Human-Friendly)**

### **1. `brand`**

* Type: *object*
* Example: `"Samsung"`, `"Apple"`
* Meaning: Brand/manufacturer of the mobile.

### **2. `model`**

* Type: *object*
* Example: `"iPhone 13"`, `"Galaxy M34"`
* Meaning: Model name of the phone listed.

### **3. `color`**

* Type: *object*
* Example: `"Black"`, `"Blue"`, `"Starlight"`
* Meaning: Color variant of the mobile phone.

### **4. `rating`**

* Type: *float*
* Range: 1.0 – 5.0
* Meaning: Average customer rating given on Flipkart.

### **5. `selling_price`**

* Type: *int*
* Example: `12999`, `74999`
* Meaning: The price at which the mobile is currently sold.

### **6. `original_price`**

* Type: *int*
* Example: `15999`, `89999`
* Meaning: The real MRP before discount.

### **7. `ram_gb`**

* Type: *float*
* Example: `4`, `6`, `8`, `12`
* Meaning: RAM capacity of the mobile (in GB).

### **8. `storage_gb`**

* Type: *float*
* Example: `64`, `128`, `256`
* Meaning: Internal storage capacity (in GB).

### **9. `discount_amt`**

* Type: *int*
* Meaning: Monetary discount amount = original_price – selling_price.

### **10. `discount_pct`**

* Type: *float (rounded)*
* Meaning: Percentage discount:
  [
  discount_pct = \frac{discount_amt}{original_price} \times 100
  ]

### **11. `price_per_storage_gb`**

* Type: *float*
* Meaning:
  [
  \text{price per GB of storage} = \frac{selling_price}{storage_gb}
  ]
  Helps compare phones based on value-for-storage.

### **12. `full_name`**

* Type: *object*
* Meaning: Full combined product name (brand + model + variant).

---

# 🧼 **Data Cleaning Summary**

### ✔ Removed duplicate or unnecessary columns

* Dropped: `clean_color` (same as `color`)

### ✔ Fixed inconsistent data types

* Converted RAM, storage, ratings, price fields to numeric formats.

### ✔ Derived new useful columns

* `discount_amt`
* `discount_pct` (rounded)
* `price_per_storage_gb`
* `price_segment` (Budget / Mid-range / Flagship)

### ✔ Handled missing values

* No missing values remain.

---

# 📊 **Descriptive Statistics Summary**

### **Overall Statistics**

* **Average Selling Price:** ₹22,000–₹25,000
* **Average Rating:** ~4.1
* **Average Discount:** ~20–30%
* **RAM Range:** 2GB – 16GB
* **Storage Range:** 32GB – 512GB

### **Brand-Level Insights**

* Samsung, Redmi, Poco, Realme dominate the listings
* Apple has fewer models but highest price range
* Budget phones most common in the dataset

### **Price Segment Distribution**

* **Budget (<10K)** → High volume
* **Mid-range (10K–30K)** → Majority of devices
* **Flagship (>30K)** → Premium brands

---

# 📈 **Visualizations Included**

### **1. Scatter Plots**

* Price vs Rating (colored by Brand)
* RAM vs Price
* Storage vs Price

### **2. Bar Plots**

* Count of phones per brand
* Avg. rating per brand
* Total discount per brand

### **3. Box Plots**

* Price distribution per brand
* Rating distribution per brand

### **4. Distribution Plots**

* Price distribution
* Ratings histogram
* RAM/Storage distributions

### **5. Sunburst Chart (Hierarchical)**

* Brand → Price Segment → Model

### **6. Correlation Heatmap**

* Visualizing relationships among numeric columns.

---

# 🔍 **Key Insights Extracted**

* Budget phones cluster around **₹8,000–₹12,000** with ratings between **3.8–4.2**.
* Apple and Samsung dominate the top price range.
* Poco, Redmi, and Realme provide **best price-to-spec value**.
* Storage and RAM have a **strong positive correlation** with price.
* Higher discount % often occurs in mid-range phones.

---

# 🛠️ **Technologies Used**

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib / Seaborn**
* **Plotly Express** (for interactive visuals)
* **Jupyter Notebook**

---

# ▶️ **How To Run This Notebook**

1. Install the dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn plotly
   ```

2. Open Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

3. Load the notebook file:

   ```
   flipkart.ipynb
   ```

4. Run cells in sequential order.

---

# 🚀 **Future Improvements**

* Add Power BI / Tableau dashboards
* Compare across other e-commerce datasets (Amazon vs Flipkart)
* Add sentiment analysis from product reviews
* Perform brand-based price trend analysis
* Identify best value-for-money phones using weighted metrics


