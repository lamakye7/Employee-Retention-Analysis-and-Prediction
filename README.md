# Employee-Retention-Analysis-and-Prediction

   

<br>

## Table of Contents
* [What is this Repo About?](#what)
* [How to Run this Code](#ip)
* [Overview](#ov)
* [Business Problem](#bp)
* [Data Understanding](#ds)
* [Conclusion](#re)
* [Recommendation](#rec)
* [Certificate](#cf)

## What is this Repo About<a name="what"></a>  
This repository contains one Jupyter notebook that has all the code for data cleansing, EDA and machine learning. 

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

## Overview<a name="ov"></a>
<details>
	<br>
	<p style='text-align:justify;'>The goal of this project was to perform employees retention analysis and create machine learning model (decision tree and random forest model) to predict whether an employee will leave the company or not. This project utilized HR data at Salifort Motors.  The final random forest model outperformed  the decision tree model with  98% recall and 98% precision. However, the  decision tree model having more FP than FN, could be able to predict true cases of employees leave, which can help the HR take retentive measures. So therefore, I adopted the decision tree model as suitable solution for employees retention over the random forest model. Based on the model, last_evaluation, number_project, monthly_loyalty, and tenure were the most influential in determining whether employee will leave or not.

</details>

## Business Problem<a name="bp"></a>
<details>

	
<p style='text-align:justify;'>The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They wanted answer to the question: what’s likely to make the employee leave the company?

Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.</p>

</details>

## Data Understanding<a name="ds"></a>
<details>

	
<p style='text-align:justify;'>The data consisted of approximately 15k rows and 10 features. The features included information on satisfaction level, last evaluation , number of project,
       average monthly hours , tenure, work accident, left, promotion for last 5years, department, and salary.</p>

</details>



## Conclusion <a name="re"></a>
<details>
At the end of this project, I was able to draw the following unique insights:

It appears that employees are leaving the company as a result of poor management. Leaving is tied to longer working hours, many projects, and generally lower satisfaction levels. It can be ungratifying to work long hours and not receive promotions or good evaluation scores. There's a sizeable group of employees at this company who are probably burned out. It also appears that if an employee has spent more than six years at the company, they tend not to leave.
</details>

## Recommendation <a name="rec"></a>
<details>
* Cap the number of projects that employees can work on.
* Consider promoting employees who have been with the company for atleast four years, or conduct further investigation about why four-year tenured employees are so dissatisfied.
* Either reward employees for working longer hours, or don't require them to do so.
* If employees aren't familiar with the company's overtime pay policies, inform them about this. If the expectations around workload and time off aren't explicit, make them clear.
* Hold company-wide and within-team discussions to understand and address the company work culture, across the board and in specific contexts.
* High evaluation scores should not be reserved for employees who work 200+ hours per month. Consider a proportionate scale for rewarding employees who contribute more/put in more effort.
</details>
<br>

## Certificate<a name="cf"></a> 
[Earned Certificate](https://coursera.org/share/7150d3c917ee5785eeb0a14c5c7d9af2)
