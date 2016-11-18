---
layout: post
title:  "Assignment 5"
date:   2016-11-17 
---

<h1>Assignment 5 Reflection</h1>
 For Assignment 5 we worked in groups to modify the script we wrote in Assignment 4 so that the answers to the survey were stored in a MySql database, not a csv file. This was a daunting task, as we hadn't gone over all the tools necessary to do this in class. Working in groups was very beneficial, since we could combine our knoweldge and work together to solve the problems we were running into.
 
 Within MySql, Jailine and I worked on making the database with the appropriate variables (ID, FAVCOLOR, SEASON, BIRTHPLACE, AGE, FAVHOLIDAY, TIMESTAMP) and the appropriate variable types (all were _varchar_, with the exception of age, which was _int_). We used the class notes from the 7th to do this. To make the actual database we used the command `CREATE DATABASE SurveyResults`. To create the tables with the variables we used the command `CREATE TABLE tblSurvey(columname TYPE)`. 
 
 While we were making the database, Dylan was modifying the script. We commented out the line of code that directed the results to a csv file (from Assignment 4) and replaced it with an _INSERT_ statement. To understand how this worked, I used [THIS](https://www.techonthenet.com/mysql/insert.php) helpful article about insert statements. Our final lines of code are below.
 
 `mysql SurveyResults -u $USER --password="" -H -e "INSERT INTO tblSurvey (ID, FAVCOLOR, SEASON, BIRTHPLACE, AGE, FAVHOLIDAY, TIMESTAMP) VALUES ('$IDENTIFIER', '$FAVCOLOR', '$SEASON', '$BIRTHPLACE', $AGE, '$FAVHOLIDAY', '$TIMESTAMP');"` 
 
 This code is basically saying that within mysql, use the database _Survey Results_, and insert the following information into _tblSurvey_: for each of the following columns, here are the appropriate values. 
 
 The `mysqldump` command makes our database sync automatically after a `gitpush` command, which required an ID column in the database so that there weren't duplicate submissions. 
 
 <h1>Challenges</h1>
 Luckily, my group member Dylan is skilled in the world of Cloud9, so we didn't run into a lot of problems while completing the main part of the assignment. When Jailine and I ran into problems, or had questions he could generally answer them and explain to us what we had done wrong. 
 
 However, we ran into two problems. First, when we ran the script, it would always ask for a password, even though our database didn't need or ask for one. Second, if someone typed an answer that included an apostorphe to one of the survey questions, and error would occur and the script couldn't finish running. 
 
 Dylan discovered that removing any instance of `-p` from the mysql commands, which solved the password problem easily. 
 
 The apostrophe problem was a bit more difficult to fix. Jailine and I played around with the `mysql_real_escape_string`, but could not figure out a way to make it work. We finally found a way to eliminate all non-alphabet letters/numbers from input into the database, so that all apostrophes/other characters could be used in a response to the survey, but would be eliminated when inserted into the database.
 
 <h1>Final Thoughts</h1>
 This was definitely the hardest assignment we've had thus far. I am grateful that my group worked well together and we were successful in solving the problems we ran into. I liked that we expanded what we did in Assignment 4 to include a database. I definitely got some problem solving/googling practice in, which I'm sure will come in handy as we start the final project. 
 
 [Here's](https://github.com/emmacai/groupsed) the link to the forked repository.
 
 Unrelated to the assignment, I also learned the incredibly useful _wrap lines_ feature on Cloud9, which makes it __so__ much easier to see what you are writing in a file.