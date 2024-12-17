# A/B Testing and Regression Analysis -  Ad Campaign Performance Analysis 📊

## Business Problem
As a marketing agency, our objective is to **maximize the return on investment (ROI)** for our clients' advertising campaigns. We conducted two ad campaigns:
1. **Facebook Ads**  
2. **AdWords Ads**

We aim to determine which platform performs better in terms of:
- Clicks  
- Conversions  
- Cost-effectiveness  

The insights will help optimize resource allocation and enhance advertising strategies.

---

## Research Question
**Which ad platform is more effective in terms of conversions, clicks, and overall cost-effectiveness?**

---

## Dataset Description

The dataset contains daily performance metrics for both Facebook and AdWords campaigns throughout **2019**. Key features include:

- **Date**: Campaign date (2019-01-01 to 2019-12-31)  
- **Ad Views**: Number of views on the ads  
- **Ad Clicks**: Number of clicks received on the ads  
- **Ad Conversions**: Number of conversions resulting from the ads  
- **Cost per Ad**: Cost associated with running the ad campaigns  
- **Click-Through Rate (CTR)**  
- **Conversion Rate**  
- **Cost per Click (CPC)**  

---

## Technologies Used

- **Python Libraries**: pandas, numpy, matplotlib, seaborn, scipy, statsmodels, scikit-learn  
- **Tools**: Jupyter Notebook  
- **Statistical Techniques**: Correlation Analysis, Hypothesis Testing, Regression Modeling, Cointegration Test  

---

## Analysis and Insights 

### 1. Distribution of Clicks and Conversions

The distributions of **clicks** and **conversions** show a symmetrical shape, indicating even performance across campaigns.

**Visualization:**
![Facebook and AdWords Clicks/Conversions](https://github.com/MNitin-Reddy/A-B-Testing/blob/main/images/Conversions%20and%20clicks%20distribution.png)

---

### 2. Frequency of Conversions by Categories

We categorized conversions into:
- Less than 6  
- 6–10  
- 10–15  
- More than 15  

**Observations:**
- Facebook had more frequent high-conversion days.
- AdWords lacked days with conversions above 10.  

**Visualization:**
![Conversion Categories](https://github.com/MNitin-Reddy/A-B-Testing/blob/main/images/Frequency%20of%20conversions.png)

---

### 3. Do Clicks Lead to More Conversions?

We analyzed the **correlation** between clicks and conversions for both platforms:

- Facebook: **Strong Positive Correlation** (0.87)  
- AdWords: **Moderate Positive Correlation** (0.45)  

This suggests Facebook is more effective in driving conversions.

**Visualization:**
![Scatterplot Correlation](https://github.com/MNitin-Reddy/A-B-Testing/blob/main/images/Correlation.png)

---

### 4. Monthly Conversions Over Time

Conversions were analyzed across months:

- Mondays and Tuesdays had the highest conversions.  
- Monthly trends showed **increased conversions** over time with minor dips in February, May, and November.

**Visualization:**
![Monthly Conversions](https://github.com/MNitin-Reddy/A-B-Testing/blob/main/images/Monthly%20Conversions.png)

---

### 5. Monthly Cost Per Conversion (CPC)

We analyzed the **Cost Per Conversion** to understand advertising cost-effectiveness:

- **May and November** had the lowest CPC values.  
- February had the **highest CPC**, indicating less cost-effectiveness.

**Visualization:**
![Cost Per Conversion](https://github.com/MNitin-Reddy/A-B-Testing/blob/main/images/CPC.png)

---

### 6. Hypothesis Testing

- **Hypothesis**: Facebook has more conversions than AdWords.  
- **Result**:  
  - Mean Conversions:  
    - Facebook: **11.74**  
    - AdWords: **5.98**  
  - **p-value**: Extremely small (9.35e-134) → Reject the null hypothesis.  

**Conclusion**: Facebook ads generate **significantly more conversions** than AdWords.

---

### 7. Linear Regression: Predicting Conversions from Clicks

We built a Linear Regression model for Facebook ads:

- **R² Score**: 76.35%  
- **Insights**: Predicting Facebook conversions based on clicks helps set realistic goals.  

Example predictions:  
- **For 50 clicks → ~9 conversions**  
- **For 80 clicks → ~14 conversions**

**Visualization:**
![Linear Regression](https://github.com/MNitin-Reddy/A-B-Testing/blob/main/images/Regression%20Analysis.png)

---

### 8. Cointegration Test: Cost and Conversions

A **cointegration test** showed a long-term equilibrium relationship between ad cost and conversions, suggesting stable budget impacts over time.

---

## Recommendations

1. Allocate **more resources to Facebook Ads** due to their higher conversions and stronger ROI.  
2. Optimize AdWords campaigns to improve click-to-conversion performance.  
3. Increase ad spend during months with **lower CPC** (e.g., May, November).  
4. Monitor and analyze performance during **Mondays and Tuesdays** for targeted campaigns.  

---

## Conclusion 

The analysis demonstrates that **Facebook Ads outperform AdWords** in driving conversions. Businesses can leverage these findings to improve ad performance and ROI.

---

## How to Run 📥

1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/ad-campaign-analysis.git
   cd ad-campaign-analysis
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook:  
   ```bash
   jupyter notebook notebooks/ad_campaign_analysis.ipynb
   ```
