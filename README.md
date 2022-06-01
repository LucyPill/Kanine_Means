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

![12.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/12.png):|:![2.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/2.png)
     
     
     
![12.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/12.png | width=50x50)png):|:![2.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/2.png | width=50x50):|:![treatment2](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/treatment2.png | width=50x50):|:![control1.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/control1.png | width=50x50)





## PostgreSQL Database
* ERD 
* Schemas were created
* Queries were generated to join tables

![Final_Readme_SQL.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images_Final_Repo/Final_Readme_SQL.png)


# Machine Learning



# Tableau Dashboard
Tableau public was used to create visualizations for the presentation. In addition dashboars and stories were created. (See links below)
* Link [Treatement Group: Dashboard](https://public.tableau.com/app/profile/lucy.e.pill/viz/TreatementGroupDashboard/Treatment-Dasboard?publish=yes)
* Link [Control Group: Dasboard](https://public.tableau.com/app/profile/lucy.e.pill/viz/ControlGroupDashboard/ControlGroupDashboard)
* Link [Treatment Group: Story](https://public.tableau.com/app/profile/lucy.e.pill/viz/TreatementGroupStory/TreatmentGroupStory?publish=yes)
* Link [Control Group: Story](https://public.tableau.com/app/profile/lucy.e.pill/viz/ControlGroupStory/ControlGroupStory)

![dashboard2.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images/dashboard2.png)

# Presentation
Presentation Slides: [Presentation](https://github.com/LucyPill/Kanine_Means/tree/main/Presentation%20%20)

Presentation video: 

# Segment 2 Progress:

## Github:
Main Branch

Main branch should include:
* All code necessary to perform exploratory analysis: Generated all the csv files needed and cleaning with pandas in jupyter notebook
* Some code necessary to complete machine learning portion of project 

## Machine Learning:
The first steps to moving data to an unsupervised algorithm are as follows:

1) Data selection (csv with vaccine data)

2) Data processing (cleaning with pandas and sql) 

## Database: 
Before data was imported into postgresSQL was cleaned with pandas and ERD showing relationships was generated.
Very first draft of ERD
![image](https://user-images.githubusercontent.com/56806834/169680938-ab9c2b87-d0b7-4f3d-9fed-7f755c307c99.png)


After all the cleaning up of the data, we have to make changes to the table structure. Following are the SQLs used to create new tables, Merge the data in two tables.
##### vaccinedata:
Create table VaccineData (SubjectNo numeric(10), Tooth_Id numeric(10), Days numeric(10), Rostral numeric(10), 
					 Buccal numeric(10), Distal numeric(10), Palatal numeric(10), GingivialRecession numeric(10),
					 BleedingAssessment numeric(10))
#### vaccinedata1:
Create table VaccineData1 (SubjectNo numeric(10), Tooth_Id numeric(10), Days numeric(10), Rostral numeric(10), 
					 Buccal numeric(10), Distal numeric(10), Palatal numeric(10), GingivialRecession numeric(10),
					 BleedingAssessment numeric(10))
#### Merge SQL:
INSERT INTO vaccinedata SELECT * FROM vaccinedata1
#### animalgroup:
Create table animalgroup (animalname varchar(30), subjectno numeric(10), grouptype varchar(30))

## Dashboard:
* Storyboard on a Google Slide(s)
* Description of the tool that will be used to create final dashboard: For this we will use Tablaeu 

Link [Treatement Group: Story](https://public.tableau.com/app/profile/lucy.e.pill/viz/TreatementGroupStory/TreatmentGroupStory?publish=yes)
Link 
Link [Control Group: Story](https://public.tableau.com/app/profile/lucy.e.pill/viz/ControlGroupStory/ControlGroupStory)

![dashboard2.png](https://github.com/LucyPill/Kanine_Means/blob/main/Images/dashboard2.png)


## Segment 2 Summary:
The following was accomplished:
* Cleaned data with pandas
* Started importing the csv files into postqresSQL 
* A blueprint of the dasboard was generated using tableau
* An outline of the presentation was generated
* Team members met during class and then communicated outside class via Zoom and slack to coordinate details
* Team members collaborated equally
* First ML model was attempted


# Segment 3 Progress:

## Github:
Main Branch

Main branch should include:
* All code necessary to perform exploratory analysis: Generated all the csv files needed and cleaning with pandas in jupyter notebook
* Some code necessary to complete machine learning portion of project 

## Machine Learning:
* A connection was made to an SQL database and the construct of the tables was produced there.  When importing from SQL, pandas and lambdas were used to further process the data.  All data was converted to numberical values.  Both tables of vaccinated and unvaccinated were combined into one table.  An additional column was greated named "group" that separated the vaccinated from the control group (unvaccinated).  A number 1 was assigned to the vaccinated group and a 0 was assigned to the unvaccinated group.  This made it possible in the end to see the differences between the two groups.
* Logistic Regression model was selected because we are determining two possible outcomes.  Was the patient vaccinated or not.  A benefit of using Logistic Regression model is the it proves to be very effiecient when the dataset has features that are linearly separable.  In this case vaccinated and unvaccinated.  One drawback of this model, it is more difficult to capture complex relationships.  For this reason, we averaged the gum pocket measurements in another column and drop all the individual measurements to see the bigger pictures.  What we were hoping to see is an over all reduction in measurements of the patients who were vaccinated.  That ultimate goal was achieved.
* The target for this dataset is the "group" column and the features selected are the "days" and "mean" columns.
* Data was split into testing and training using sklearn's train_test_split.
* With a current accuracy score of 1.00, this model has the highest accuracy score amongst other models tested.

## Database: 
We decided that we will separate main data table into two different tables
- conttrolgroupdata
- treatmentgroupdata

Similarly animal names are also in two different tables
- animalcontrolgroup
- animaltreatmentgroup

New ERD with new tables

![image](https://user-images.githubusercontent.com/56806834/170814519-e03703c8-f254-475c-af19-2ef91e5b7254.png)


Table Structure

![image](https://user-images.githubusercontent.com/56806834/170814538-dcc23b30-2c33-4a3f-97c6-1618c783f33f.png)



Created a SQL to join two tables to get appropriate animal name with the right values: 

- select a.animalname, g.* from treatmentgroupdata g inner join animaltreatmentgroup a on g.subjectno = a.subjectno

- select a.animalname, g.* from controlgroupdata g inner join animalcontrolgroup a on g.subjectno = a.subjectno



## Dashboard:

