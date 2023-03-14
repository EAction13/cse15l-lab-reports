# Lab Report 5 - An alternate Lab Report 3

In Lab Report 3, I used the command `less` to scroll through the contents of a file using the command prompt.
This time, I will be looking at the command `find`, which outputs a list of files in the command prompt based on what input is used with the command.

## Command 1 - -type

By using `-type`, you can filter whether you want to find files or directories. `-type f` searches for files and `-type d` searches for directories.

For example, I used the following command in the written_2 directory:
`$ find non-fiction/OUP -type f`

This should output all of the files (but not directories) within the non-fiction/OUP directory.

This was the result:

```
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch14.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/CH4.txt
non-fiction/OUP/Berk/ch7.txt
non-fiction/OUP/Castro/chA.txt
non-fiction/OUP/Castro/chB.txt
non-fiction/OUP/Castro/chC.txt
non-fiction/OUP/Castro/chL.txt
non-fiction/OUP/Castro/chM.txt
non-fiction/OUP/Castro/chN.txt
non-fiction/OUP/Castro/chO.txt
non-fiction/OUP/Castro/chP.txt
non-fiction/OUP/Castro/chQ.txt
non-fiction/OUP/Castro/chR.txt
non-fiction/OUP/Castro/chV.txt
non-fiction/OUP/Castro/chW.txt
non-fiction/OUP/Castro/chY.txt
non-fiction/OUP/Castro/chZ.txt
non-fiction/OUP/Fletcher/ch1.txt
non-fiction/OUP/Fletcher/ch10.txt
non-fiction/OUP/Fletcher/ch2.txt
non-fiction/OUP/Fletcher/ch5.txt
non-fiction/OUP/Fletcher/ch6.txt
non-fiction/OUP/Fletcher/ch9.txt
non-fiction/OUP/Kauffman/ch1.txt
non-fiction/OUP/Kauffman/ch10.txt
non-fiction/OUP/Kauffman/ch3.txt
non-fiction/OUP/Kauffman/ch4.txt
non-fiction/OUP/Kauffman/ch5.txt
non-fiction/OUP/Kauffman/ch6.txt
non-fiction/OUP/Kauffman/ch7.txt
non-fiction/OUP/Kauffman/ch8.txt
non-fiction/OUP/Kauffman/ch9.txt
non-fiction/OUP/Rybczynski/ch1.txt
non-fiction/OUP/Rybczynski/ch2.txt
non-fiction/OUP/Rybczynski/ch3.txt
```

On the other hand, I tried filtering to find just the directories by using `-type d`:
`$ find non-fiction/OUP -type d`

This was the output:

```
non-fiction/OUP
non-fiction/OUP/Abernathy 
non-fiction/OUP/Berk      
non-fiction/OUP/Castro    
non-fiction/OUP/Fletcher  
non-fiction/OUP/Kauffman  
non-fiction/OUP/Rybczynski
```

## Command 2 - -and

The `-and` command, much like the common "and" operator found in many programming languages, allows you to find the directories to which two different parameters both apply.

For example, I used the command: 
`$ find non-fiction/OUP -name "ch1*" -and -type f`

This finds all of the files (not directories) starting with "ch1" within non-fiction/OUP.

The output was:

```
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch14.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Fletcher/ch1.txt
non-fiction/OUP/Fletcher/ch10.txt
non-fiction/OUP/Kauffman/ch1.txt
non-fiction/OUP/Kauffman/ch10.txt
non-fiction/OUP/Rybczynski/ch1.txt
```

Next, I used the command:
`$ find non-fiction/OUP -name "*c*" -and -type d`.

This searches for all directories with c in their names.

This was the output:

```
non-fiction/OUP/Fletcher
non-fiction/OUP/Rybczynski
```

## Command 3 - -or

Much like the common logical operator "or" in many programming languages, `-or` allows us to search for files or directories where EITHER parameter is true.

I took a look at the previous commands, but replaced `-and` with `or`.

First, I tried:

`$ find non-fiction/OUP -name "ch1*" -or -type f`

This was the output:

```
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch14.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/CH4.txt
non-fiction/OUP/Berk/ch7.txt
non-fiction/OUP/Castro/chA.txt
non-fiction/OUP/Castro/chB.txt
non-fiction/OUP/Castro/chC.txt
non-fiction/OUP/Castro/chL.txt
non-fiction/OUP/Castro/chM.txt
non-fiction/OUP/Castro/chN.txt
non-fiction/OUP/Castro/chO.txt
non-fiction/OUP/Castro/chP.txt
non-fiction/OUP/Castro/chQ.txt
non-fiction/OUP/Castro/chR.txt
non-fiction/OUP/Castro/chV.txt
non-fiction/OUP/Castro/chW.txt
non-fiction/OUP/Castro/chY.txt
non-fiction/OUP/Castro/chZ.txt
non-fiction/OUP/Fletcher/ch1.txt
non-fiction/OUP/Fletcher/ch10.txt
non-fiction/OUP/Fletcher/ch2.txt
non-fiction/OUP/Fletcher/ch5.txt
non-fiction/OUP/Fletcher/ch6.txt
non-fiction/OUP/Fletcher/ch9.txt
non-fiction/OUP/Kauffman/ch1.txt
non-fiction/OUP/Kauffman/ch10.txt
non-fiction/OUP/Kauffman/ch3.txt
non-fiction/OUP/Kauffman/ch4.txt
non-fiction/OUP/Kauffman/ch5.txt
non-fiction/OUP/Kauffman/ch6.txt
non-fiction/OUP/Kauffman/ch7.txt
non-fiction/OUP/Kauffman/ch8.txt
non-fiction/OUP/Kauffman/ch9.txt
non-fiction/OUP/Rybczynski/ch1.txt
non-fiction/OUP/Rybczynski/ch2.txt
non-fiction/OUP/Rybczynski/ch3.txt
```

