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

## Machine Learning Model: 
The machine learning model considered for this project is hierarchical clustering.  The two main factors for this selection are as follows:

&nbsp;&nbsp;&nbsp;*The dataset is relatively small in size. Hierarchical clustering works well with small datasets.

&nbsp;&nbsp;&nbsp;*Hierarchical clustering is an unsupervised ML model.  Since the outcome of the data is unknown, unsupervised ML is likely the best selection.

## Database:
We are going to have one table VaccineData which will hold all the readings for all tooth positions for all the dogs in all different groups. Please see the sample data below.
![image](https://user-images.githubusercontent.com/56806834/167991483-49d85ab4-cedb-4835-a0a0-14b305a760b6.png)

We will be having couple reference tables for Animals and Groups. We will be creating these tables in the next segments.


## Segment 1 Summary:
The following was accomplished:
* Topic was selected
* The reason the topic was selected
* Description of the source of data
* Question we hope to answer with the data
* A GitHub Repo was created and members were invited to collaborate
* Members met in person last weekend and disccused more details during class this evening
* Provisional machine learning model was suggested
* Provisional database was suggested 

# Segment 2 Progress:

## Github:
Main Branch

Main branch should include:
* All code necessary to perform exploratory analysis: Generated all the csv files needed and cleaneing with pandas in jupyter notebook
* Some code necessary to complete machine learning portion of project 

## Machine Learning:
Data needed for this cleaned with pandas...

![pandas_cleaning.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images/pandas_cleaning.png)

## Database: 
Before data was imported into postgresSQL was cleaned with pandas and ERD showing relationships was generated.

## Dashboard:
* Storyboard on a Google Slide(s)
* Description of the tool that will be used to create final dashboard: For this we will use Tablaeu 

## Segment 2 Summary:
The following was accomplished:
* Cleaned data with pandas
* Started importing the csv files into postqresSQL 
* A blueprint of the dasboard was generated using tablaeu 
* An outline of the presentation was generated
* Team memebers met during class and then communicated outside class via Zoom and slack to coordinate details.

