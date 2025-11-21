☀ Solar Power Generation Prediction <br>
📌 Project Overview <br>
This project predicts solar power output based on historical environmental and operational data. The goal is to help understand power generation patterns and improve forecasting for energy planning and efficiency.
The project applies regression modeling techniques and includes full data analysis, model building, evaluation, and visualization.<br>

Datasets details: <br>
Column Name and Description<br>
distance-to-solar-noon -> Time difference from the solar noon of the given day<br>
temperature	 -> Ambient temperature at the time of measurement<br>
wind-direction	-> Direction of wind flow in degrees<br>
wind-speed -> 	Instantaneous wind speed<br>
sky-cover	P-> ercentage of sky covered by clouds<br>
visibility	-> Visibility in meters/kilometers<br>
humidity	-> Atmospheric moisture percentage<br>
average-wind-speed-(period)	-> Average wind speed over a given time period<br>
average-pressure-(period)	-> Average pressure recorded over a given time period<br>
power-generated	-> Target variable – solar energy produced<br>

🎯 Objectives

Perform Exploratory Data Analysis (EDA)<br>
Build predictive models to estimate solar power output<br>
Compare multiple regression techniques<br>
Visualize trends and model results<br>
Evaluate performance using regression metrics<br>

🧠 Approach & Methodology<br>

1️⃣ Data Preprocessing <br>
<br>
1) Handling missing values<br>
2) Outlier detection<br>
3) Feature scaling<br>
4) Train-test split<br>
<br>
2️⃣ Exploratory Data Analysis<br>
<br>
1) Distribution plots
2) Trend and time-based analysis
3) Correlation heatmaps
4) Feature importance tracking
<br>
3️⃣ Model Building<br>
<br>
1) Models include:<br>
2) Linear Regression<br>
3) Random Forest Regressor<br>
4) Decision Tree Regressor<br>
5) Gradient Boosting<br>
<br>
<br>
📊 Regression Metrics & Challenges Faced<br>

1️⃣ MAE (Mean Absolute Error)<br>

What it means:<br>
MAE measures the average absolute difference between actual values and predicted values. It tells how much, on average, the model is “off” in prediction.<br>

Challenge faced:<br>
During development, MAE increased when the model failed to capture sudden variations in power generation due to unexpected weather changes. The model needed better feature engineering and tuning to reduce this gap.<br>

2️⃣ MSE (Mean Squared Error)<br>

What it means:<br>
MSE squares the error before averaging, giving more weight to large mistakes. If the model makes a few big errors, MSE becomes high.<br>

Challenge faced:<br>
A few extreme outliers in the dataset (e.g., sudden drops in output) caused the MSE to rise significantly. Handling outliers and transforming features helped stabilize the model’s performance.<br>

3️⃣ RMSE (Root Mean Squared Error)<br>

What it means:<br>
RMSE is the square root of MSE and gives errors in the same units as the target variable (power-generated). It is more interpretable and highlights large errors.<br>

Challenge faced:<br>
Initially, RMSE was much higher than MAE, which indicated that some predictions were very far from the real values. Hyperparameter tuning and testing different models were required to minimize these large deviations.<br>

4️⃣ R² Score (Coefficient of Determination)<br>

What it means:<br>
R² measures how much of the variability in the target variable is explained by the model.<br>

1.0 = perfect prediction<br>

0.0 = no predictive power<br>

Challenge faced:<br>
Early models showed lower R² because the model wasn’t capturing non-linear relationships well. Switching to tree-based models (like Random Forest and Gradient Boosting) significantly improved the R² score.<br>

💻 Tech Stack<br>

Languages<br>
1) Python<br>
2) Libraries<br>
3) Pandas<br>
4) NumPy<br>
5) Scikit-learn<br>
6) Seaborn<br>
7) Matplotlib<br>

🚀 How to Run<br>
1️⃣ Clone the repository<br>
git clone https://github.com/Arifkhd/solar-power-prediction<br>

2️⃣ Install dependencies<br>
pip install -r requirements.txt<br>

3️⃣ Run the Streamlit App<br>
streamlit run app.py<br>

4️⃣ Open in Browser<br>

After running the command, Streamlit will automatically open the app in your browser.<br>
If it doesn’t, open the link shown in the terminal (usually http://localhost:8501).<br>
<br>
<br>

📈 Future Enhancements<br>

1) Deploy using Flask, FastAPI, or Streamlit<br>

2) Integrate real-time sensor or weather API data<br>

3) Add automated monitoring and retraining (MLOps)<br>

4) Expand dataset to include seasonal and geographical variations<br>

🤝 Contribution<br>

Open to pull requests and improvements.<br>
Please create an issue for major changes.<br>
