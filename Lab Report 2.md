# Lab Report 2

## Part 1
The code for the Simplest Search Engine is below:

In the file SearchEngine.java the code was

```java
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> strings = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Add a string!");
        } else if (url.getPath().equals("/add")) {
            String[] parameters = url.getQuery().split("=");
            if(parameters[0].equals("s"))
            {
                strings.add(parameters[1]);
                return String.format("You added " + parameters[1]);
            }
        } else {
            String returnString = "";
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/search")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    String stringToLookFor = parameters[1];
                    for(String s : strings){
                        if(s.contains(stringToLookFor)){
                            returnString += s;
                            returnString += "\n";
                        }
                    }

                    return String.format(returnString);
                }
            }
        }

        return "404 Not Found";
    }
}

class SearchEngine {
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
When you first start the server with a port number of your choice (4000 in this case), the load up or default screen is the screenshot below.

![Load Up Screenshot](Lab Report 2 Screenshots/Load Up Screenshot)

This is a list of of strings and you can add or search for Strings! Below is a screenshot of adding strings.

![Add Pineapple Screenshot](Lab Report 2 Screenshots/Add Pineapple Screenshot)

When you append `/add?s=pineapple` to the intial link of `localhost:4000`, the method of the second if statement below is called.
```java
else if (url.getPath().equals("/add")) {
            String[] parameters = url.getQuery().split("=");
            if(parameters[0].equals("s"))
            {
                strings.add(parameters[1]);
                return String.format("You added " + parameters[1]);
            }
        }
```

Since `url.getPath()` equals our `/add` this if statement is called. Then, the method will split the query where the equal sign is and place the two values into a String array. After `/add`, we are left with `?s=pineapple`. The query knows it starts at `?` and it will split the string at `=`, making the first element in the String array `s` and the second element in the String array `pineapple`. Then the program will make sure that the first String array element is `s`, then add the actual string (the one in the second element), `pineapple` into the ArrayList in the code. It will then print what was added. Every part of the path is relevant and missing a `/`, `?`, or `/add` provide an "404 Not Found" error instead. The only value that would change when trying to add a string is the string you want to add. As long as you start the whole path with `localhost:(your port number)/add?s=(your String)`, the request will process each one individually. 

We can add another string "apple".

![Add Apple Screenshot](Lab Report 2 Screenshots/Add Apple Screenshot)

I will also add the string "orange", but there won't be a screenshot for it. Now the ArrayList includes the strings ["pineapple", "apple", "orange"].

Say we want to search and see which strings that we added have the string "app" inside them. This would be from the custom search method we created (also an if statement). See the code below:

```java
else {
  String returnString = "";
  System.out.println("Path: " + url.getPath());
  if (url.getPath().contains("/search")) {
      String[] parameters = url.getQuery().split("=");
      if (parameters[0].equals("s")) {
          String stringToLookFor = parameters[1];
          for(String s : strings){
              if(s.contains(stringToLookFor)){
                  returnString += s;
                  returnString += "\n";
              }
          }
          return String.format(returnString);
      }
  }
}
```

In this case, 

