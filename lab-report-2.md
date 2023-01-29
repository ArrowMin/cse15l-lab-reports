# Lab Report 2

Code for StringServer
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String homepage = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return homepage;
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    homepage += parameters[1] + "\n";
                    return homepage;
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if (args.length == 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```
![Image](images/LR2Image2.png)

When first loading the web server, the main method is called. Then, when loading the webpage onto the browser, the handleRequest method is called. The relevant arguments for the main method is the port number in the command line, and the relevant argument for the handleRequest method is http://localhost:4000/add-message?s=Helllooooooo. In the command line argument, the port number 4000 is converted from a String to an int value. For the handleRequest method, the argument is changed from an URI to a String value.

![Image](images/LR2Image3.png)

The handleRequest method is called. The relevant arguments for the handleRequest method is http://localhost:4000/add-message?s=Heyyyyyyyyy/. In the handleRequest method, the argument is changed from an URI to a String value.
