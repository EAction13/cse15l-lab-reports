# Week 2 Lab Report - Servers and Bugs

## Part 1 - StringServer

I used the provided folder wavelet and its files as a base for creating StringServer.java. 
I made no changes to Server.java so I will not include it in my screenshots. 
Here is the code for StringServer.java (I modified NumberServer.java to write it).

```
import java.io.IOException;
import java.net.URI;
import java.util.*;



class Handler implements URLHandler {
    /*
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    int num = 0;
    */

    ArrayList<String> strList = new ArrayList();

    public String handleRequest(URI url) {
        
        //String temp = "";
        //The default page with no extra path just shows the number
        if (url.getPath().equals("/")) {
            String temp = "";
            for(int i = 0; i < strList.size(); i++){
                temp += strList.get(i);
                temp += "\n";
            }
            return temp;
        } /*
        //The path /increment adds 1 to the number and displays "Number incremented!"
        else if (url.getPath().equals("/increment")) {
            num += 1;
            return String.format("Number incremented!");
        } 
        //Allows the user to add a number to the current number
        //by entering it as a query after the path /add.
        else {*/
            

            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    strList.add(parameters[1]);

                    String temp = "";
                    for(int i = 0; i < strList.size(); i++){
                        temp += strList.get(i);
                        temp += "\n";
                    }
                    return temp;
                }
            }
            
            //If the URL is not any of the valid operations, return an error message
            return "404 Not Found!";
        //}
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

I set up the server and tried using /add-message twice:
![image](https://user-images.githubusercontent.com/122485081/215658616-418f5cd2-8018-4800-857b-89ae5b2c7848.png)

![image](https://user-images.githubusercontent.com/122485081/215658840-270c2c5c-4ff5-4ff8-b421-c8f5a9d0a4c7.png)

In both of these screenshots, the same methods are called and the same fields are changed.
The method main() in the class StringServer was called when setting up the server using the terminal.
Each time a new URL is used, handleRequest(URI url) is called.
Each time we use /add-message, the string in the URL is added to the ArrayList strList.
strList is declared outside of the method handleRequest, so that it does not get overwritten every time a URL is used.
To return strList, I made a new String called temp every time a valid URL is given. A for loop is used to copy the contents of strList into temp, including a newline after every element.

## Part 2 - Debugging in Lab 3

In this lab report, I will look at how I debugged the method `averageWithoutLowest(double[] arr)` from ArrayExamples.java.

**Failure-inducing input:**
When I input an array with all of the numbers the same, the test did not pass:

![image](https://user-images.githubusercontent.com/122485081/215664839-3d0bdde1-af6c-472b-8a19-ee75b06cc5bc.png)

**Successful tests:**
When I input this empty array, the test passed - the output was 0 as expected.

![image](https://user-images.githubusercontent.com/122485081/215663259-51fb8c8e-d019-42b2-84f0-0a47daa99226.png)

The output was also 0, as expected, when I input an array with only one element.
After that, I input arrays with multiple values, where all of the values were different. These tests also gave the expected results.

**Symptoms:**
The failure-inducing input gave this result:

![image](https://user-images.githubusercontent.com/122485081/215665092-58af4963-0ab5-4aae-990d-9a7f93535aa2.png)

The average of an array full of the same number should be that same number. However, the result given was 0.

**Bugs:**
I noticed that, because of the portion of the code that is underlined in this image, the value determined to be the lowest will be skipped every time it occurs in the array, rather than just once.

![image](https://user-images.githubusercontent.com/122485081/215666131-f3cb7fa3-7a69-465e-b826-f51385e2fe4e.png)

To fix this, I made a boolean variable that functions as a flag - once the lowest value has been left out, the rest will be summed without comparing them.
This is my edited code:

![image](https://user-images.githubusercontent.com/122485081/215666535-d2f51d19-77fe-4e33-a6fe-2e841637f80c.png)

## Part 3 - Something new I learned
Despite taking a Java class before, I did not know about JUnit and its usefulness in debugging.
I think it is a very useful tool in writing and running tests in an organized manner.
I also did not know how to create a web server in Java until this class.
