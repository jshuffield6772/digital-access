![cover](https://github.com/jshuffield6772/digital-access/blob/main/images/primage.jpeg)

_When schools moved their classes online during the pandemic, how did this move affect poorer districts, poorer students, and students of color? This study explores inequities in access to digital learning in the states of Illinois, New York, and Utah._

# The Impact of COVID-19 On Digital Learning
COVID-19's impact on the world and U.S. economies continues to be a subject of analysis, but less is understood about how the virus has impacted education. Media stories covering this dimension of the pandemic have focused on the politics of school closures, openings, and mask mandates, and in some cases the transition from in-class instruction to distance learning via Zoom or other platforms--but there has been no in-depth analysis of the impacts on schoolchildren of the change in venues and instruction methods.

To begin to address the need for "hard data" on COVID's impact on education, LearnPlatform, a company devoted to increasing accessibility to computer and web-based education tools for all students in the U.S., has released data for 233 districts in 22 states and the District of Columbia, along with a call for analysts to use the data in combination with data from other sources, to assess how the pandemic impacted education in 2020.

This project explores a smaller subset of this data--55 school districts in the states of Illinois, New York, and Utah, and combines it with data from the COVID-19 State Policy Database and statistics from the KIDS COUNT project.  The links below open the project notebook and Tableau presentation, and I have included the introduction below as well.  

[PROJECT NOTEBOOK](https://colab.research.google.com/github/jshuffield6772/digital-access/blob/main/Impact-of-COVID-on-digital-access.ipynb)

[TABLEAU PRESENTATION](https://public.tableau.com/views/TheImpactofCOVID-19onDigitalLearning/COVIDandEducation?:language=en-US&:display_count=n&:origin=viz_share_link)

---

## The Challenge

LearnPlatform released the data on Kaggle, as part of a challenge they sponsored:
> Link: https://www.kaggle.com/c/learnplatform-covid19-impact-on-digital-learning/overview

We challenge the Kaggle community to explore
- the state of digital learning in 2020 and
- how the engagement of digital learning relates to factors such as district demographics, broadband access, and state/national level policies and events.
We encourage you to guide the analysis with questions that are related to the themes that are described above. Below are some examples of questions that relate to our problem statement:
- What is the picture of digital connectivity and engagement in 2020?
- What is the effect of the COVID-19 pandemic on online and distance learning, and how might this also evolve in the future?
- How does student engagement with different types of education technology change over the course of the pandemic?
- How does student engagement with online learning platforms relate to different geography? Demographic context (e.g., race/ethnicity, ESL, learning disability)? Learning context? Socioeconomic status?
- Do certain state interventions, practices or policies (e.g., stimulus, reopening, eviction moratorium) correlate with the increase or decrease in online engagement?
## THE DATA
### LearnPlatform's Files
LearnPlatform released the following data:
- Engagement data for 233 school districts, comprising daily measurements of page loads per 1000 students for individual software applications and web services (each identified with a numeric ID assigned by LearnPlatform), as well as the percentage of students in the district that had at least one page load of each application each day. Date ranges for each file are usually Jan 1, 2020 - December 31, 2020

- District Demographics for each district, detailing
  - the district locale (city, suburban, town, or rural);
  - the percentage of Black and Hispanic students;
  - the percentage of free and reduced lunches;
  - county connection ratios (# of high-speed connections per household);
  - combined local and federal annual per pupil spending
> **Anonymized Data:** The districts are anonymized using a numeric district ID, and demographics above are expressed as ranges of percents (0-20%, 20%-40%, etc.), or ranges of dollar amounts in thousands (4000 - 6000, etc.), decreasing the likelihood that a given district can be identified from this information.

- A Products File listing the 372 applications most widely used in the districts that LearnPlatform services, together with
  - the target audience for each app (K-12, Higher Ed, Corporate, or All)
  - the purpose of the app (Curriculum & Learning, Classroom Management, School & District Operations, or All)
  - LearnPlatform's numeric ID, the app name, and the corporation that owns the app.
 
LearnPlatform encourages using this data in combination with at least two additional sources of data:
### The State COVID-19 Policy Database
> Link: https://www.openicpsr.org/openicpsr/project/119446/version/V130/view
> 
This dataset, published on the data portal of the Inter-university Consortium for Political and Social Research (ICPSR), details the dates of important COVID policy changes enacted in each state in the U.S.

### The Kids Count Data Center
> Link: https://datacenter.kidscount.org

Kids Count, an ongoing project of the Annie E. Casey foundation, collects important data regarding the lives of children in the U.S., and it has published relevant statistics related to the impact of the pandemic on children's education, from which I selected the following time-based datasets:
- Households with children who lost employment income by race/ethnicity
- Households with children with access to both a high speed connection and a device/computer available for education purposes by race/ethnicity
- Change in how households with children received education due to the coronavirus pandemic by race/ethnicity. This is really five statistics in one, and it will be easier to parse by each statistic so that each will be easier to compare by race/ethnicity. The five different changes in education venue/method are:
  - Classes Cancelled
  - Online Distance Learning
  - Paper Distance Learning
  - Other (Classes changed in some other way)
  - Schools Open

> (**NOTE:** Each of the Kids Count statistics are recorded as percentages of total state populations (i.e., 72% of Black/Hispanic households in the state with schoolchildren) on a weekly basis beginning April 23, 2020.)
## The Task
Map the health of digital learning in the U.S. during the pandemic by exploring:
- Varying digital engagement levels for different demographic segments (race, ethnicity, wealth, locale)
- The impact of statewide COVID policy changes on digital engagement
- Correlating changes in state-level statistics (household income loss, household access to digital environments, and changes in how households received education) to the engagement data
- Digital infrastructure, by investigating engagement levels and applications used prior to and during the pandemic.

## Desired Outcomes
- A multi-dimensional understanding of how various forces represented in the listed data sources interact to impact engagement levels.
- An interactive visual that allows stakeholders to explore these various insights.

## Some Constraints
- **Size of the dataset(s):** The combined data sources for this project are a bit large for my project, therefore, I will be searching for ways to subset the data that still allow for a meaningful exploration of the problem.
- **Incomplete data:** The LearnPlatform data is not comprehensive; for example, many districts did not report all demographics. Also, the engagement data for most districts contains data for 1000s of applications, but of these, only 372 are identifiable via LearnPlatform's Products File. This incomplete data already suggests options for reducing the size of the datasets.
- **Time Series resolution:** The Kid's Count statistics were collected each week from the end of April 2020 to the present. The district engagement files begin in January 2020 and continue through the end of December 2020, and that data is collected daily, so coordinating these two elements will require some resampling.
- **Python/Jupyter Notebook:** Springboard requires the bulk of the analysis to be done using Python, in a Jupyter notebook; however, once my analysis has moved from the exploratory and descriptive phases to the inferential, I plan to streamline the presentation and visualizations using Tableau.

[See the Project Notebook/Code](https://colab.research.google.com/github/jshuffield6772/digital-access/blob/main/Impact-of-COVID-on-digital-access.ipynb)
