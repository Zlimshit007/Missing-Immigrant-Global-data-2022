## Questions
1. what region has the highest amount of incidents recorded?
2. what is the total sum of death cases, Number of Missing cases, and Number of Survivors cases recorded in
 
a. all the total regions? 

b. in each region? 
3. what is the total number of Females cases, Males cases, and Child cases recorded in

a. all the total regions?

b. in each region? 
4. what is the most likely Cause of Death recorded?
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

***
4. what is the most likely Cause of Death recorded

```sql
SELECT
Region,
SUM(Number_of_Females),
SUM(Number_of_Males),
SUM(Number_of_Children)
FROM missing_immigrant GROUP BY Region;

```
![q4](https://user-images.githubusercontent.com/114537955/229375144-c150e9b7-f6ef-452d-8440-4880e5e12c4c.png)

***
5. what month was the incident mostly Reported?

```sql
SELECT
Reported_Month,
COUNT(Reported_Month)
FROM missing_immigrant GROUP BY Reported_Month;

```
![q5](https://user-images.githubusercontent.com/114537955/229375379-2a9aaac4-7490-4701-a046-0d862c9e8b7c.png)

***
6. what is the month with the highest number of death cases, Missing cases, Survivors cases, Female cases, Male cases, Children cases?
```sql
SELECT Reported_Month,
COUNT(Reported_Month),
SUM(Number_Dead),
SUM(Minimum_Estimated_Number_of_Missing),
SUM(Number_of_Survivors), SUM(Number_of_Females),
SUM(Number_of_Males), SUM(Number_of_Children)
FROM missing_immigrant GROUP BY Reported_Month;

```
![q6](https://user-images.githubusercontent.com/114537955/229375531-0b81da2e-dcb0-4196-9189-e5550e6cc295.png)

***
7. what is the most likely cause of death in the month of January?
```sql
SELECT
Reported_Month,
Cause_of_Death, COUNT(Cause_of_Death)
FROM missing_immigrant
WHERE Reported_Month = 'January' GROUP BY Cause_of_Death;

```
![q7](https://user-images.githubusercontent.com/114537955/229375652-3fe631f4-8b4d-4de8-9f01-8a0721b649af.png)

***
8. what is the most likely cause of death recorded in October?
```sql
SELECT
Reported_Month, Cause_of_Death,
COUNT(Cause_of_Death)
FROM missing_immigrant
WHERE Reported_Month = 'October'
GROUP BY Cause_of_Death;
```
![q8](https://user-images.githubusercontent.com/114537955/229375746-7ab511ce-3b79-4ec2-9604-aaa67017afdb.png)




