
# Heart Disease Risk Factors: China vs USA

An NTU IE0005 group data science project investigating differences in heart disease risk factors between Chinese and US datasets.

**My contributions:** Exploratory Data Analysis (EDA) and Random Forest Classifier implementation.

**Technologies:** Python, Pandas, Matplotlib, scikit-learn, Jupyter Notebook, Google Colab.

**Key work:**
- Explored and visualized relationships between health indicators and heart disease.
- Implemented Random Forest classifiers to compare feature importance across the Chinese and US datasets.
- Generated comparative visualizations to interpret differences in predictive factors.

**Key finding:** Diabetes had the highest Random Forest feature importance in the US model (0.4129), while sex ranked highest in the China model (0.1751), narrowly ahead of diabetes (0.1735).

**Run the notebook:** [Open in Google Colab](https://colab.research.google.com/drive/1A49CYe41S55z8qYimu0LKyIrccxSD7yn)


Dataset 1: Chinese data

Dataset 2: CDC BRFSS Data

Problem:
Which variable has the strongest influence on the risk of heart disease of a person for both countries(USA, CN)?

Is it a small problem?

No, because:

Heart disease is a major global health issue, but risk factors differ between populations.
China and the USA have different lifestyles, diets, healthcare systems, and social environments.

Does it make sense to apply machine learning?
Yes, because:

The likelihood of having heart disease is largely determined by factors such as age, exercise, smoking, alcohol use, and other health indicators.
Individuals with similar lifestyle and health profiles should have similar risks of heart disease.
Individuals with very different habits or health conditions should have different risks of heart disease.
1. Loading Data
The numerical data and so are already labelled from Kaggle. Kaggle itself provides an API for easy import of data; it even caches it for you onto the local disk.

The cell below creates:

us_data, a pandas.DataFrame of the CDC BRISS 2021 data
cn_data, a pandas.DataFrame of the Chinese data


