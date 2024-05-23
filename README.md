# <p align="center"> Capstone-Project-on-Insurance-Claims </p>

# <p align="center">![image](https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/assets/96239993/70b59c6c-3693-4015-a3e2-2bcfb5e48f69)</p>


## Overview

Machine learning in insurance claim analysis involves employing algorithms to analyze claim data. 
These algorithms detect fraudulent claims by identifying irregular patterns and behaviors. 
They also assess risk levels associated with claims, predict claim severity, and estimate claim frequency based on historical data and relevant factors. 
By leveraging machine learning, insurers can make data-driven decisions, improving efficiency, reducing costs, and effectively managing risk. 
This enables insurers to streamline the claims process, detect fraudulent activities, and allocate resources more efficiently, ultimately benefiting both insurance companies and policyholders.


  ## Requirements

- Python 3

- Libraries: NumPy, pandas, Sklearn, etc.

- Jupyter Lab

[Datasets Used]
[Claims1.csv](https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/blob/3d49eed36dad710952b5249aacd6ed8b6b247855/Claims1.csv)

https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/blob/529c75ae951b6db47dacdb30915903cacea57d60/cust_demographics%20(1).xlsx

[Python Script (Code)][(Capstone Project_Insurance Claims (1).ipynb)](https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/blob/ddbe97d81046d1eeb5b3c632fc3e9c354ebd215a/Capstone%20Project_Insurance%20Claims%20(1).ipynb)


[Ppt presentation]([Capstone project ppt.pptx](https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/blob/d9a6037c3d70f74831c65d83adbe3fc15c0d69a0/Capstone%20project%20ppt.pptx))


### Features 

- Data preprocessing: Clean and prepare the transactional data for analysis.
  
- Supervised learning: Train classification models to classify transactions as fraudulent or legitimate.
  
- Model evaluation: Assess the performance of the models using relevant metrics such as precision, recall, and F1-score.


## Balancing an unbalanced dataset:
```py
import matplotlib.pyplot as plt
plt.figure(figsize = (3,3))
Cust_data["fraudulent"].value_counts().plot(kind="bar",color=["red","green"])
```
```py
import matplotlib.pyplot as plt
fig = plt.figure(figsize = (3,3))
balanced_sample.fraudulent.value_counts().plot(kind='bar', color= ['red','green'])
plt.title('Distribution of data based on the Fraudulent of our balanced dataset')
plt.show()
```

###### Result: 

![image](https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/assets/96239993/1fe09a51-a79b-4b88-a0a2-1826df4266f0)

## Model evaluation:

##### Compariosion of All The Accuracy of Each Model

```py
models = ['LogisticRegression', 'DecisionTreeClassifier','RandomForestClassifier', 'KNeighborsClassifier', 'GaussianNB',] 
accuracy_values = [LogisticRegression_Train_Accuracy, DecisionTreeClassifier_Train_Accuracy,RandomForestClassifier_Train_Accuracy, KNeighborsClassifier_Train_Accuracy, GaussianNB_Train_Accuracy] 
plt.figure(figsize=(18, 5))
# # Plot the bar graph
bars = plt.bar (models, accuracy_values, color=['red', 'blue', 'green', 'orange','black'])
#Add accuracy values on top of each bar
plt.bar_label(bars, labels=[f"{acc:.2f}" for acc in accuracy_values])
#Add Labels and title
plt.xlabel('Models')
plt.ylabel('Accuracy')
plt.title('Accuracy Comparison for Different Models')
#Show the plot
plt.show()
```

###### Result:

![image](https://github.com/manojgaikwad13/Capstone-Project-on-Insurance-Claims/assets/96239993/88af7d20-36f7-4b1f-b5f6-19ae2efe5cae)


