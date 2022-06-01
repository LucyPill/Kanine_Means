# Kanine_Means
## Topic: Proof of Concept (POC) for a Vaccine to Prevent Gum Disease
#### “Periodontal disease is an infectious disease of the oral cavity which destroys the gum tissue and bone that support the teeth.”

The reason for selecting this topic is that we have an ongoing study, and we need to determine the effects that a potential vaccine candidate has in a sample population of 10 subjects. In this study, we will be monitoring and evaluating gum disease after the vaccine is administered and the immune response the vaccine generates against the antigens (target) we are using in our vaccine.
The data generated from this in vivo preclinical POC testing will be useful in guiding the design of both preclinical studies as well as the early-phase clinical trials, while contributing to defining reasonable risk for the investigational product in the intended patient population.


## Purpose:
Developing a vaccine is a complex long process. Before a vaccine is available to the public, it must go through several stages of testing. The first stage is the proof of concept (POC). During this stage, studies can be performed in rodents such as mice, rats, rabbits, etc.
The purpose of this study is to determine if:
* The vaccine induces a positive immune response against the bacteria we are targeting 

## Description of the source of data:
Subjects in this study will be given three vaccinations at three different time points. Blood samples will be collected after each time point to measure the antibody response and measurements of each tooth will be performed to measure pocket depth. The pocket is the space between the root surface and the gingiva. Our subjects have 32 teeth/each, each tooth will have four measurements at four different time points.

![pic2.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images/pic2.png)

### WHAT DO THE MEASUREMENTS MEAN?
Typically smaller and tighter measurements mean healthier gums. 

0-3mm without bleeding means you are in great shape. 
1-3mm with bleeding is an early sign of gingivitis. 

3-5mm without bleeding means gum disease is possible.
3-5mm with bleeding could be the beginning of gum disease.

5-7mm with bleeding means tissue damage and probably bone loss.
7mm and above with bleeding is generally the advanced stage of periodontal disease. 

## Question we hope to answer with the data:
Does the vaccine have a positive impact in preventing, or slowing gum disease?

## Deliverables:
* Presentation (Google Slides)
*  Database (PostgreSQL)
*  Machine Learning Model (Logistic Regression Model)
*  Interactive Dashboard (Tableau)

## Resources 
* Jupyter Notebook
* Python 3.7
* Tableau 
* PostgreSQL
* Visual Studio Code
* Slack

## Analysis
* Generating Tableau CSV: [ETL_Tableau.ipynb](https://github.com/LucyPill/Kanine_Means/blob/main/Tableau/ETL_Tableau.ipynb)
* Schemas and queries: [Final_SQL.txt](https://github.com/LucyPill/Kanine_Means/blob/main/SQL/Final_SQL.txt)
* Machine learning Code: [Machine_learning.Model_Final.ipynb](https://github.com/LucyPill/Kanine_Means/blob/main/Machine_Learning/Machine_learning.Model_Final.ipynb)
* Presentation Slides: [Final_Project.pptx](https://github.com/LucyPill/Kanine_Means/blob/main/Presentation/Final_Project.pptx)
* Presentation video: 

## Explore trends in the data if any:
This will allow for an educated guess of how we would like to analyze the data and how we use the tools availabe to our advantage

#### Scatter plot shows an inverse-linear trend between the two groups

![12.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/12.png):|:![2.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/2.png) 

### Bar and line graphs show an iverse-linear trend as well

![bar.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/bar.png)
![lines](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/lines.png)

##### Based on these initial observations, we decided to try logistic regression model for classification of the groups within the study

## PostgreSQL Database
* ERD: [ERD.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/ERD.png)
* Schemas and queries: [Final_SQL.txt](https://github.com/LucyPill/Kanine_Means/blob/main/SQL/Final_SQL.txt)
* CSV files used to create schemas: [Resources](https://github.com/LucyPill/Kanine_Means/tree/main/Resources)
![Final_Readme_SQL.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/Final_Readme_SQL.png)
