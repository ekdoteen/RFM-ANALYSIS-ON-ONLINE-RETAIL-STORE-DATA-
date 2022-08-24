# RFM-ANALYSIS-ON-ONLINE-RETAIL-STORE-DATA-

DESCRIPTION

A banking institution requires actionable insights into mortgage-backed securities, geographic business investment, and real estate analysis. 
The mortgage bank would like to identify potential monthly mortgage expenses for each region based on monthly family income and rental of the real estate.
A statistical model needs to be created to predict the potential demand in dollars amount of loan for each of the region in the USA. Also, there is a need to create a dashboard which would refresh periodically post data retrieval from the agencies.
The dashboard must demonstrate relationships and trends for the key metrics as follows: number of loans, average rental income, monthly mortgage and owner’s cost, family income vs mortgage cost comparison across different regions. The metrics described here do not limit the dashboard to these few.Data Import and Preparation:

Import data. 

Figure out the primary key and look for the requirement of indexing.

Gauge the fill rate of the variables and devise plans for missing value treatment. Please explain explicitly the reason for the treatment chosen for each variable.

Perform debt analysis. You may take the following steps:

Explore the top 2,500 locations where the percentage of households with a second mortgage is the highest and percent ownership is above 10 percent. Visualize using geo-map. You may keep the upper limit for the percent of households with a second mortgage to 50 percent

Use the following bad debt equation:

Bad Debt = P (Second Mortgage ∩ Home Equity Loan)
Bad Debt = second_mortgage + home_equity - home_equity_second_mortgage
Create pie charts  to show overall debt and bad debt

Create Box and whisker plot and analyze the distribution for 2nd mortgage, home equity, good debt, and bad debt for different cities

Create a collated income distribution chart for family income, house hold income, and remaining income

Perform EDA and come out with insights into population density and age. You may have to derive new fields (make sure to weight averages for accurate measurements): 

Use pop and ALand variables to create a new field called population density

Use male_age_median, female_age_median, male_pop, and female_pop to create a new field called median age

Visualize the findings using appropriate chart type

Create bins for population into a new variable by selecting appropriate class interval so that the number of categories don’t exceed 5 for the ease of analysis.

Analyze the married, separated, and divorced population for these population brackets

Visualize using appropriate chart type

Please detail your observations for rent as a percentage of income at an overall level, and for different states.

Perform correlation analysis for all the relevant variables by creating a heatmap. Describe your findings.

 
 The economic multivariate data has a significant number of measured variables. The goal is to find where the measured variables depend on a number of smaller unobserved common factors or latent variables. 

Each variable is assumed to be dependent upon a linear combination of the common factors, and the coefficients are known as loadings. Each measured variable also includes a component due to independent random variability, known as “specific variance” because it is specific to one variable. Obtain the common factors and then plot the loadings. Use factor analysis to find latent variables in our dataset and gain insight into the linear relationships in the data. 

       Following are the list of latent variables:

Highschool graduation rates

Median population age

Second mortgage statistics

Percent own

Bad debt expense

 

Data Modeling :

Build a linear Regression model to predict the total monthly expenditure for home mortgages loan. 

       Please refer deplotment_RE.xlsx. Column hc_mortgage_mean is predicted variable. This is the mean monthly mortgage and owner costs of specified geographical location.

       Note: Exclude loans from prediction model which have NaN (Not a Number) values for hc_mortgage_mean. 

       a) Run a model at a Nation level. If the accuracy levels and R square are not satisfactory proceed to below step.

       b) Run another model at State level. There are 52 states in USA.

       c) Keep below considerations while building a linear regression model:

Variables should have significant impact on predicting Monthly mortgage and owner costs

Utilize all predictor variable to start with initial hypothesis

R square of 60 percent and above should be achieved

Ensure Multi-collinearity does not exist in dependent variables

Test if predicted variable is normally distributed

 

Data Reporting:

Create a dashboard in tableau by choosing appropriate chart types and metrics useful for the business. The dashboard must entail the following:

Box plot of distribution of average rent by type of place (village, urban, town, etc.).

Pie charts to show overall debt and bad debt.

Explore the top 2,500 locations where the percentage of households with a second mortgage is the highest and percent ownership is above 10 percent. Visualize using geo-map.

Heat map for correlation matrix.

Pie chart to show the population distribution across different types of places (village, urban, town etc.).

.......................>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

RFM (Recency Frequency Monetary) is a method used for analyzing customer value. Needed to perform customer segmentation using RFM analysis in order to find out most valuable and least valuable customers.     Also needed to figure out the active customers on a monthly basis and the retention rate of the customers.
•	Performed descriptive analysis after data inspection and cleaning
•	Performed Cohort analysis by creating month cohorts and analyzing the active customers for each cohort.
•	Also plotted heatmap based on cohort month and cohort index in order to visualize the retention rate percentage.
•	Used datetime library and groupby function to find recency. 
•	Used count and groupby function to find the frequency values. 
•	Used groupby and sum function to find the amount spent by each customer(monetary).
•	After that joined the columns using inner join and removed outliers using Inter Quartile Range (IQR).
•	Performed scaling on the columns in order to reduce the deviance compared to each other.
•	Used K Means clustering method for the model.
•	Used 3 clusters for the model. Verified by WSS method by comparing with different values of cluster.
•	Performed exploratory data analysis on the clusters in order to find which clusters have highest recency, frequency and monetary values.
•	Used libraries such as numpy, pandas, matplotlib, seaborn, sklearn.
•	Created dashboard in Tableau giving insights on different metrics.
