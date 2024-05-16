1: Selezionare tutti gli studenti iscritti al corso di laurea in economia:
SELECT * 
FROM `students`
INNER JOIN `degrees`
ON `students`. `degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = "Corso di laurea in economia";

2: Selezionare tutti i corsi di Laurea Magistrale del Dipartimento di neuroscienze:
SELECT `degrees`.`name`, `degrees`.`level`, `departments`.`name`
FROM `degrees`
INNER JOIN `departments`
ON `degrees`. `department_id` = `departments`.`id`
WHERE `departments`.`name` = "Dipartimento di neuroscienze" AND `degrees`.`level` = "magistrale";

3: Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44):
SELECT *
FROM `course_teacher`
WHERE `teacher_id` = 44;

4:  Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
 sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
 nome:
SELECT *
FROM `students`
INNER JOIN `degrees`
ON `students`.`degree_id`=`degrees`.`id`
INNER JOIN `departments`
ON `degrees`.`department_id`= `departments`.`id`
ORDER BY `surname` ASC;