This result is the same as all of the files in the directory, because everything with a name starting with "ch1" will be a file.

This was the next command I tried:
`find non-fiction/OUP -name "*c*" -or -type d`

This command outputs every file or directory with the letter c in it, and any directory regardless of its name.

These were the results:

```
non-fiction/OUP
non-fiction/OUP/Abernathy
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch14.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Berk
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/ch7.txt
non-fiction/OUP/Castro
non-fiction/OUP/Castro/chA.txt
non-fiction/OUP/Castro/chB.txt
non-fiction/OUP/Castro/chC.txt
non-fiction/OUP/Castro/chL.txt
non-fiction/OUP/Castro/chM.txt
non-fiction/OUP/Castro/chN.txt
non-fiction/OUP/Castro/chO.txt
non-fiction/OUP/Castro/chP.txt
non-fiction/OUP/Castro/chQ.txt
non-fiction/OUP/Castro/chR.txt
non-fiction/OUP/Castro/chV.txt
non-fiction/OUP/Castro/chW.txt
non-fiction/OUP/Castro/chY.txt
non-fiction/OUP/Castro/chZ.txt
non-fiction/OUP/Fletcher
non-fiction/OUP/Fletcher/ch1.txt
non-fiction/OUP/Fletcher/ch10.txt
non-fiction/OUP/Fletcher/ch2.txt
non-fiction/OUP/Fletcher/ch5.txt
non-fiction/OUP/Fletcher/ch6.txt
non-fiction/OUP/Fletcher/ch9.txt
non-fiction/OUP/Kauffman
non-fiction/OUP/Kauffman/ch1.txt
non-fiction/OUP/Kauffman/ch10.txt
non-fiction/OUP/Kauffman/ch3.txt
non-fiction/OUP/Kauffman/ch4.txt
non-fiction/OUP/Kauffman/ch5.txt
non-fiction/OUP/Kauffman/ch6.txt
non-fiction/OUP/Kauffman/ch7.txt
non-fiction/OUP/Kauffman/ch8.txt
non-fiction/OUP/Kauffman/ch9.txt
non-fiction/OUP/Rybczynski
non-fiction/OUP/Rybczynski/ch1.txt
non-fiction/OUP/Rybczynski/ch2.txt
non-fiction/OUP/Rybczynski/ch3.txt
```

Because all of the text files contain the letter c, all of the text files were output. But there were also some directories output which did not contain the letter c, such as Kauffman.

## Command 4 - -not

This command allows us to search for files or directories without certain properties. For example:

`find non-fiction/OUP -name "*c*" -not -name "ch1*"`

This will serach for all files and directories in non-fiction/OUP which contain the letter c, but do not start with "ch1".
This is the output:

```
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/ch7.txt
non-fiction/OUP/Castro/chA.txt
non-fiction/OUP/Castro/chB.txt
non-fiction/OUP/Castro/chC.txt
non-fiction/OUP/Castro/chL.txt
non-fiction/OUP/Castro/chM.txt
non-fiction/OUP/Castro/chN.txt
non-fiction/OUP/Castro/chO.txt
non-fiction/OUP/Castro/chP.txt
non-fiction/OUP/Castro/chQ.txt
non-fiction/OUP/Castro/chR.txt
non-fiction/OUP/Castro/chV.txt
non-fiction/OUP/Castro/chW.txt
non-fiction/OUP/Castro/chY.txt
non-fiction/OUP/Castro/chZ.txt
non-fiction/OUP/Fletcher
non-fiction/OUP/Fletcher/ch2.txt
non-fiction/OUP/Fletcher/ch5.txt
non-fiction/OUP/Fletcher/ch6.txt
non-fiction/OUP/Fletcher/ch9.txt
non-fiction/OUP/Kauffman/ch3.txt
non-fiction/OUP/Kauffman/ch4.txt
non-fiction/OUP/Kauffman/ch5.txt
non-fiction/OUP/Kauffman/ch6.txt
non-fiction/OUP/Kauffman/ch7.txt
non-fiction/OUP/Kauffman/ch8.txt
non-fiction/OUP/Kauffman/ch9.txt
non-fiction/OUP/Rybczynski
non-fiction/OUP/Rybczynski/ch2.txt
non-fiction/OUP/Rybczynski/ch3.txt
```

The next command I tried was:

`$ find non-fiction/OUP -name "*h*" -not -type f`

This searches for everything containing the letter h in the name, but excludes files (so it searches for directories).

The output is:

```
non-fiction/OUP/Abernathy
non-fiction/OUP/Fletcher
```
