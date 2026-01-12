# 🏠 House Price Prediction using Regression Models

## 📌 Project Overview
The objective of this project is to build a predictive model that estimates house prices based on various structural and amenity-related features such as area, number of bedrooms, bathrooms, furnishing status, air conditioning, and proximity to main roads.  

The dataset presents a key challenge in the form of **strong multicollinearity among features**, making it an ideal case study for applying **regularization techniques** and regression diagnostics.

---

## 🎯 Problem Statement
To predict house prices accurately using regression models while:
- Understanding relationships between features and price
- Handling multicollinearity effectively
- Ensuring model interpretability and generalization

---

## 📂 Dataset Description
The dataset consists of housing attributes including:

- **Numerical Features**
  - Area (sq. ft)
  - Bedrooms
  - Bathrooms
  - Stories
  - Parking

- **Categorical / Binary Features**
  - Furnishing status
  - Air conditioning
  - Main road access
  - Guest room availability
  - Basement availability

### ⚠️ Key Challenges
- Strong multicollinearity between numerical variables
- Mixed data types (numerical + categorical)
- Small dataset size, limiting model complexity

---

## 🔍 Exploratory Data Analysis (EDA)
EDA was performed to understand feature distributions and relationships with house prices.

Key observations:
- House **area** shows a strong positive correlation with price
- **Bathrooms** impact price more than bedrooms
- Furnished houses generally command a premium
- Amenities such as air conditioning and parking add value but with diminishing returns

Visualizations included:
- Distribution plots
- Correlation heatmaps
- Feature vs price analysis

---

## 🛠️ Data Preprocessing & Feature Engineering
Steps performed:
- Handling categorical variables using encoding
- Train–test split performed **before scaling** to avoid data leakage
- Feature scaling using **StandardScaler**
- Preserving feature names post-scaling for interpretability

---

## 📉 Multicollinearity Handling
Multicollinearity was diagnosed using:
- Correlation matrix
- **Variance Inflation Factor (VIF)**

Rather than aggressively dropping features, the project adopts **regularization-based regression models** to mitigate multicollinearity while retaining information.

---

## 🤖 Model Building
The following models were trained and evaluated:

- Linear Regression
- Ridge Regression (L2 regularization)
- Lasso Regression (L1 regularization)
- **ElasticNet Regression (L1 + L2)**
- Random Forest (exploratory comparison)

Evaluation metrics:
- **R² Score**
- **Root Mean Squared Error (RMSE)**

---

## 🏆 Final Model Selection
**ElasticNet Regression** was selected as the final model because:
- It effectively handles multicollinearity
- Provides stable coefficients
- Balances feature selection (L1) and coefficient shrinkage (L2)
- Maintains interpretability compared to tree-based models

Random Forest was explored but not selected as the final model due to:
- Limited dataset size
- Reduced interpretability for business insights

---

## 📊 Model Evaluation & Residual Diagnostics
Final evaluation included:
- R² and RMSE comparison
- Residuals vs Predicted plot
- Residual distribution analysis

### Residual Analysis Conclusion:
- Residuals are randomly distributed around zero
- No strong patterns indicating violation of linearity
- Error distribution is approximately normal

This confirms that regression assumptions are reasonably satisfied.

---

## 📈 Feature Coefficient Interpretation
Coefficient analysis from the ElasticNet model revealed:
- **Area** as the strongest driver of house price
- **Bathrooms** contribute more to price than additional bedrooms
- Furnishing and air conditioning add moderate value
- Some features exhibit minimal impact, indicating redundancy

This improves transparency and trust in the model.

---

## 💼 Business Insights
- Buyers prioritize **space** over most amenities
- Adding bathrooms increases property value more effectively than bedrooms
- Furnished homes attract higher prices mainly in premium segments
- Amenities show diminishing returns for smaller homes

These insights can guide pricing strategies and housing development decisions.

---

## ⚠️ Limitations
- Dataset size is limited
- Location information lacks fine-grained granularity
- Temporal market trends are not included
- Linear models may not capture complex non-linear relationships

---

## 🚀 Future Improvements
- Incorporate neighborhood-level location data
- Experiment with polynomial regression
- Apply advanced ensemble models (XGBoost, Gradient Boosting)
- Include economic indicators and time-based features

---

## 🧠 Key Learnings
- Importance of diagnosing and handling multicollinearity
- Regularization improves stability and interpretability
- Model evaluation goes beyond metrics — diagnostics matter
- Translating predictions into business insights is critical

---

## 🧪 Technologies Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## 📬 Author
**Akshay ManjuBai Rathod**  
Aspiring Data Analyst / Data Scientist  
