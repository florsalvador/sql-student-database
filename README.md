# Student Database

## Tutorial 1

1. `echo hello SQL`
2. `psql --username=freecodecamp --dbname=postgres`
3. `\l`
4. `CREATE DATABASE students;`
5. `\l`
6. `\c students`
7. `CREATE TABLE students();`
8. `CREATE TABLE majors();`
9. `CREATE TABLE majors_courses();`
10. `\d`
11. `ALTER TABLE students ADD COLUMN student_id SERIAL PRIMARY KEY;`
12. `ALTER TABLE students ADD COLUMN first_name VARCHAR(50) NOT NULL;`
13. `ALTER TABLE students ADD COLUMN last_name VARCHAR(50) NOT NULL;`
14. `ALTER TABLE students ADD COLUMN major_id INT;`
15. `ALTER TABLE students ADD COLUMN gpa NUMERIC(2,1);`
16. `\d`
17. `\d students`
18. `ALTER TABLE majors ADD COLUMN major_id SERIAL PRIMARY KEY;`
19. `ALTER TABLE majors ADD COLUMN major VARCHAR(50) NOT NULL;`
20. `\d majors`
21. `ALTER TABLE students ADD FOREIGN KEY(major_id) REFERENCES majors(major_id);`
22. `\d students`
23. `ALTER TABLE courses ADD COLUMN course_id SERIAL PRIMARY KEY;`
24. `ALTER TABLE courses ADD COLUMN course VARCHAR(100) NOT NULL;`
25. `\d courses`
26. `ALTER TABLE majors_courses ADD COLUMN major_id INT;`
27. `ALTER TABLE majors_courses ADD FOREIGN KEY(major_id) REFERENCES majors(major_id);`
28. `ALTER TABLE majors_courses ADD COLUMN course_id INT;`
29. `ALTER TABLE majors_courses ADD FOREIGN KEY(course_id) REFERENCES courses(course_id);`
30. `\d majors_courses`
31. `ALTER TABLE majors_courses ADD PRIMARY KEY(major_id, course_id);`
32. `\d majors_courses`
33. `\d`
34. `\d majors`
35. `INSERT INTO majors(major) VALUES('Database Administration');`
36. `SELECT * from majors;`
37. `INSERT INTO courses(course) VALUES('Data Structures and Algorithms');`
38. `SELECT * from courses;`
39. `\d majors_courses`
40. `INSERT INTO majors_courses(major_id, course_id) VALUES(1, 1);`
41. `SELECT * from majors_courses;`
42. `select * from majors;`
43. `INSERT INTO students(first_name, last_name, major_id, gpa) VALUES('Rhea', Kellems', 1, 2.5);`
44. `select * from students;`
45. `TRUNCATE majors, students, majors_courses;`
46. `select * from majors;`
47. `select * from majors_courses;`
48. `select * from students;`
49. `select * from courses;`
50. `TRUNCATE courses, majors_courses;`
51. `TRUNCATE TABLE`
52. `select * from courses;`
53. `select * from majors;`
54. `TRUNCATE majors, students, majors_courses;`
55. `select * from majors;`
56. `TRUNCATE majors, students, majors_courses;`
57. `TRUNCATE TABLE`
58. `select * from majors;`
59. `\d courses`
60. `TRUNCATE majors, students, majors_courses;`
61. `select * from courses;`
62. `\d majors_courses`
63. `select * from majors;`
64. `select * from courses;`
65. `select * from majors_courses;`
66. `select * from students;`
67. `\d students`
68. `select * from students;`
69. `select * from majors;`
70. `select * from courses;`
71. `select * from majors_courses;`
72. `SELECT * from courses;`
73. `\d majors_courses`
74. `INSERT INTO majors_courses(major_id, course_id) VALUES(1, 1);`
75. `SELECT * from majors_courses;`
76. `select * from majors;`
77. `INSERT INTO students(first_name, last_name, major_id, gpa) VALUES('Rhea', Kellems', 1, 2.5);`
78. `select * from students;`
79. `TRUNCATE majors, students, majors_courses;`
80. `select * from majors;`
81. `select * from majors_courses;`
82. `select * from students;`
83. `select * from courses;`
84. `TRUNCATE courses, majors_courses;`
85. `select * from courses;`
86. `select * from majors;`
87. `TRUNCATE majors, students, majors_courses;`
88. `select * from majors;`
89. `TRUNCATE majors, students, majors_courses;`
90. `select * from majors;`
91. `\d courses`
92. `TRUNCATE majors, students, majors_courses;`
93. `select * from courses;`
94. `\d majors_courses`
95. `select * from majors;`
96. `select * from courses;`
97. `select * from majors_courses;`
98. `select * from students;`
99. `\d students`
100. `select * from students;`
101. `select * from majors;`
102. `select * from courses;`
103. `select * from majors_courses;`

## Tutorial 2

