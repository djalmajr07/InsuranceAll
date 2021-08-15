# Insurance All

Ranking most likely clients to purchase vehicle insurance with machine learning.

![insurance](https://github.com/djalmajr07/InsuranceAll/blob/main/img/capa.jpg)

[![NPM](https://img.shields.io/npm/l/react)](https://github.com/djalmajr07/InsuranceAll/blob/main/LICENSE) 

# Bussiness Problem

Insurance All is a company that provides health insurance to its customers and the product team is analyzing the possibility of offering a new product: Car insurance.
As with health insurance, customers of this new car insurance plan must pay an amount annually to Insurance All in order to obtain an amount insured by the company, intended for the costs of an eventual accident or damage to the vehicle.

Insurance All surveyed nearly 380,000 customers about interest in joining a new auto insurance product last year. All customers showed interest or not in purchasing auto insurance and these responses were saved in a database along with other customer attributes.

The product team selected 127,000 new customers who did not respond to the survey to participate in a campaign, in which they will receive an offer of the new car insurance product. The offer will be made by the sales team through phone calls.
However, the sales team has the capacity to make 20,000 calls within the campaign period.


# The challenge
In this context, me as a Data Scientist must build a model that predicts whether or not the customer would be interested in auto insurance.

As a result of my consultancy, I need to present a model that show a rank of clients who would buy a car insurance and answers to the following questions:
	
 1. The most relevant attributes of customers interested in purchasing auto insurance.
  
 2. What percentage of customers interested in purchasing auto insurance will the sales team be able to contact by making 20,000 calls?
	
 3. And if the sales team capacity increases to 40,000 calls, what percentage of customers interested in purchasing auto insurance will the sales team be able to contact?
  
 4. How many calls does the sales team need to make to contact 80% of customers interested in purchasing auto insurance?

# Business Assumption
- the most policy sales channels used were belivied to be phone, email and cellphone.
- all costumers were above minimum drive age.
- colocar mais uma ou duas aqui depois de ver a eda

# Attribute List

![image](https://user-images.githubusercontent.com/85264359/129487323-f322d8c7-d42f-469c-b0e4-47be6d993c7e.png)


# Solution Strategy

The method applied was CRISP-DM:

**Step 01. Data Description:** The objective is to use statistical metrics to identify outliers in the business scope.

**Step 02. Feature Engineering:** Derive new attributes based on the original variables to better describe the phenomenon to be modeled.

**Step 03. Data Filtering:** Filter rows and select columns that do not contain information for modeling or do not correspond to the business scope.

**Step 04. Exploratory Data Analysis:** Explore the data to find insights and better understand the impact of variables on model learning.

**Step 05. Data Preparation:** Prepare data so machine learning models can learn specific behavior.

**Step 06. Selection of resources:** Selection of the most significant attributes to train the model.

**Step 07. Machine Learning Modeling:** machine learning model training

**Step 08. Hyperparameter Fine Tunning:** Choose the best values for each of the parameters of the model selected in the previous step.

**Step 09. Convert model performance to business values:** Convert model performance to a business result.

**Step 10. Deploy Model to Production:** Publish the model to a cloud environment so that other people or services can use the results to improve the business decision.

**Step 11. Google Sheets:** Creation of google sheets button to show custumer score.

# Top Three Data Insights

H3. The place of residence influences the decision to take out car insurance.
**True Hypothesys** 

H6. People with newer vehicles are more likely to take out car insurance.
**False Hypothesys** 

H8. People without a driver's license tend not to want car insurance.
**True Hypothesys** 


# Machine Learning Models Applied
Tests were performed using the following algorithms:

**KNN Classifier**

**Logistic Regression**

**Random Forest Classifier**

**XGBoost Classifier**

**Extra Trees Classifier**

**Naive Bayes Classifier**

**LGBM Classifier**

# Machine Learning Model Performance

**Single Performance**

![Single_perf](https://user-images.githubusercontent.com/85264359/129481921-9e5cc525-c900-4cf1-8de2-21eb33b75c7a.png)


**Real Performance - Cross Validation**


![cross_validation](https://user-images.githubusercontent.com/85264359/129482000-0540752a-93fc-48f7-b472-d65dd9ee84b6.png)

LGBM Classifier has the best performance and it's lighter than others, this model was chosen to continue.


**Final Performance - Hyperparameter Fine Tunning Cross Validation**

After finding the best parameters for the model through the Random Search method, the final metrics for the model were as follows:

![fine_tuning](https://user-images.githubusercontent.com/85264359/129482450-22ad41d2-6ea8-4571-bd38-3b80a72f2c61.png)


# Bussines Result After LGBM Model

Now with a model built, I can answer the questions made by the product team.

1. The most relevant attributes of customers interested in purchasing auto insurance.

	A: they are : 'annual_premium', 'vintage', 'age', 'region_code', 'vehicle_damage', 'previously_insured', 'policy_sales_channel'.


2. What percentage of customers interested in purchasing auto insurance will the sales team be able to contact by making 20.000 calls?

	A: The percentage of intrested costumers will reach 71% by making 20.000 calls


3. And if the sales team capacity increases to 40.000 calls, what percentage of customers interested in purchasing auto insurance will the sales team be able to contact?

	A: The percentage of intrested costumers will reach 99% by making 40.000 calls


4. How many calls does the sales team need to make to contact 80% of customers interested in purchasing auto insurance?

	A: To reach 80% the sales team will have to make 23317 calls

Gains Resume : suposing that each vehicle insurance was sell at 1900 and 71% of intrested clients purchase this insurance, by making 20000 calls it should results in $26.980.000,00 with a lift in gain araund 2.5 than the base line. 


![image](https://user-images.githubusercontent.com/85264359/129485589-92709c97-4a1a-43e2-bace-7b3945cdfde4.png)

The deployment of this model was done on HEROKU, over there it's working in poduction. To test it, a link between a Google Sheet and Heroku was made containing a new dataset with costumers whose were not surveyed. Inside Sheets was created a button called 'Health Insurance Prediction' with a function 'Get Score', it will hand over a propensity score of each client in a column named 'Score'. A sample of this dataset unsorted is shown below.


![image](https://user-images.githubusercontent.com/85264359/129486338-8ac562b3-4d4b-45b2-a53a-344be2d83fb2.png)


#  Conclusion

Finally, it is clear that if the sales team call people without ranking them, their cost and effort would be exorbitant. for instance, according to this model with a list of costumers ranked if called 40.000 people out of 127.000 the result of interested costumer should reach 99%, consequently the others 87.000 clients must not be called due their lack of interesting in buy a car insurance. So this business case is classified as a ranking problem, how better ranked less effort need to be made. With a bunch of features that characterize potential costumers this model has shown to the team how to focus their calls to reduce costs and lift their gains.



#  Next steps

Start a second cycle to analyze the problem, seeking different approaches, especially considering to balance this dataset.

Possible points to be addressed in the second cycle:

-**Work with new combinations of features**

-**Balance the dataset**

-**Create a logic inside google script to re-order my table when get the score, ordering it ascendant**

-**Try new models after balance**

-**Work with a more robust method to find the best Hyper parameters for the model**

# Technologies

- Jupyter;
- AWS;
- Postgres;
- Python.
 
# Deployment into production
- Back end: Heroku, Google Scripts ;
- Front end web: Google Sheets;
- Database: kaggle csv files, Comunidade DS aws, Postgres SQL .

# Author

Djalma Luiz da Silva Junior



[<img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>](https://www.linkedin.com/in/djalmajunior07)
