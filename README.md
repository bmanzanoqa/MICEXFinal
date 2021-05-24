# MINI BLOCKS EXHIBITION APP


## Contents
* [Summary](#Summary)
   * [History](#my-approach)
   * [Project Requirements](#project-requirements)
* [Project Tracking](#project-tracking)
* [Databases Structure](#database-structure)
* [Risk Assessment](#risk-assessment)
* [CI Pipeline](#ci-pipeline)


* [Testing](#testing)
* [Front-End Design](#front-end-design)
* [Known Issues](#known-issues)
* [Future Improvements](#future-improvements)
* [Authors](#authors)

## Summary
### History 
I love building 'stuff' with microblock pieces. My project is based in the idea of having an APP where I can store the items I build and the rooms (called Exhibitions) where they will be displayed.  I wanted to have a login page where user(other than me, ie, my children) could create a new account or login. Once I had login I would be taken to a page where I would have the options of Items and Exhibitions. In any of these options, once I clicked on them, I would be presented with a selection of CRUD(create, Read, Update,Delete) options. This was more difficult than anticipated so I went for a simpler version.   
This here is how all started.... [First Idea](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/Starting%20point.png) and [Project Structure](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/Project%20Structure.png).  
One day.... it will look like that, till then....


## So.... the simpler version:

The app offers you the option to create, Read, Update and Delete (CRUD) items and Exhibitions (Items are the things I built and Exhibitions the rooms where they will be display).  
The app is run on a database where the tables have a one to many relationships.

### Project Requirements
The objective of this project is to create a CRUD application with utilisation of supporting tools, such as:
- Jira board to cover the project management side of it
- A relational databases with at least 2 tables, showing the relationship between them
- A README.md document explaining the basis and architecture of this project
- Risk Assessment
- A functional CRUD application created in Python that will meet the requirements of the Jira Board
- Python Testing
- A functioning front-end website and integrated API's, using Flask.
- Code fully integrated into a Version Control System using the
Feature-Branch model which will subsequently be built through a CI
server and deployed to a cloud-based virtual machine.

## Project Tracking
As project Management Software I have used Jira. The link to this board can be found in here [Jira Board](https://trizmanz.atlassian.net/secure/admin/EditDefaultDashboard!default.jspa)

![Jira Board Backlog](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/Jira%20Board%20Backlogs%2023.05.21.PNG)

![Jira Board All Sprints](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/Jira%20Board%20All%20Sprints.PNG)

In these 2 boards I have taken a screenshoot of the Backlogs showing the Epics and User Stories this project is based on and a screenshoot of the Dashboard showing where we are with our sprints. A user story is an end goal expressed from the user’s perspective​. I have used the Definition of Ready (DoR)
to establish what a product backlog item needs before it can go into the sprint backlog andd the Definition of Done (DoD) defines what is needed before it can be regarded as complete.

## Database Structure
This project needs a relational database with at least 2 tables, showing the relationship between them. 
The tables created are:
- Exhibitions
- Items

Both tables have a primary key (). The foreign key is in the Items table, showing the relationship to the Exhibitions table.

The relationship is a ```one-to-many``` relationship where an Exhibition can have many Items but an Item can belong or appear in one Exhibition (can't be in 2 places at the same time) .

In the pictures below we can see an Entity Relationship Diagram explaining the relationship between the tables used in this project. This file can be found in [ERD](https://github.com/bmanzanoqa/PythonProjects/blob/main/MICEX/Screenshots.png/ERD%202%20tables.PNG).

![ERD](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/ERD%202%20tables.PNG)



## Risk Assessment
We use Risk Assessments to evaluate scenarios that may impact the project in a negative way. By knowing the risk and ways to mitigate them we are able to create a project were risks are less likely to occur. As parts of the projects were getting near completion others risks were added to the template and all of them revisited.This file can be found in [Risk Assessment](https://github.com/bmanzanoqa/PythonProjects/blob/main/MICEX/Screenshots.png/ERD%202%20tables.PNG)

Below is a screenshot of the Risk Assessment I have carried out for this project. To see an earlier copy of it you can go to this [First Risk Assessment](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/RA%201.PNG). 

![Risk Assessment][https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/RA%20latest.PNG]


## CI Pipeline
Continuous integration (CI) allows developers to frequently merge code changes into a central repository where others can contribute.    
The main Version Control System used for this project is GitHub. The VCS is designed to track changes to code over time as contributors add new features to the application. This system allows for cohesive collaboration and the ability to easily revert an application to a previous, stable state if new code breaks something.  
The CI server I have used to handle all the automated building, testing, and deployment of code as it is pushed to the VCS is Jenkings.

In the image below we can see how the developers (me) write the code in a chosen language (we have chosen Python for this project) and this gets push to the git repository and pull back to the local branch so everyone can work independently, contribute in the project and have always the latest version.   As explained above I have used Jira as a project tracking tool which it is supported by GitHub too so the boards can be updated, sprints start and finish and be always on top.   With continuous integration I have used Jenkins as CI server so some parts of the project can be automated by this tool.  Again, Jenkins and GitHub will pull and poll code as the scripts are run, saving time and gaining accuracy.
For the testing side of the peoject I have used pytest as testing environment and as a cloud provider I have used GCP.

![CI Pipeline](https://github.com/bmanzanoqa/MICEXFinal/blob/main/Supporting%20Files/CI%20Pipeline.PNG)

## Testing
As with most things, testing is the part where, after you have hit your head against the table for a 1000 times because you could not get the app to work when you were developing, then this 'testing' comes around and finishes you. When you thought that everything work, you have that feeling of accomplishment and triumph, you feel like a winner because your app does what you tell it to do... you decide to run 'some tests' and your app crashes. Yes, that is what happened to me every time I tried to run the Integration testing. 
I have used pytest as my testing tool. 

I started with unit testing, runing a total of 12 tests and reaching 95% of the covering report as you can see in the image below. You can also look at the HTML report [here](file:///C:/Users/B/Desktop/MICEXFinal/htmlcov/index.html).

Screenshots of my progress are below:
[coverage1]()
[final report]()



Below is my first error when running unit testing with pytest....
[First error]()
And it finally worked! I think what caused me more trouble with the unit testing were the validators. 

Here you can see some of the many errors I encountered with doing [integration testing](https://onedrive.live.com/view.aspx?resid=96A94FCBFABC7DB5%2170903&id=documents&wd=target%28MICEX.one%7C5462FF26-5891-4F62-AC9E-01DC3AAB8BC9%2FErrors%7CC861D920-7CD4-41FE-B595-D82E5FE51456%2F%29). My machine just refuses to connect.... I would be logged into the terminal of the VM and I would be running a test and even though I am connected to it I will get errors saying it cannot connect. 











Opening Microblocks Exhibitions ....
Deleting any previous databases, please wait .....
Creating a new database

[Link](https://google.com)

![pic](https://github.com/bmanzanoqa/PythonProjects/blob/ba09f39d1323940254550d6a17c1eba15b26bb34/MICEX/Screenshots.png/Bear%20Shopping.jpg)

| Left Align  | Centre Align | Right Align   |
| :---        |    :----:    |          ---: |
| Row1        | Row1         | Row1          |
| Row2        | Row2         | Row2          |


<details>
<summary>"Click to expand"</summary>
this is hidden
</details>

