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

```SQL
SELECT `office_address` AS `building`,
COUNT(*) AS `teacher_count`
FROM db_university.teachers
GROUP BY `office_address`
ORDER BY `teacher_count` DESC
```