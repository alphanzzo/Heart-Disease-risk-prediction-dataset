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
cn_data, a pandas.DataFrame of the Chinese dat
