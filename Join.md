1: Selezionare tutti gli studenti iscritti al corso di laurea in economia:
SELECT * 
FROM `students`
INNER JOIN `degrees`
ON `students`. `degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = "Corso di laurea in economia";