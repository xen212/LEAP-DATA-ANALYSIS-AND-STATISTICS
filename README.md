📌 Project Overview
This repository contains the R scripts, datasets, presentation, and final academic report for the LEAP Data Analysis and Statistics final project.

The objective of this project is to analyze a real-world health dataset comprising 442 individuals to identify which baseline patient characteristics are most strongly associated with the progression of diabetes one year later. The analysis emphasizes rigorous statistical modeling, the evaluation of linear regression assumptions, and the responsible interpretation of observational data (correlation vs. causation).

📊 The Dataset
The dataset (diabetes.tab.txt) consists of 442 patient records and 11 variables.

Outcome Variable: progression (a quantitative measure of disease progression one year after baseline).

Predictor Variables:

age, sex

bmi (Body Mass Index)

bp (Mean Arterial Blood Pressure)

s1 to s6 (Six blood serum measurements including total cholesterol, LDL, HDL, and log serum triglycerides).

Note: As this project handles sensitive health information, the analysis discusses the strict adherence to GDPR principles, emphasizing patient anonymity and purpose limitation.

🛠️ Tech Stack & Libraries
Language: R

Environment: RStudio

Key Packages: tidyverse, ggplot2 (for data visualization), broom (for tidy statistical outputs), car (for VIF/diagnostic metrics).

🚀 Key Analysis Steps
Exploratory Data Analysis (EDA): Assessing data quality, missing values, and generating descriptive statistics and distributions (e.g., right-skewed progression vs. normally distributed predictors).

Investigating Relationships: Utilizing correlation matrices, heatmaps, and scatterplots to identify top predictors (BMI, BP, S5) while screening for severe multicollinearity (e.g., the 90% correlation between S1 and S2).

Regression Modeling:

Simple Linear Regression: Modeling progression using only BMI (
R 
2
 =34.4%).

Multiple Linear Regression: Expanding the model to include BMI, Blood Pressure, and S5 (Log Serum Triglycerides).

Model Evaluation: Inspecting residuals-vs-fitted plots for non-linearity and heteroscedasticity, and utilizing Variance Inflation Factors (VIF) to confirm the absence of multicollinearity.

Decision-Maker Presentation: Translating complex statistical uncertainty and causal limitations into accessible business/clinical insights.

📈 Main Findings
Top Predictors: BMI, Blood Pressure, and S5 (log serum triglycerides) are the most robust independent baseline predictors of diabetes progression.

Model Performance: The multiple regression model explains ~48% of the variance in disease progression (Adjusted 
R 
2
 =0.477). Holding other factors constant, every 1-unit increase in BMI is associated with a 6.50-point increase in disease progression (
p<0.001).

Limitations (Omitted Variable Bias): Despite high statistical significance, 52.3% of the variance remains unexplained. Unmeasured lifestyle factors (diet, exercise, medications) likely play a massive role.

Causation vs. Correlation: The findings represent mathematical correlations from observational data. We cannot mechanistically guarantee that lowering a patient's BMI will halt their disease progression at the exact rates estimated by the model coefficients.

📁 Repository Structure
data/ : Contains the diabetes.tab.txt dataset.

scripts/ : The R scripts used for EDA, visualization, and regression modeling.

report/ : The final written report (XENIDIS_FINAL_PROJECT_REPORT.pdf / .docx).

presentation/ : The Decision-Maker slide deck translating statistical findings for non-technical stakeholders.

visualizations/ : Exported graphs (Correlation Heatmap, BMI vs. Progression scatterplots, Residuals plot).

💡 How to Run the Code
Clone this repository: git clone [https://github.com/xen212/LEAP-DATA-ANALYSIS-AND-STATISTICS.git](https://github.com/xen212/LEAP-DATA-ANALYSIS-AND-STATISTICS.git)

Open the R project file or script in RStudio.

Ensure the required packages are installed (install.packages(c("tidyverse", "broom", "ggplot2"))).

Run the script section by section to reproduce the statistical summaries, plots, and regression outputs.
