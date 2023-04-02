## Questions
1. what region has the highest amount of incidents recorded?
2. what is the total sum of death cases, Number of Missing cases, and Number of Survivors cases recorded in all the total regions and in each region? 
3. what is the total number of Females cases, Males cases, and Child cases recorded in all the total regions and in each region?
4. what is the most likely Cause of Death recorded in all the total regions and in each region?
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
