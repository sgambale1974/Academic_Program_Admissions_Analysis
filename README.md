Note:  Because of the sensitive nature of the data in this project, the raw data is not provided

Project:  This was a large scale data analysis for a public school district that houses several academic programs with competetive admssions programs. The district had some suspicion that there admissions criteria were not measuring important markers of success within the program.

Summary: Predictive analysis ML modeling were utilized in order to improve admissions accuracy by over 20%

Steps: 
1) Data Cleaning: (MIB Admissions Analysis_clean_data_final_2.10.22.ipynb)
This step of the process was met with many logistical challenges; the first being that the admissions data was colleted in separate spreadsheets spanning a 15 year period.  Over this period, the admissions criteria changed and in other cases, when the criteria remained constant, the naming conventions changed.
Once all of the spreadsheets were cleaned and standardized, there were to main conditions to contend with.  Namely, for a portion of the span, the program interviewed candidates and for the other portion, they did not.  Therefore, the data had to be separated into 4 conditions - 2 programs x 2 interview conditions.
Once the data was in a standard format, it had to then be standardized over the time span.  For example, test scores from different years and different tests were not necessarily comparable.  Therefore, all data had to be normalized within admissions year before being aggregated.

2) Exploratory Data Analysis (EDA) (MIB Admissions Analysis_eda_magnet_4.5.22.ipynb)
The first step in the EDA process was to look at the distribution of each variable and their relationships to each other.  Since the ultimate goal was to conduct predictive analyses, it was important to handle outliers and correlated variables.
Once this was handled, a Principal Components Analysis (PCA) was conducted in order to reduce dimensionality and help in data visualization. At this point, K-Means Clustering was utilized in order to explore the underlying structure of the data.
Finally, the actual data was graphed in the context of these clusters which indicated a very weak relationship between the admissions criteria and ultimate student success within the programs.

3) KPI Development (MIB KPI Analysis v1_2.25.22.ipynb)
This step marked a major step forward for the district, as it had not previously considered specifically what it meant to "be successful" in these programs.  This file utilized a combiniation of admissions data and students performance data to create several KPIs.
The major programmatic challenge here was taking several databases, over several iterations and years and combining them.  For example, over the time span, the SATs changed their measurement several times.  In addition, each database stored student names differently.  The FuzzyWuzzy library was utilized here to match names.
Once the raw data was collected, cleaned and standardized, several KPIs were created in order to label each student "success" or "not success" for regression and ML analysis

4) Model development (MIB Admissions Logistic Regression Analysis.ipynb & MIB Admissions Supervised ML Models.ipynb)
Finally, in these two files, a logistic regression was conducted and an ML pipeline was developed in order to test 8 different machine learning models. Ultimately, a model was developed that improved addmissions accuracy by over 20%
 
