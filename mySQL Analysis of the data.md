## Questions
1. what region has the highest amount of incidents recorded?
2. what is the total sum of death cases, Number of Missing cases, and Number of Survivors cases recorded in
a. all the total regions? 
b. in each region? 
3. what is the total number of Females cases, Males cases, and Child cases recorded in
a. all the total regions?
b. in each region? 
4. what is the most likely Cause of Death recorded in
a. all the total regions?
b. in each region? 
5. what month was the incident mostly Reported?
6. what is the month with the highest number of death cases, Missing cases, Survivors cases, Female cases, Male cases, Children cases
7. what is the most likely cause of death in the month of January?
8. what is the most likely cause of death recorded in October?

***

## Solutions
1. what region has the highest amount of incidents recorded?
```sql
SELECT Region, COUNT(Region)
FROM missing_immigrant GROUP BY Region;

```
![q1](https://user-images.githubusercontent.com/114537955/229356882-13f54c0e-d915-4052-9168-a3fa0a60b6a4.png)

***
2. what is the total sum of death cases, Number of Missing cases, and Number of Survivors cases recorded in

a. all the total regions?  
```sql
SELECT SUM(Number_Dead),
SUM(Minimum_Estimated_Number_of_Missing),
SUM(Number_of_Survivors)
FROM missing_immigrant;

```
![q2](https://user-images.githubusercontent.com/114537955/229358416-a3f26af8-d4b4-4f0c-acc0-a979e8f8ca6e.png)

b. in each region? 
```sql
SELECT Region,
SUM(Number_Dead),
SUM(Minimum_Estimated_Number_of_Missing),
SUM(Number_of_Survivors)
FROM missing_immigrant GROUP BY Region;

```
![q2b](https://user-images.githubusercontent.com/114537955/229358544-b647d5bc-b945-49a8-9daf-aef596765337.png)

***
3. what is the total number of Females cases, Males cases, and Child cases recorded in

a. all the total regions?  
```sql
SELECT
SUM(Number_of_Females),
SUM(Number_of_Males),
SUM(Number_of_Children)
FROM missing_immigrant;

```
![q3](https://user-images.githubusercontent.com/114537955/229358672-d8d25893-bfef-41b1-9b59-af999fd8f852.png)

b. in each region? 
```sql
SELECT
Region,
SUM(Number_of_Females),
SUM(Number_of_Males),
SUM(Number_of_Children)
FROM missing_immigrant GROUP BY Region;

```
![q3b](https://user-images.githubusercontent.com/114537955/229358752-a7c446da-8aa2-4816-98ae-069238f7b4a9.png)
