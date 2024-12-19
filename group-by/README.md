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

###  Calcolare la media dei voti di ogni appello d'esame

```SQL
SELECT 
	es.exam_id AS `exam_id`,
    e.date AS `exam_date`,
    AVG(es.vote) AS `average_vote`
FROM 
	db_university.exam_student AS es
JOIN 
	db_university.exams AS e
ON 
	es.exam_id = e.id
GROUP BY
	es.exam_id,
    e.date
ORDER BY 
	`exam_date` ASC;
```