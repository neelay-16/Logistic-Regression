# Titanic Survival Prediction using Logistic-Regression

This project uses logistic regression to predict survival on the Titanic dataset. The dataset contains information about passengers and their survival status. We'll go through the data preprocessing steps and build a logistic regression model to predict whether a passenger survived or not.

# Prerequisites

Before running the code, make sure you have the following libraries installed:

pandas
seaborn
scikit-learn
You can install them using pip command.

# Data Exploration

Let's start by loading the dataset and exploring its basic information.

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/a7250fe9-49f0-4388-8956-b60e7f83dcb5)

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/a965117a-c574-46bf-a95f-f653e2e1ed96)

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/78514bae-c1d0-41c6-a3e5-78ec2c7c579c)

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/ac51d6cb-b917-4bb4-89ec-d7c06cd09605)

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/3d980a1f-5fed-43bd-b0dd-b3e62504f732)

# Data Visualization

Let's visualize the data using seaborn. Now, create count plots to show the survival distribution based on gender and explore missing data with a heatmap.

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/9fb0e2da-d68c-4772-b907-f68c994e07b9)

# Data Preprocessing

From the heatmap,we come to know that there are many missing values in the 'age' and 'cabin' column. We can't proceed with such type of data because it can affect the accuracy of our model. So,it seems that 'age' column has fewer less number of missing values that in the 'cabin' column. So,lets try to work on our 'age' column a bit.

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/f028cb0d-d54b-4cb0-a035-0008f846d406)

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/6692f240-5220-45a1-8cb4-38120e246dfb)

And it seems that working on the 'cabin' column is not feasible because it contains many gaps. Even if we try to improve the data in that column,even it may affect the accuracy of our model.
So,we will just drop that column

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/be83de26-4f4e-4a2a-b8d6-2beaec841c34)

# Feature Engineering

Doing another cleaning of data by changing the string in 'Sex' column to number because ML model works only on number. This I will do with the help of "One hot Encoding" where I will be creating dummy variables of male and female. Similarly,for 'PClass','SibSp','Parch','Embarked' columns too. But also be aware of the dummy variable trap which occurs due to the collinearity. This is also known as categorical variable.

![image](https://github.com/neelay-16/Logistic-Regression/assets/135517502/c9317024-2ec5-4f29-9e40-77098dec8700)


# Model Building