1. `psql --username=freecodecamp --dbname=postgres`
2. `\l`
3. `\c students`
4. `\d`
5. `\d students`
6. `select * from students;`
7. `select first_name from students;`
8. `select first_name, last_name, gpa from students where gpa < 2.5;`
9. `select first_name, last_name, gpa from students where gpa >= 3.8;`
10. `select first_name, last_name, gpa from students where gpa != 4.0;`
11. `select * from majors;`
12. `select * from majors where major = 'Game Design';`
13. `select * from majors where major != 'Game Design';`
14. `select * from majors where major > 'Game Design';`
15. `select * from majors where major >= 'Game Design';`
16. `select * from majors where major < 'G';`
17. `select * from students where last_name < 'M';`
18. `select * from students where last_name < 'M' or gpa = 3.9;`
19. `select * from students where last_name < 'M' and gpa = 3.9;`
20. `select * from students where last_name < 'M' and gpa = 3.9 or gpa < 2.3;`
21. `select * from students where last_name < 'M' and (gpa = 3.9 or gpa < 2.3);`
22. `select * from courses;`
23. `select * from courses where course like '_lgorithms';`
24. `select * from courses where course like '%lgorithms';`
25. `select * from courses where course like 'Web%';`
26. `select * from courses where course like '_e%';`
27. `select * from courses where course like '% %';`
28. `select * from courses where course not like '% %';`
29. `select * from courses where course like '%A%';`
30. `select * from courses where course ilike '%A%';`
31. `select * from courses where course not ilike '%A%';`
32. `select * from courses where course not ilike '%A%' and course like '% %';`
33. `select * from students;`
34. `select * from students where gpa is null;`
35. `select * from students where gpa is not null;`
36. `select * from students where major_id is null;`
37. `select * from students where major_id is null and gpa is not null;`
38. `select * from students where major_id is null and gpa is null;`
39. `select * from students order by gpa;`
40. `select * from students order by gpa desc;`
41. `select * from students order by gpa desc, first_name;`
42. `select * from students order by gpa desc, first_name limit 10;`
43. `select * from students where gpa is not null order by gpa desc, first_name limit 10;`
44. `select min(gpa) from students;`
45. `select max(gpa) from students;`
46. `select sum(major_id) from students;`
47. `select avg(major_id) from students;`
48. `select ceil(avg(major_id)) from students;`
49. `select round(avg(major_id)) from students;`
50. `select round(avg(major_id), 5) from students;`
51. `select count(*) from majors;`
52. `select count(*) from students;`
53. `select count(major_id) from students;`
54. `select distinct(major_id) from students;`
55. `select major_id from students group by major_id;`
56. `select major_id, count(*) from students group by major_id;`
57. `select major_id, min(gpa) from students group by major_id;`
58. `select major_id, min(gpa), max(gpa) from students group by major_id;`
59. `select major_id, min(gpa), max(gpa) from students group by major_id having max(gpa) = 4.0;`
60. `select major_id, min(gpa) as min_gpa, max(gpa) from students group by major_id having max(gpa) = 4.0;`
61. `select major_id, min(gpa) as min_gpa, max(gpa) as max_gpa from students group by major_id having max(gpa) = 4.0;`
62. `select major_id, count(*) as number_of_students from students group by major_id;`
63. `select major_id, count(*) as number_of_students from students group by major_id having count(*) < 8;`
64. `select * from students full join majors on students.major_id = majors.major_id;`
65. `select * from students left join majors on students.major_id = majors.major_id;`
66. `select * from students right join majors on students.major_id = majors.major_id;`
67. `select * from students inner join majors on students.major_id = majors.major_id;`
68. `select * from majors left join students on majors.major_id = students.major_id;`
69. `select * from majors inner join students on majors.major_id = students.major_id;`
70. `select * from majors right join students on majors.major_id = students.major_id;`
71. `select major from majors inner join students on majors.major_id = students.major_id;`
72. `select distinct(major) from majors inner join students on majors.major_id = students.major_id;`
73. `select * from majors left join students on majors.major_id = students.major_id where student_id is null;`
74. `select * from students left join majors on students.major_id = majors.major_id;`
75. `select * from students left join majors on students.major_id = majors.major_id where major = 'Data Science' or gpa >= 3.8;`
76. `select first_name, last_name, major, gpa from students left join majors on students.major_id = majors.major_id where major = 'Data Science' or gpa >= 3.8;`
77. `select * from students full join majors on students.major_id = majors.major_id where first_name like '%ri%' or major like '%ri%';`
78. `select first_name, major from students full join majors on students.major_id = majors.major_id where first_name like '%ri%' or major like '%ri%';`
79. `select students.major_id from students full join majors on students.major_id = majors.major_id;`
80. `select students.major_id from students full join majors as m on students.major_id = m.major_id;`
81. `select s.major_id from students as s full join majors as m on s.major_id = m.major_id;`
82. `select * from students full join majors using(major_id);`
83. `select * from students full join majors using(major_id) full join majors_courses using(major_id);`
84. `select * from students full join majors using(major_id) full join majors_courses using(major_id) full join courses using (course_id);`
