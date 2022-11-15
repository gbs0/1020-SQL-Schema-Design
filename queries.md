SELECT COUNT(*) AS c, specialty
FROM doctors
GROUP BY specialty
ORDER BY c DESC;
ORDER BY specialty ASC;

SELECT p.first_name, p.last_name, c.occurs_on
FROM consultations c
JOIN patients p ON c.patient_id = p.id

SELECT p.first_name, p.last_name, c.occurs_on
FROM consultations AS c
JOIN patients AS p ON c.patient_id = p.id
JOIN doctors AS d ON c.doctor_id = d.id
WHERE d.first_name = 'Rosalind'
AND d.last_name = 'Franklin';