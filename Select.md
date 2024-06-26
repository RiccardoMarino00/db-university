### 1)  Selezionare tutti gli studenti nati nel 1990
```sql
    SELECT *
    FROM `students`
    WHERE YEAR(`date_of_birth`) = 1990;
```

### 2)  Selezionare tutti i corsi che valgono più di 10 crediti
```sql
     SELECT *
     FROM `courses`
     WHERE `cfu` > 10;
```

### 3)  Selezionare tutti gli studenti che hanno più di 30 anni
```sql
    SELECT * 
    FROM `students` 
    WHERE TIMESTAMPDIFF(YEAR, `date_of_birth` , CURDATE()) > 30;
```

### 4)  Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
 laurea
```sql
   SELECT *
   FROM `courses`
   WHERE `period` = "I semestre" AND `year` = 1;
```

### 5)  Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
 20/06/2020
```sql
 SELECT * 
 FROM `exams` 
 WHERE `hour` BETWEEN '14:00:00' AND '24:00:00' AND `date` = '2020-06-20';
```

### 6) Selezionare tutti i corsi di laurea magistrale
```sql
    SELECT *
   FROM `degrees`
   WHERE `name` LIKE 'Corso di laurea magistrale%';
```

### 7)  Da quanti dipartimenti è composta l'università?
```sql
    SELECT COUNT(*) AS `number_of_departments`
    FROM `departments`;
```

### 8)  Quanti sono gli insegnanti che non hanno un numero di telefono?
```sql
   SELECT *
   FROM `teachers`
   WHERE `phone` IS NOT NULL;
```
    
