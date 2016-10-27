---
layout: post
title:  "Assignment 3"
date:   2016-10-27 
---

# Abstract of Written Work
The written work that I chose to convert is a paper I wrote for Communication 140 at UNC called "Internet Memes: Weapons of Mass Disruption". The purpose of this paper was to understand how Internet memes have the capacity to influence people in a way that disrupts nromal political socialization. I argue that Internt memes offer a modern method of social commentary, particularly in relation to politics. Memes like "Pepper Spray Cop" and "Ted Cruz is the Zodiac Killer" allow people to spread their opinions with a large audience through the Internet, influencing their political opinions. With the creation of the Internet, political socialization is driven not only by friends and family, but also by people all over the world that we connect with throught the Internet. Internet memes are one of the many online factors that affect political socialization.

# How I Converted the Files
My file was initially a .docx file, so I imported it to Cloud 9 and renamed it "example-paper.docx". I then converted it to a markdown file in Cloud 9 by running `pandoc -o example-paper.md example-paper.docx`. 

Within the .md file, I added pictures and a table, and ensured that my headings were correct. This took some trial and error, but with the help of online resources I figured out how to do this. 

To write my script, I used the following commands:
<ul>
<li>HTML
<ul>
<li>`pandoc --smart -o example-paper.html example-paper.md`</li>
</ul></li>
<li>DOCX
<ul>
<li>`pandoc --smart -o example-paper.docx example-paper.md`</li>
</ul></li>
<li>ODT
<ul>
<li>`pandoc --smart -o example-paper.docx example-paper.md`</li>
</ul></li>
<li>PDF
<ul>
<li>`pandoc --smart -o example-paper.pdf example-paper.md`</li>
</ul></li>
</ul>

I included `--smart` so that the files would all have smart quotes, which can also be achieved by writing -S. 

# Here are the links to my converted files on Github
[example-paper.md](https://github.com/inls161/assignment-3-emmacai/blob/320abe222ad99aff3922ede4f47af5394512acd9/example-paper.md)

[example-paper.docx](https://github.com/inls161/assignment-3-emmacai/blob/320abe222ad99aff3922ede4f47af5394512acd9/example-paper.docx)

[example=paper.html](https://github.com/inls161/assignment-3-emmacai/blob/320abe222ad99aff3922ede4f47af5394512acd9/example-paper.html)

[example-paper.odt](https://github.com/inls161/assignment-3-emmacai/blob/320abe222ad99aff3922ede4f47af5394512acd9/example-paper.odt)

[example-paper.pdf](https://github.com/inls161/assignment-3-emmacai/blob/320abe222ad99aff3922ede4f47af5394512acd9/example-paper.pdf)

# Here is the link to my script:
[script](https://github.com/inls161/assignment-3-emmacai/blob/320abe222ad99aff3922ede4f47af5394512acd9/emmacai-convert-docs.sh)

# Here is the link to my Github and Cloud 9 Workspace
[Github](https://github.com/inls161/assignment-3-emmacai)
[Cloud9](https://ide.c9.io/emmacai/assignment3)

# Reflection
I didn't find this assignment particularly challenging. It was definitely helpful to work with the people around me. However, I noticed that I wasn't as consistent with committing and pushing my changes to Github, which resulted in only having a few commits that had a _lot_ of changes. I think that converting documents is an interesting and useful skill to have. 