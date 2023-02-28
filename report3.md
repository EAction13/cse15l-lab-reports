# Lab Report 3 - Researching commands

The command I chose to research is `less`. 

Less allows you to scroll through the contents of a file within the command prompt.

## Command 1 - Using *

By using * in the path that I was trying to scroll through, I was able to scroll through multiple files using the one command.

I used this command: `$ less non-fiction/OUP/Abernathy/*.txt`

![image](https://user-images.githubusercontent.com/122485081/218652969-dbb125fd-d30a-4c12-9537-ceca60134b48.png)

This command will allow me to use the terminal to scroll through all of the files in the Abernathy directory.

Output:

```
In the late 1940s, Bond Stores, the largest men's clothing chain at the t 
ime, created a sensation in New York City by offering a wide selection of  
suits with two pairs of pants instead of one, reintroducing a level of p  
roduct choice not seen since before the war.1 When the line of hopeful bu  
yers at its Times Square store stretched around the block, Bond had to im  
pose a limit of two suits per customer. During World War II, the apparel  
and textile industries had been converted to supply field jackets, overco  
ats, and uniforms to the U.S. and Allied Forces. But in the years immedia  
non-fiction/OUP/Abernathy/ch1.txt (file 1 of 9)
```


This function is very useful if there are a lot of short text files within one directory.

Another example:

Command: `$less non-fiction/OUP/Berk/*.txt`

![image](https://user-images.githubusercontent.com/122485081/218653454-f24a3911-7c23-4e2b-99c9-76ea66675596.png)

Output:

```
In my three decades of teaching university courses in child development,
I have come to know thousands of students, many of whom were parents or w 
ho became parents soon after completing my class. I also served on boards 
of directors and advisory committees for child-care centers, preschools,
elementary schools, and parent organizations. And my research continuall 
y drew me into classrooms, where for countless hours I observed and recor  
ded preschool and school-age children’s activities, social interactions,   
and solitary behaviors, in hopes of answering central questions about how  
non-fiction/OUP/Berk/ch1.txt (file 1 of 4)
```


## Command 2 - -N

By using the -N command, the number representing the line is displayed next to the text.

I used the command: `$ less -N non-fiction/OUP/Abernathy/ch1.txt`

This allows me to scroll through Abernathy ch1.txt with the lines numbered.
Output:

```
1
      2
      3
      4
      5 In the late 1940s, Bond Stores, the largest men’s clothing chain 
      5 at the time, created a sensation in New York City by offering a w
      5 ide selection of suits with two pairs of pants instead of one, re
      5 introducing a level of product choice not seen since before the w
      5 ar.1 When the line of hopeful buyers at its Times Square store st
      5 retched around the block, Bond had to impose a limit of two suits
      5  per customer. During World War II, the apparel and textile indus
      5 tries had been converted to supply field jackets, overcoats, and 
non-fiction/OUP/Abernathy/ch1.txt
```

This function is useful when scrolling through long files if you want to look at a specific line when there are too many to count.

Here is another example:
`$ less -N non-fiction/OUP/Kauffman/ch1.txt`

This command lets me scroll through Kauffman ch1.txt with the lines numbered.
Output:

```
1
      2
      3
      4
      5 Chapter 1
      6 Prolegomenon to a General Biology
      7 ecturing in Dublin, one of the twentieth century’s most famous ph
      7 ysicists set the stage of contemporary biology during the war-hea
      7 vy year of 1944. Given Erwin Schrödinger’s towering reputation as
      7  the discoverer of the Schrödinger equation, the fundamental form
      7 ulation of quantum mechanics, his public lectures and subsequent 
      7 book were bound to draw high attention. But no one, not even Schr
non-fiction/OUP/Kauffman/ch1.txt
```

## Command 3 - -X

The -X command leaves the text from the file you scrolled through in the terminal rather than clearing it.

I tried the command `$ less -X non-fiction/OUP/Kauffman/ch3.txt`

This allowed me to scroll through Kauffman ch3.txt, then once I exited using the Q key, the text I was scrolling through stayed on-screen.
Output:

```
Chapter 3
Autonomous Agents
Some wellspring of creation, lithe in the scattered sunlight of an early 
planet, whispered something to the gods, who whispered back, and the myst
ery came alive. Agency was spawned. With it, the nature of the universe c
hanged, for some new union of matter, energy, information, and something 
more could reach out and manipulate the world on its own behalf. Selfish?
Yes. But how does matter, energy, information, and something else miracu

puppy@DESKTOP-RG1U2SF MINGW64 ~/Documents/skill-demo1-data/written_2 (main)
$
```

This is useful if you are scrolling through the file to find specific information that you can use in the terminal or your code later on.

Another example:

Command: `$ less -X non-fiction/OUP/Castro/chA.txt`

Output:

```
El Abuelo (Grandfather)
An old-man figure called el abuelo (the grandfather) played the role of a
bogeyman in Hispano folklore. In literature it is sometimes spelled ague
lo, and some scholars speculate that it may be a borrowed word from the l
anguage of the Pueblo Indians. In Spanish it means “grandfather,” and has
become synonymous with coco, cucui, and bogeyman. This folk character is
more known in northern New Mexico than in other parts of the Southwest. 
He appeared at Christmastime to test and discipline children who did not 

puppy@DESKTOP-RG1U2SF MINGW64 ~/Documents/skill-demo1-data/written_2 (main)
$
```



## Command 4 - /pattern

While scrolling through a file using `less`, typing / followed by some text will search for that text and highlight it.

I tried `$ less -X non-fiction/OUP/Castro/chA.txt` and then `/the`:

This highlighted all of the occasions of the word "the" in Castro chA.txt. I will leave these outputs as images so that the highlighted effect stays visible.

![image](https://user-images.githubusercontent.com/122485081/218657821-7a5bc5be-765b-4446-924f-1e00a24e2f1d.png)

This is useful when searching for mentions of specific words or strings.

Another example: 
I used `$ less non-fiction/OUP/Abernathy/ch2.txt` and `/and`.

This highlighted all mentions of the word "and" in Abernathy ch2.txt

![image](https://user-images.githubusercontent.com/122485081/218658413-35471644-8b88-4caa-aa48-9eb1247a1734.png)

