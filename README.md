Code 1:
SELECT * 
FROM crime_scene_report
LIMIT 5;

Output:


![image](https://github.com/user-attachments/assets/9ef29f2e-d69c-47f4-8ee6-e3eddb76bf05)


 ![image](https://github.com/user-attachments/assets/11c37725-2625-4397-9a95-a949845932ec)


Code 2:
SELECT *
FROM crime_scene_report
WHERE type = "murder";

Code 3:
SELECT *
FROM crime_scene_report
WHERE type = "murder"
AND date = 20180115
AND city = "SQL City";


Output: ![image](https://github.com/user-attachments/assets/ca96cb6d-55c8-430c-9751-9fcd996ae703)

 

Code 4:
SELECT *
FROM person
LIMIT 5;

Output:

![image](https://github.com/user-attachments/assets/997e2493-f171-416e-9aff-768b57e137ae)


Code 5:
SELECT *
FROM person
WHERE address_street_name = "Northwestern Dr"
ORDER BY address_number DESC;


Output:
![image](https://github.com/user-attachments/assets/61ce4390-0f42-4915-a229-7b86db6787d9)


Code 6:
SELECT *
FROM person
WHERE name LIKE '%Annabel%'
AND address_street_name = "Franklin Ave";

Output:
 

![image](https://github.com/user-attachments/assets/73892291-b236-469b-819f-38d5f84cd5c6)

Code 7:
SELECT *
FROM interview
WHERE person_id IN ("14887", "16371");

Output:

![image](https://github.com/user-attachments/assets/da71a0c5-bd6a-49ef-81ff-d9af19cb20c7)




So, here's our clues:
•	Murderer is a man and a member of a gym called "Get Fit Now Gym" and has a gold membership no. starting from "48Z".
•	He was working out at the gym on 9th Jan.
•	He drives a car with car plate containing "H42W".


Code 8:
SELECT *
FROM get_fit_now_check_in
WHERE membership_id LIKE '48Z%'
AND check_in_date = "20180109";

Output:
 ![image](https://github.com/user-attachments/assets/d9a6f9d0-47f6-45a5-8cf7-166bb1553b8e)


Code 9:
SELECT *
FROM drivers_license
WHERE gender = "male"
AND plate_number LIKE '%H42W%';




Output:
 ![image](https://github.com/user-attachments/assets/bc91b6bc-e1c8-4acf-926f-ea6f2338c3de)


Code 10:
SELECT *
FROM person
WHERE license_id IN ("423327", "664760");

Output:
 ![image](https://github.com/user-attachments/assets/154c93b4-1d91-409b-bb08-5ff0a372917d)


Code 11:
SELECT *
FROM get_fit_now_member
WHERE person_id IN ("51739", "67318");

Output:
![image](https://github.com/user-attachments/assets/791b6147-6cd3-4a9d-8a35-5ed9dcfb27a4)

 
Jeremy Bowers is the Murderer.

THE FINAL SOLUTION
 ![image](https://github.com/user-attachments/assets/e2e7d863-4c8b-49db-9895-f0c9b7910954)

 Code 12:
 INSERT INTO solution VALUES (1, 'Jeremy Bowers'); 
SELECT value FROM solution;



Code 13:
SELECT *
FROM interview
WHERE person_id = "67318";



Code 14:

SELECT *
FROM drivers_license
WHERE gender = "female"
	AND hair_color = "red"
	AND height BETWEEN 65 AND 67
	AND car_make = "Tesla"
	AND car_model = "Model S";

 Code 15:
SELECT *
FROM person
WHERE license_id IN ("202298", "291182", "918773");


code 16:

SELECT *
FROM personSELECT 
	person_id, 
    event_name, 
    COUNT(*) AS event_count
FROM facebook_event_checkin
WHERE person_id IN ("78881", "90700", "99716")
GROUP BY person_id, event_name;
WHERE license_id IN ("202298", "291182", "918773");

Code 17:
INSERT INTO solution VALUES (1, 'Miranda Priestly');
SELECT value FROM solution;
