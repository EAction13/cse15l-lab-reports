# Lab Report 3 - Researching commands

The command I chose to research is `less`. 

## Command 1 - Using *

By using * in the path that I was trying to scroll through, I was able to scroll through multiple files using the one command.

I used this command: `$ less non-fiction/OUP/Abernathy/*.txt`

![image](https://user-images.githubusercontent.com/122485081/218652969-dbb125fd-d30a-4c12-9537-ceca60134b48.png)

![image](https://user-images.githubusercontent.com/122485081/218653013-39c865dd-910e-43d0-9437-2370c8e504ff.png)

This function is very useful if there are a lot of short text files within one directory.

Another example:

![image](https://user-images.githubusercontent.com/122485081/218653454-f24a3911-7c23-4e2b-99c9-76ea66675596.png)

![image](https://user-images.githubusercontent.com/122485081/218653418-06151055-eb30-4a8c-b0af-8510c94ddb98.png)


## Command 2 - -N

By using the -N command, the number representing the line is displayed next to the text.

I used the command: `$ less -N non-fiction/OUP/Abernathy/ch1.txt`

![image](https://user-images.githubusercontent.com/122485081/218654199-730687cd-eb9f-4695-a8b2-e9309d61a17e.png)

This function is useful when scrolling through long files if you want to look at a specific line, but there are too many to count.

Here is another example:
`$ less -N non-fiction/OUP/Kauffman/ch1.txt`

![image](https://user-images.githubusercontent.com/122485081/218654769-4142e123-06f0-468f-92ad-4f79514d4957.png)

## Command 3 - -X

The -X command leaves the text from the file you scrolled through in the terminal rather than clearing it.

![image](https://user-images.githubusercontent.com/122485081/218656509-3385706f-0209-4fc1-8c35-7f0af3b876e6.png)

This is useful if you are scrolling through the file to find specific information that you can use in the terminal or your code later on.

Another example:

![image](https://user-images.githubusercontent.com/122485081/218657349-dd4def3f-b707-4965-a040-fd0d8acb1a05.png)

## Command 4 - /pattern

While scrolling through a file using `less`, typing / followed by some text will search for that text and highlight it.

I tried `$ less -X non-fiction/OUP/Castro/chA.txt` and then `/the`:

![image](https://user-images.githubusercontent.com/122485081/218657821-7a5bc5be-765b-4446-924f-1e00a24e2f1d.png)

This is useful when searching for mentions of specific words or strings.

Another example: 
I used `$ less non-fiction/OUP/Abernathy/ch2.txt` and `/and`.

![image](https://user-images.githubusercontent.com/122485081/218658413-35471644-8b88-4caa-aa48-9eb1247a1734.png)

