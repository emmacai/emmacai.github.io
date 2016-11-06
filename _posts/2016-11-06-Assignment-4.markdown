---
layout: post
title:  "Assignment 4"
date:   2016-11-06 
---

# Assignment 4 Reflection
One of the major things that differentiated Assignment 4 from other assignments in this class was that we were working in a group. I was in a group with Dylan and Jailine. I think that my group was able to collaborate very successfully. Dylan is definitely a more experienced coder than Jailine and I. I'm sure that he was frustrated with our much slower pace at some points, but he was always willing to explain things to us, which was very helpful!

For Assignment 4, my group created a bash script that prompts users to take a survey, with their answers being logged in a CSV file. Like with most assignments in this class, this one sounded more intimidating than it actually was. Once I read through the directions on the assignment page, I realized that we were basically writing a simple script and then applying the concepts that we learned in class on the 31st of October (output redirection, csv, etc).

To write our script, we created five questions. To implement them in the script we used alternating `echo` and `read` commands. The questions are placed after the `echo` command, which marks them as the question. After each `read` command there was a corresponding variable name that shows what the survey-taker's response represents 

`echo "What is your favorite color?"`
`read FAVCOLOR`

We implemented the date stamp by coding in `TIMESTAMP=$(date)`. An easy Google search tells you that when you run `$(date)`, it prints the date out. To implement this into our script, we assigned it to a variable `TIMESTAMP`. 

Dylan created the random string identifier with the cryptography suite __openssl__. Although I don't entirely understand how this works, I do understand that it was saved to variable `IDENTIFIER`. 

On the last line of the script, we used output redirection to write an echo command that would take all of the survey responses, the time stamp, and the random string identifier into a _comma separated variable_ (CSV) file. We used the `>>` operator, which allows you to _append_ the survey responses to the csv file instead of overwriting existing responses.

`echo "$IDENTIFIER,$FAVCOLOR,$SEASON,$BIRTHPLACE,$AGE,$FAVHOLIDAY,$TIMESTAMP" >> survey.csv`

Working as a group within github and cloud9 wasn't as difficult as I expected, although I definitely struggled at some points to remember to `git push` and `git pull` to be able to see what my other group members had done, and to share what I had done with them. This assignment made me realize that I do actually know how to do a lot in Cloud9, and it's better to approach these assignments with that positive perspective.

