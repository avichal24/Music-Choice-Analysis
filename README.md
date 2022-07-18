
# MUSIC PREFERENCE:-
An Analysis of a basic handmade dataset 
to process forward to a music streaming app
company as a guide in buying the best
'Genre of music'.



## About the Dataset

It is basically my First Data Analysis 
project wherein keeping my first deployment
easy, I have made my dataset myself so that,
it does not require any type of data 
preprocessing.

Catagories are:
Age: int64
Gender: int64
Genre: Object

#### Age
This Catagory defines the different age 
group of people listening to music.


#### Gender
This column comprises of the Gender where;
Male is assigned as 1, and Female as 0.


#### Genre
This is the output variable comprising of 
the different Catagories of types of 
music like: 
    1. Classical
    2. HipHop
    3. Dance
    4. Jazz etc.
## The Algorithm Used
I have used the Decision Tree Classification
for predicting the genre of music for any random
input of Age as well gender of a person.

#### Decision Tree:
Decision Trees are a type of Supervised 
Machine Learning where the  data is continuously 
split according to a certain parameter. 
The tree can be explained by two entities,
namely decision  nodes and leaves. 
The leaves are the decisions or the final
outcomes. And the decision nodes are where 
the data is split.

![Decision tree](https://user-images.githubusercontent.com/109500969/179484002-6ad30456-1798-4f46-9c86-fe75b76ae3cc.png)

## Deployment

PLEASE LOOK FOR .ipynb FORMAT FILE, BEST EXPLANATION IS THERE ONLY.
To deploy this project run

```bash
#Music Choice Analysis 

## Importing the libraries and Dataset

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('/content/music.csv')

## Making arrangements to remove the Null Values.

df.isnull().sum()
## Found Zero Null Values

## Spliting the dataset into two variables {y: Dependent Variable; x: Independent Variable}

x = df.drop(columns=['genre']).values
y = df['genre'].values

## Decision Tree Algorithm for Classification

# Train and testing split of the variables
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size =0.20, random_state=0)

from sklearn.tree import DecisionTreeClassifier
regressor = DecisionTreeClassifier()
regressor.fit(x_train, y_train)

# predicting a Random value with input as x variable caagories.
regressor.predict([[23,1]])


## Some exploratory Data Analysis for Conclusions:

sns.countplot(df['genre'])

## Conclusion:
###From the Above Diagram we conclude that Classical music is the most listened music in Every age group of people. So, our company should not miss any deal in buying the 'Classical Genre' of music. Which can be the best value proportion for our Company

sns.countplot(df['age'])

##Conclusion:
###The above diagram dipicts us for the Age group of people to be targeted for the better gorwth and we conclude that 'The young segnment' is most of listening Music
```
## Do Not Forget to visit the "Music_Choice Analysis.ipynb" file.



## 🚀 About Me
I'm a Mechanical Engineer by education, and
love to work with data, eventually started 
my coding journey for one of my Drone project 
where I realized that, it is something that makes
me feel happy in doing.


Hope! You liked it, and it is just a begining, 
many more to come, till then Happy Analysing!!
