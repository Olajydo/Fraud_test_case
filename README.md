# **Fraud Detection in Hotel Bookings**  

In this project, we developed a fraud detection model to predict whether a booking is fraudulent or legitimate. Our objective was to design a system that could accurately detect fraudulent transactions using historical booking data. Below is a step-by-step breakdown of our approach:  

### **1. Data Preprocessing**  
- Cleaned the dataset by handling missing values and ensuring variables were in the correct format.  
- Encoded categorical variables and scaled numerical features to improve model performance.  

### **2. Feature Engineering**  
- Extracted new features such as booking frequency, transaction amounts, and time-related variables.  
- These engineered features helped in identifying patterns that indicate fraudulent behavior.  

### **3. Handling Class Imbalance**  
- Fraudulent bookings were significantly fewer than legitimate ones.  
- To address this imbalance, we applied **SMOTE (Synthetic Minority Over-sampling Technique)** to generate synthetic instances of fraudulent bookings, ensuring the model learned to detect fraud without bias.  

### **4. Feature Selection (Random Forest)**  
- Used **Random Forest** to determine feature importance, helping us identify the most predictive variables.  
- Key fraud indicators included high-value bookings, bookings made with temporary email addresses, and irregular booking behaviors.  

### **5. Model Training (XGBoost)**  
- Implemented **XGBoost**, a powerful gradient boosting algorithm, for classification.  
- Fine-tuned hyperparameters using cross-validation to optimize accuracy and ensure generalization to new data.  

### **6. Model Evaluation**  
- Evaluated performance using **Precision, Recall, F1-score, and ROC-AUC** to balance fraud detection while minimizing false positives.  
- The model achieved strong predictive power in detecting fraudulent transactions.  

### **7. Model Insights**  
The model provided critical insights into fraud trends, revealing patterns that fraudsters often exploit:  
- High-value bookings had a significantly higher fraud risk, as fraudsters tend to target expensive transactions.  
- Fraudsters might impersonate certain age groups to avoid detection. While younger users initially appeared more likely to engage in fraudulent bookings, further analysis suggests that fraudsters may deliberately **choose an age group that is perceived as more trustworthy** (e.g., middle-aged or older users) to bypass security checks.  
- Disposable email addresses were frequently used in fraudulent attempts, likely to avoid detection and enable repeated offenses without being traced.  


### **8. Interactive Confusion Matrix**  
To visualize model performance, we created an **interactive confusion matrix** using Plotly,
his visualization helps us analyze **true positives, false positives, and false negatives**, making it easier to interpret our model’s predictions.  

### **Conclusion**  
By following this structured approach, we successfully built a **highly effective fraud detection model** that not only predicts fraudulent bookings accurately but also provides valuable insights into fraudulent behaviors. The combination of **Random Forest for feature selection and XGBoost for classification** allowed us to develop a **robust fraud detection system**, helping businesses minimize financial losses and improve security.  
