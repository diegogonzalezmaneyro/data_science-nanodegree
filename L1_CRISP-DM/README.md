# CRISP-DM

The CRISP-DM Process (Cross Industry Process for Data Mining)
The lessons leading up to the first project are about helping you go through CRISP-DM in practice from start to finish. Even when we get into the weeds of coding, try to take a step back and realize what part of the process you are in, and assure that you remember the question you are trying answer and what a solution to that question looks like.

## 1. Business Understanding
This means understanding the problem and questions you are interested in tackling in the context of whatever domain you're working in. Examples include
* How do I break into the field?
* What are the placement and salaries of those who attended a coding bootcamp?
* How well can we predict an individual's salary?
* What aspects correlate well to salary?
* How well can we predict an individual's job satisfaction?
* What aspects correlate well to job satisfaction?

## 2. Data Understanding
At this step, you need to move the questions from Business Understanding to data. You might already have data that could be used to answer the questions, or you might have to collect data to get at your questions of interest.
In this case, you will be using the Stackoverflow survey data to get some insight into each of these questions. In the rest of the lesson, you can work along with me to answer these questions, or you can take your own approach to see if the conclusions you draw are similar to those you would find throughout this lesson.

## 3. Prepare Data
Luckily stackoverflow has already collected the data for us. However, we still need to wrangle the data in a way for us to answer our questions. The wrangling and cleaning process is said to take 80% of the time of the data analysis process. You will see that will hold true through this lesson, as a majority of the remaining parts of this lesson will be around basic data wrangling strategies.

We will discuss the advantages and disadvantages of the strategies discussed in this lesson

There are two main 'pain' points for passing data to machine learning models in sklearn:

* Missing Values
* Categorical Values
Sklearn does not know how you want to treat missing values or categorical variables, and there are lots of methods for working with each. For this lesson, we will look at common, quick fixes. These methods help you get your models into production quickly, but thoughtful treatment of missing values and categorical variables should be done to remove bias and improve predictions over time.

Three strategies for working with missing values include:

* We can remove (or “drop”) the rows or columns holding the missing values.
* We can impute the missing values.
* We can build models that work around them, and only use the information provided.

## 4. Data Modeling

## 5. Evaluate the Results

## 6. Deploy


