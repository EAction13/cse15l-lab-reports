# Lab Report 4

## Step 4 - logging into ieng6

My first input was `$ ssh cs15lwi23aju@ieng6.ucsd.edu`, and then I entered my password after being prompted.

This was the output:

![image](https://user-images.githubusercontent.com/122485081/221766617-56b1b751-e75d-44a4-ab75-6bce9e3aa9a2.png)
![image](https://user-images.githubusercontent.com/122485081/221766741-240e1941-b2c5-49bf-9791-05a5861306d9.png)

## Step 5 - cloning fork of lab7 repository

I typed `git clone`, then pasted the link to my fork of the repository from github. 
Overall, the command was: `$git clone https://github.com/EAction13/lab7.git`

![image](https://user-images.githubusercontent.com/122485081/221768410-5734ffc5-ce6e-4e02-94e1-d11b343acc70.png)

## Step 6 - running the tests

First I typed `$ cd lab7` to move into the lab7 directory.

![image](https://user-images.githubusercontent.com/122485081/221770122-3d42ea0d-210d-44d0-81ea-b99147db8523.png)

Next I copy-pasted `$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` from the week 3 page.

![image](https://user-images.githubusercontent.com/122485081/221770235-78609e46-0439-431e-9ea6-58720cd79552.png)

Then I typed `ls` to see the names of the files in lab7.

![image](https://user-images.githubusercontent.com/122485081/221770903-19a435f6-7294-4d0f-9661-a9eb99d701d6.png)

Then I copied and pasted the command to run the JUnit tests from the same page, and fixed the file name to run TestListExamples.class.

`$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`

![image](https://user-images.githubusercontent.com/122485081/221770658-dbc49f93-36bf-49df-bbf7-9bbbb1c23d0c.png)

## Step 7 - editing the code

First, I used `$ nano ListExamples.java`.

![image](https://user-images.githubusercontent.com/122485081/221771382-60d516e0-b9f7-4fa4-83cf-ca9758f20f47.png)

I then navigated toward the bottom of the page with the arrow keys, and replaced the 1 in index1 with 2:

![image](https://user-images.githubusercontent.com/122485081/221771572-c02edd91-b6d3-46ed-8f91-987366cc657d.png)

I then pressed ctrl+o to save:

![image](https://user-images.githubusercontent.com/122485081/221771760-6308090a-d2c6-466b-89ae-0e529225c500.png)

I pressed enter to confirm the file name, then pressed ctrl+x to exit nano.

## Step 8 - re-running the tests

To execute the command `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`, I pressed `<up> <up> <up> <up> <enter>`.

![image](https://user-images.githubusercontent.com/122485081/221772438-03af347e-2e23-4467-84a7-e47ced04cde1.png)

Next, to execute `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples`, I pressed `<up> <up> <up> <enter>`.

![image](https://user-images.githubusercontent.com/122485081/221772718-f5ac76e0-d341-41ee-a8b1-f895190347ce.png)

## Step 9 - commit and push

First I typed `$ git add ListExamples.java`, because ListExamples.java is the only relevant file we made changes to.

![image](https://user-images.githubusercontent.com/122485081/221773525-c5806faa-c84e-4f4f-910d-1b2208daece3.png)

Next I used `$ git commit -m "yeet"`:

![image](https://user-images.githubusercontent.com/122485081/221773920-f4daf12d-6ea1-4fd1-9bb9-a31aa0544e00.png)

I then used `$ git push` and typed my Github username and password when prompted. I believe there was an error because I did not set up the SSH key on this device.

![image](https://user-images.githubusercontent.com/122485081/221774678-d52e89ca-d3e7-4edc-a481-93b5072b8865.png)

