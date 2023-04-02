# Missing-Migrants-Project
Missing Migrants Project counts migrants  who have died at the external borders of states, or in the process of migration towards an international destination, regardless of their legal status. The Project records only those migrants who die during their journey to a country different from their country of residence.

Missing Migrants Project data include the deaths of migrants who die in transportation accidents, shipwrecks, violent attacks, or due to medical complications during their journeys. It also includes the number of corpses found at border crossings that are categorized as the bodies of migrants, on the basis of belongings and/or the characteristics of the death. For instance, a death of an unidentified person might be included if the decedent is found without any identifying documentation in an area known to be on a migration route.  Deaths during migration may also be identified based on the cause of death, especially if is related to trafficking, smuggling, or means of travel such as on top of a train, in the back of a cargo truck, as a stowaway on a plane, in unseaworthy boats, or crossing a border fence.  While the location and cause of death can provide strong evidence that an unidentified decedent should be included in Missing Migrants Project data, this should always be evaluated in conjunction with migration history and trends.



![3039686-902684853](https://user-images.githubusercontent.com/114537955/228284149-078a8bb6-4b1e-4105-8573-a94100671656.jpg)

The project's goal was to analyze and gain insight into the amount of immigrant missing till now.

# Tools Used

The following tools were used for this project:

- Excel worksheet
- Python
- Mysql
- Power BI

## Data Sorting, Cleaning, and Transformnation using Python
the process can be found in the link below
https://github.com/Zlimshit007/Missing-Migrants-Project/blob/main/missing-immigrant-globally-dataset.ipynb


## Data Analysis using MySQL server
For my analysis phase, I created a database called global_terrorism on MySQL server. I imported my csv file which i re-write from python directly to MySQL server by creating a new schema in my connected server and naming it immigrant_df
![Screenshot 2023-04-01 213121](https://user-images.githubusercontent.com/114537955/229312918-ee3858dc-76b4-4ab9-8ac6-10f409e14223.png)

then importing the file from TABLE DATA IMPORT WIZARD option, I created a table in the database named MISSING_IMMIGRANT, and inserts the data into the tables. Overall, this method is much easier because it reads the data much faster and inserts it into the database much more quickly.

![Screenshot 2023-04-01 213916](https://user-images.githubusercontent.com/114537955/229313090-d84f1d4c-17d8-4307-a623-b8658d8179a0.png)


After Importing the tables, I explored the data and asked several questions to gain more insight and knowledge from the data, detect patterns, and establish connections between different variables. The questions asked were:

- what region have the highest amount of incident recorded?
- what is the total sum of death case, and Number of Missing cases, Number of Survivors cases recorded in all the total regions and in each region? 
- what is the total number of Number of Females cases, Males cases, and Children cases recorded in all the total region and in each region?
- what is the most likely Cause of Death recorded in all the total region and in each region?
- what month was the incident mostly Reported?
- what is the month with the highest number of death cases, Missing cases, Survivors cases, Female cases, Male cases, Children cases
- what is the most likely cause of death in the month of january?
- what is the most likely cause of death recorded in october?

you can find the solution here https://github.com/Zlimshit007/Missing-Migrants-Project/commit/e2b9a17dc11110af9dd65d75ad9ae832f80c9d09

