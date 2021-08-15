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
	
 1. Main Insights on the most relevant attributes of customers interested in purchasing auto insurance.
  
 2. What percentage of customers interested in purchasing auto insurance will the sales team be able to contact by making 20,000 calls?
	
 3. And if the sales team capacity increases to 40,000 calls, what percentage of customers interested in purchasing auto insurance will the sales team be able to contact?
  
 4. How many calls does the sales team need to make to contact 80% of customers interested in purchasing auto insurance?

# Business Assumption
- the most policy sales channels used were belivied to be phone, email and cellphone.
- all costumers were above minimum drive age.
- colocar mais uma ou duas aqui depois de ver a eda

# Attribute List

![image](https://user-images.githubusercontent.com/85264359/129464212-df36b06e-d1a0-4cbd-8ba3-198ad89edc7e.png)

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

**Step 11. Google Sheets:** Creation of google sheets button to show custumer score  on the telegram app, to consult the forecast at any time

# Top Three Data Insights





- tentar criar um botar que ordena a lista do google sheets
