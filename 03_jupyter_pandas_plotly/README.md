# 03: Data Analysis with Jupyter, Pandas and Plotly

# 03.1: Titanic Dataset

Now that you know basic Python, it's time to use it to analyze data. The core functionality is provided by:
- Jupyter, which gives you a nicer web-based interface meant for experimentation
- Pandas, which allows you to use Series objects for sequences of data (such as time series) and DataFrame objects for tabular data
- plotting libraries such as Plotly to produce charts and graphs

Unlike the previous module where you were following the exercises of a book, in this one we make it a bit more realistic by making up questions that a non-technical person might ask you about your data.

## Getting Started
1. Start by installing [Jupyter](https://jupyter.org/install), [Pandas](https://pandas.pydata.org/docs/getting_started/install.html#installing-from-pypi) (note that you're probably installing with PyPI, not with Anaconda), and [Plotly](https://plotly.com/python/getting-started/).
2. Next, go to Kaggle and have a look at the [Titanic dataset](https://www.kaggle.com/c/titanic/data). For now, use only the `train.csv` file. This is the data that you will be studying in this exercise.

The dataset you downloaded contains the following information:
- Passenger information such as gender, age, cabin type (1st, 2nd, or 3rd class), etc
- A boolean column representing whether they survived the Titanic disaster or not

## Exercises
Your goal is to answer the following questions. Use Pandas to manipulate the data. Questions 1, 2 and 3 can be answered just with a number, question 4 asks you to produce a new file and a plot. Question 5 is more open-ended and plots are the main tool for it.

- Q1: What's the average age of all Titanic passengers?
- Q2: What's the average age of the passengers who did not survive?
- Q3: What is the fraction of survivors within women aged 40 and over?
- Q4: Let's call AgeGroup the decade of the person's age. So people aged [0,10[ belong to one AgeGroup, people aged [10,20[ belong to another AgeGroup, and so on. Produce a new CSV with the following format:
```
Gender,AgeGroup,SurvivalRate
Male,0-10,XXX
Male,10-20,YYY
Male,20,30,ZZZ
...
Male,90-100,AAA
Female,0-10,BBB
Female,10-20,CCC
...
Female,90-100,DDD
```
where XXX,YYY,ZZZ,AAA,BBB,CCC,DDD are the survival rates for people of that sex and AgeGroup. Create also a graph which appropriately represents the survival by gender and AgeGroup.

- *Q5: What else can you find about the data?* (this is what's called Exploratory Data Analysis: exploring the data without specific questions in mind)

# 03.2: Wisconsin Breast Cancer Dataset
TODO

# 03.3: Lending Club Dataset
TODO

# Learning Materials
You're welcome to first do a tutorial on Jupyter, Pandas or Plotly (or more than one), but for this exercise try to get into the habit of searching online for answers. For example, if you don't know how to import a CSV into pandas, try searching "how to import csv into python pandas". If you don't know how to compute the average of a column, search for that, and so on.

If you get stuck, ask for help on Slack. Learning the right balance between "I should search online for this" and "I've been already stuck for hours, time to ask for help" is part of your training too.
