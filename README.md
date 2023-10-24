# Employee-Retention-Analysis-and-Prediction

<p>Salifort Motors is a fictional French-based alternative energy vehicle manufacturer. Its global workforce of over 100,000 employees research, design, construct, validate, and distribute electric, solar, algae, and hydrogen-based vehicles. Salifort’s end-to-end vertical integration model has made it a global leader at the intersection of alternative energy and automobiles.</p>      

<br>

## Table of Contents
* [What is this Repo About?](#what)
* [How to Run this Code](#ip)
* [Business Problem](#bp)
* [Methodology](#md)
* [Results](#re)
* [Certificate](#cf)

## What is this Repo About<a name="what"></a>  
This repository contains one Jupyter notebook that has all the code for data cleansing, EDA and machine learning, powerpoint presentation of executive summary and a python script that contains code for the deployment of the model

The final app is publicly deployed on Streamlit Cloud 👉🏽 [click here](https://warehouse-stock-level-prediction-app-exhz93bydwp2mrpp8imuae.streamlit.app/)


## How to Run this Code<a name="ip"></a>
<p style='text-align:justify;'>To run the jupyter notebook on your localhost, I recommend you install the packages I used for this project.</p>

1. Download the requirements.txt file and save it into the directory you'll be working from.
2. Create a conda environment with python 3.*

	```python

	conda create --name env-name python == 3.11
	``
3. Now install the packages from the requirements.txt file. Make sure you're in folder that has the file.

	```python

	pip install requirements.txt
	```
4. Finally, activate the environment and run the downloaded jupyter notebook

	```python

	conda activate env-name
	```
<br>


## Business Problem<a name="bp"></a>
<details>
	<summary>Problem Statement</summary>
	<br>
	<p style='text-align:justify;'>The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They refer to you as a data analytics professional and ask you to provide data-driven suggestions based on your understanding of the data. They have the following question: what’s likely to make the employee leave the company?

Your goals in this project are to analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company.

If you can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.</p>

</details>

<details>
	<summary>Project Goals</summary>
	<br>
	<ol>
		<li>Draw unique insights from what’s likely to make the employee leave the company .</li>
		<li>Build a predictive model to predict whether or not an employee will leave the company using machine learning model.</li>
	</ol>
</details>




<details>
<summary>Exploratory Data Analysis</summary>
<br>
<p>&nbsp;</p>
	
I provided answer to the following questions to draw insight from the dataset

* What is the distribution of the numerical dtype?
* What is the distribution of the categorical columns?
* How does the trend for stock level and total sale differ per hour?
* What is the total quantity sold per category?
* What is the total sales per category?
* What is the average sale per product category?
* What is the average spending per customer type?
* What is the average transaction per payment type?
* What is the hourly trend of sale recorded for each day?
* What are the top products by sales amount and quantity sold?
* What is the distribution of each product category sold per each day and hour?
</details>


<details>
<summary>Statistical Analysis</summary>
<br>
To ascertain that the  different in the average sale amount between customers who use credit cards and customers who use cash and the estimated_stock_pct of hour with sale activities greater than hour without sale activities for specific product do not occur by chance. To do this I performed hypothesis testing(Welch's t-Test) to draw conclusion on .
</details>

<details>
<summary>Feature Selection and Engineering</summary>
<br>
Some of the tasks I performed for this step include;	
	
* Creating new features from the categorical columns using `pd.get_dummies`
	
</details>

<details>
<summary>Predictive Modeling</summary>
<br>
To complete this task I went through the various machine learning steps which includes;
	
* Data Splitting - I split data to training set and test set to 80:20 ratio
* Standardization - I stardardized the dataset using `StandardScaler`
* Model Training and Evaluation - In this step, I trained various algorithms on a standardized dataset using default parameters in 10-fold  
* Hyperparameter Tuning - I performed model turning using GridSearch for the various algorithms, and the best model turned out to be __RandomForest Regressor__ 
* Final Model - I build a final model using the optimized parameter after tuning the model. 
* Model Visualization - I plot the feature importance from the model and also plotted the predicted values and actual for the  testset again time.
</details>

<br>

## Results<a name="re"></a>
At the end of this project, I was able to draw the following unique insights:

* The distribution of `temperature` and `estimated_stock_pct` is normal distribution, this means the `mean` and the `median` are equal, and the data points are evenly distributed on both side of the `mean`
* The distribution of `tota` and `unit_price` are positively skewed. This means that there are relatively fewer data points with extremely high values compared to the majority of data points, which tend to cluster toward the lower end of the distribution and also the `median` is lower than the `mean`
* Fruit & vegetables are the 2 most frequently bought product categories 
* Non-members & standard are the most frequent buyers within the store
* Tuesday and Thursday are the two most frequent day for shopping 
* Cash is the most frequently used payment method
* The hour of 11 has the highest sale recorded and sale mostly drop from the hour of 11 to V-turn at hour of 15.
* `Premium` customers have highest average spending. There is no slight difference in the average  spending amount of customers. Though `non-member` customers buy frequently, however the `average` spending of `premium` customer are higher than the average spending of `non-member`. 
*  `Medicine` has the highest average total sales of `42.77`
* `Cash` has the highest average total sales of `20.37`
* `Kitchen`, `meat` and `seafood` are the top three product categories by total sales amount of `14,456.65`, `14,102.31` and `10754.81` respectively
* `Fruit` & `vegetables` are the top 2 bought product categories by quantity sold

Base on the hypothesis test
* You cannot conclude at the 5% significance level that There is a difference in the average sale amount between customers who use credit cards and customers who use cash.
* You can conclude at the 5% significance level that the `mean estimated_stock_pct` of products with sale activities is greater than  the mean `estimated_stock_pct` of products without sale activities at specific time of the day.

The final model gave `mean absolute error` (MAE) of 0.227 which suggests that, on average, the model's predictions are off from the actual values by approximately 0.227 units. I found out that `unit_price`, `temperature` and  `total`, have strong influence on the model's prediction for stock level. I recommend that the the dataset needs to be further engineered, or more datasets need to be added.

In conclusion, I have been able to achieved the 2 main goals and have also tested the inital hypothesis.
<br>

## Certificate<a name="cf"></a> 
[Earned Certificate](https://coursera.org/share/7150d3c917ee5785eeb0a14c5c7d9af2)
