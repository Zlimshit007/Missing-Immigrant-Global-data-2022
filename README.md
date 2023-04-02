## Questions
1. How many successful attacks were carried out, and what was the total number of deaths?
2. Which target types were the most prominent in successful terrorist attacks?
3. What was the most common attack type in successful terrorist attacks?
4. Which regions have the highest number of successful terrorist activities?
5. Which countries had the most terrorist attacks, and what were the number of fatalities, kidnappings, and injuries in those countries?
6. What happened to the hostages who were kidnapped after the attacks?
7. What are the top six weapon types used in successful terrorist attacks, based on the number of fatalities and injuries?
8. What is the trend of successful terrorist attacks over the years?

***

## Solutions
1. How many successful attacks were carried out, and what was the total number of deaths?
```sql
SELECT count(success) AS successful_attack,
       count(nkill) AS total_death
FROM attack
WHERE attack.success = 1;
```
| successful_attack | total_death |
|------------------|-------------|
|     161632      |   151721   |
