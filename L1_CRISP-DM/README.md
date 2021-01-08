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

For Data Wrangling there are some good tips in that section [here](https://chrisalbon.com/)
Luckily stackoverflow has already collected the data for us. However, we still need to wrangle the data in a way for us to answer our questions. The wrangling and cleaning process is said to take 80% of the time of the data analysis process. You will see that will hold true through this lesson, as a majority of the remaining parts of this lesson will be around basic data wrangling strategies.

We will discuss the advantages and disadvantages of the strategies discussed in this lesson

There are two main 'pain' points for passing data to machine learning models in sklearn:

* Missing Values
* Categorical Values
Sklearn does not know how you want to treat missing values or categorical variables, and there are lots of methods for working with each. For this lesson, we will look at common, quick fixes. These methods help you get your models into production quickly, but thoughtful treatment of missing values and categorical variables should be done to remove bias and improve predictions over time.

Three strategies for working with missing values include:

### 3.1. We can remove (or “drop”) the rows or columns holding the missing values.
Though dropping rows and/or columns holding missing values is quite easy to do using numpy and pandas, it is often not appropriate.

Understanding why the data is missing is important before dropping these rows and columns. In this video you saw a number of situations in which dropping values was not a good idea. These included

Dropping data values associated with the effort or time an individual put into a survey.
Dropping data values associated with sensitive information.
In either of these cases, the missing values hold information. A quick removal of the rows or columns associated with these missing values would remove missing data that could be used to better inform models.

Instead of removing these values, we might keep track of the missing values using indicator values, or counts associated with how many questions an individual skipped.

### 3.2. We can impute the missing values.
Imputation is likely the most common method for working with missing values for any data science team. The methods shown here included the frequently used methods of imputing the mean, median, or mode of a column into the missing values for the column.

There are many advanced techniques for imputing missing values including using machine learning and bayesian statistical approaches. This could be techniques as simple as using k-nearest neighbors to find the features that are most similar, and using the values those features have to fill in values that are missing or complex methods like those in the very popular AMELIA library.

Regardless your imputation approach, you should be very cautious of the BIAS you are imputing into any model that uses these imputed values. Though imputing values is very common, and often leads to better predictive power in machine learning models, it can lead to over generalizations. In extremely advanced techniques in Data Science, this can even mean ethical implications. Machines can only 'learn' from the data they are provided. If you provide biased data (due to imputation, poor data collection, etc.), it should be no surprise, you will achieve results that are biased.

* Impute the mean of a column.
* If you are working with categorical data or a variable with outliers, then use the mode of the column. Also to work with categorical data when there are only a few values you can choose [this](https://pbpython.com/categorical-encoding.html)
* Impute 0, a very small number, or a very large number to differentiate missing values from other values.
* Use knn to impute values based on features that are most similar.

Chris' content is again very helpful for many of these items. He uses the [sklearn.preprocessing library](https://scikit-learn.org/stable/modules/preprocessing.html). There are also a ton of ways to fill in missing values directly using pandas, which can be found [here](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.fillna.html)

### 3.3. We can build models that work around them, and only use the information provided.
By droping all the missing data you can work around with the dataset, but it's really important that if you don't have enough data this may be lead to bad results

## 4. Data Modeling
In the 'putting all together' notebook you can find like the last iteration of all the process, but it's really important to understand that this is a cycle process and maybe you can find new ways to clean and prepare the data to get better or different results

## 5. Evaluate the Results
Results are the findings from our wrangling and modeling. They are the answers you found to each of the questions.

## 6. Deploy
Two techniques for deploying your results include:

Automated techniques built into computer systems or across the web. You will do this later in this program!

Communicate results with text, images, slides, dashboards, or other presentation methods to company stakeholders.
To get some practice with this second technique, you will be writing a blog post for the first project and turning in a Github repository that shares your work.

As a data scientist, communication of your results to both other team members and to less technical members of a company is a critical component

