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
* Presentation
*  Database
*  Machine Learning Model 
*  Interactive Dashboard

## Resources 
* Jupyter Notebook
* Python 3.7
* Tableau 
* PostgreSQL

## Analysis
* Generating Tableau CSV: [ETL_Tableau.ipynb](https://github.com/LucyPill/Kanine_Means/blob/main/Tableau/ETL_Tableau.ipynb)
* Schemas: [SQL](https://github.com/LucyPill/Kanine_Means/tree/main/SQL)
*  XXXXXXXX
*  XXXXXXXX

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

