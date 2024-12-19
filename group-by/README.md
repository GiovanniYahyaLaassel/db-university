### Contare quanti iscritti ci sono stati ogni anno

```SQL
SELECT 
YEAR (enrolment_date) AS `year`,
COUNT(*) AS student_count
FROM db_university.students
GROUP BY 
YEAR(enrolment_date)
ORDER BY 
`year` ASC;
```
### Contare gli insegnanti che hanno l'ufficio nello stesso edificio

