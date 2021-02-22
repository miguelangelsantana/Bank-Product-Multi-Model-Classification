# Banking Features & Subscriber Term Deposits  
## Predicting Drivers of Subscriber Term Deposits

* **Author**: Miguel Santana

The contents of this repository detail an analysis of client, campaign, social, economic and additional features provided by a Portuguese bank with regard to customer term deposits. The analysis will provide insight into product performance through classification models and offer insight into driving factors for business development. Analysis, business recommendations, limitations and future work are provided below. 

## Business problem:

A Portuguese financial institution provided data resulting from various direct telemarketing campaigns (Moro et al., 2014). The Portuguese bank looks to analyze the various client, campaign, social, economic and miscellaneous features to identify their significance as they relate to subscriber term deposits. 

### Data
The dataset includes the following client, campaign, social, economic and other attributes:

**Client Data**
* Age
* Job Type
* Marital Status
* Education 
* Default **(client credit in default)**
* Housing **(client housing loan)**
* Loan **(client personal loan)**

**Current Campaign | Last Contact** 
* Contact Type
* Month 
* Day of Week 
* Duration (in seconds)

**Other Attributes:**
* Campaign (number of contacts/this campaign)
* Pdays (days since last contacted/previous campaign)
* Previous (contacts performed before this campaign/this client)
* Poutcome (previous campaign outcome)

**Social & Economic Context Attributes**
* Emp.var.rate (quarterly employment variation rate)
* Cons.price.idx (monthly indicator - consumer price index)
* Cons.conf.idx (monthly indicator - consumer confidence index)
* Euribor3m (daily indicator - euribor 3 month rate)
* Nr.employed (quarterly indicator - number of employees)

**Output/Target**
* y (has the client subscribed a term deposit?)

### Framework

![graph1](/images/OSEMN.png)

**The OSEMN Framework was used to analyze the data**

## Data Cleaning/Scrubbing 

**Choices**

* Renaming Target Variable
* Dropping "Unknown" Variables in Client Features
* Addressing Outlier Data (Age)
* Using Multiple Models | Selecting Top Features

## Exploratory Data Analysis | Client Features

### Client Features

**Client Education Level**

![graph2](/images/education.png)

**Client Occupations**

![graph3](/images/job.png)

### Bank Features

**Days Since Customer Last Contacted**

![graph4](/images/daysslastcontact.png)

**Number Of Contacts This Campaign**

![graph5](/images/numbercontactc.png)

## Model

**Eight classification models were performed. The models included a gradient boosting classifier, adaboost, k-nearest neighbors, random forest, decision tree, support vector machine, logistic regression and guassian naive bayes classifier.**

**Multi-Model Accuracy Scores**

![graph6](/images/modelscores.png)

**Gradient Boosting Classifier**

![graph7](/images/gbcresults.png)

## Results | Conclusion

The dataset offered various consumer trends and illustrated multiple areas of opportunity. In most cases, the features that related to these constants represented both; highest number of subscribers and highest number of non-subscribers. This leads us to believe that consistency and performance metrics are not followed as the volume of work increases resulting in a natural increase of total subscribers but an exponential increase in consumers who decline term deposit products. Selected customer and bank features will be evaluated in the business recommendations below. 

### Top Features

Top features were selected using the overlapping important features in the top two performing models. The top two models were the Gradient Boosting Classifier and AdaBoost.

### Selected Features

* Age
* Number of Employees (Quarterly)
* Days Since Last Contact
* Number of Contacts (This Campaign)

**Visualizing Top Features**

![graph8](/images/resultsvisuals.png)

## Business Recommendations

1) Consumers between the ages of 30 and 40 make up the largest amount of term deposit subscribers but also reflect the largest amount of non-subscribing customers. The age group with the smallest gap between subscribing and non-subscribing customers includes customers ages 17 to 25. Construct and apply similarly structured marketing, outreach and advertising techniques to the customer age segment 30 to 40 in order to convert additional non-subscribing customers. 

2) The gap between number of subscribing and non-subscribing customers begins to grow significantly once the number of quarterly employed employees goes over 5076. While the number of subscribed term deposits does continue to grow the level of productivity declines dramatically. Review bank productivity guidelines and drive performance per employee when employee levels go over 5076. 

3) When considering the number of times a consumer has been contacted for the current campaign – there is an obvious decline in the number of subscriber term deposits as the number of contacts per customer increase. Deploy an A team (high performers) to handle customer outreach during the first three contacts to increase the chance of conversion. 

4) The 'days since last contact' data show an abundance of non-subscribing and subscribing consumers in the '999' or 'has not been contacted' category. Deploy a B team to (high performers) to field incoming marketing calls that arrive from numbers that are not registered in the bank's database. In addition, consider methods of dividing customers into 'new' and 'existing' during day-to-day operations.  High performing team members should be deployed to address new bank customers.  

## Limitations

The dataset and business insights are limited to customers who specifically cite their job type, marital status and education level when registering as a bank customer. Additionally, the models and features reflect clients that are between 17 and 69 years of age. 

## Future Work
In order to more accurately define the boundaries of our features it is important to understand what customs and cultural influences are tied to this dataset (Portuguese banking info). For example: knowing the average level of education, the geographic locations of client residences and information on financial markets in this region may alter the way we perceive these variables.

Additionally, the dataset illustrates that the vast majority of subscribing consumers enroll in bank products when they are not contacted by telemarketers. It would be helpful to review additional data on these consumers in order to evaluate different means of product conversion (such as social media, the Internet, day-to-day walk-ins, etc.)

### For further information
Please review the narrative of our analysis in [our jupyter notebook](./jupyter_notebook.ipynb) or review our [presentation](./presentation.pdf)

For any additional questions, please reach out via email at santana2.miguel@gmail.com, on [LinkedIn](https://www.linkedin.com/in/miguel-angel-santana-ii-mba-51467276/) or on [Twitter.](https://twitter.com/msantana_ds)


##### Repository Structure:

```

├── README.md               <- The top-level README for reviewers of this project.
├── jupyter_notebook.ipynb     <- narrative documentation of analysis in jupyter notebook
├── presentation.pdf        <- pdf version of project presentation

```


