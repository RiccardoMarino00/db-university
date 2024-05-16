1: Contare quanti iscritti ci sono stati ogni anno :
   SELECT COUNT(*) AS `number_enrollment_per_year` , YEAR(`enrolment_date`) AS `year`
   FROM `students`
   GROUP BY  `year`;

2: Contare gli insegnanti che hanno l'ufficio nello stesso edificio:
   SELECT COUNT(*) AS `teachers_same_building` , `office_address`
   FROM `teachers`
   GROUP BY `office_address`;

3: Calcolare la media dei voti di ogni appello d'esame:
   SELECT AVG(`vote`) , `exam_id`
   FROM `exam_student`
   GROUP BY `exam_id`;
