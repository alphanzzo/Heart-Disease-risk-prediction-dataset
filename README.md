
# Heart Disease Risk Factors: China vs USA

An NTU IE0005 group data science project investigating differences in heart disease risk factors between Chinese and US datasets.

**My contributions:** Exploratory Data Analysis (EDA) and Random Forest Classifier implementation.

**Technologies:** Python, Pandas, Matplotlib, scikit-learn, Jupyter Notebook, Google Colab.


**Key work:**
- Explored and visualized relationships between health indicators and heart disease.
- Implemented Random Forest classifiers to compare feature importance across the Chinese and US datasets.
- Generated comparative visualizations to interpret differences in predictive factors.

**Key finding:** Diabetes had the highest Random Forest feature importance in the US model (0.4129), while sex ranked highest in the China model (0.1751), narrowly ahead of diabetes (0.1735).

**Run the notebook:** "Scroll down all the way to see the results and conclusion" [Open in Google Colab](https://colab.research.google.com/drive/1A49CYe41S55z8qYimu0LKyIrccxSD7yn)


Dataset 1: Chinese data

Dataset 2: CDC BRFSS Data

Problem:
Which variable has the strongest influence on the risk of heart disease of a person for both countries(USA, CN)?

Does it make sense to apply machine learning?
Yes, because:

The likelihood of having heart disease is largely determined by factors such as age, exercise, smoking, alcohol use, and other health indicators.
Individuals with similar lifestyle and health profiles should have similar risks of heart disease.
Individuals with very different habits or health conditions should have different risks of heart disease.


## Data Analysis & Visualizations
<img width="1092" height="188" alt="image" src="https://github.com/user-attachments/assets/37aba5ae-f33e-4c3d-aa8e-e8e62774eaf4" />

### 1. Exploratory Data Analysis — Cramér's V

![China Cramér's V Heatmap]
<img width="1092" height="188" alt="image" src="https://github.com/user-attachments/assets/37aba5ae-f33e-4c3d-aa8e-e8e62774eaf4" />


This heatmap visualizes the strength of association between categorical variables in the Chinese dataset using Cramér's V.

Most off-diagonal values are close to zero, indicating very weak pairwise associations among the variables examined. This prompted further investigation into the dataset's relationships and suitability for predictive modelling.

Cramér's V measures association, not causation, and low pairwise associations do not establish statistical independence.

### 2. Logistic Regression — Age and Heart Disease Log-Odds

![Age vs Heart Disease Log-Odds]

<img width="579" height="433" alt="image" src="https://github.com/user-attachments/assets/973ab0f7-c916-4984-9a6d-f904e59d294a" />
This visualization compares observed heart disease log-odds across age groups in the US and Chinese datasets.

**Key observations:**
- **USA:** Log-odds generally increase with age, suggesting a positive association between age and the recorded heart disease outcome.
- **China:** Log-odds remain approximately constant across the age groups examined, indicating little apparent age-related variation in this dataset.

The contrasting patterns raise questions about differences in dataset construction, target definitions and population characteristics.

As part of exploratory analysis, we also investigated logistic regression assumptions, including binary outcomes, multicollinearity and the relationship between continuous predictors and log-odds.

### 3. Random Forest — Feature Importance Comparison

![Random Forest Feature Importance]=<img width="889" height="590" alt="image" src="https://github.com/user-attachments/assets/48995fa0-89bd-4295-9933-a9ce60bc9b1e" />

Separate Random Forest classifiers were trained on the Chinese and US datasets to compare the relative importance of common predictors.

**Key findings:**
- **USA:** Diabetes had the highest feature importance (0.4129), followed by smoking status (0.1868).
- **China:** Sex had the highest feature importance (0.1751), closely followed by diabetes (0.1735) and obesity (0.1704).
- Feature importance scores were more evenly distributed in the Chinese model than in the US model.

These results describe how the fitted models used the available variables. They do not establish causal relationships or clinical risk factors.

### Limitations

- The two datasets use different outcome definitions, including heart disease and heart attack, which limits direct comparability.
- Dataset sampling and feature coding may affect the observed patterns.
- The Random Forest importance analysis has not yet been evaluated on a held-out test set.
- Findings are exploratory and should not be interpreted as clinical predictions or medical conclusions.

The cell below creates:

us_data, a pandas.DataFrame of the CDC BRISS 2021 data
cn_data, a pandas.DataFrame of the Chinese data



