# Lab Report 2
## part 1
The server is constructed using the Server class used in the lab. Therefore, the main method works the same with valid/invalid arguments. The main method constructs the server on the local machine using the port number given to the terminal. The terminal will start the server after compiling and providing a port number. After the terminal starts the server we are provided with an alert "server started", then we can open the web server from the local machine by using localhost:4040 (port). The following chat commands will be written directly in the search bar using paths and queries. 
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    private ArrayList <String> chatMessages = new ArrayList<String>();

    public String handleRequest(URI url) {
        if(url.getPath().equals("/")){
            return"welcome to the server";

        }else{
            if (url.getPath().equals("/add-message")) {
                return segmentString(url);
            } else {
                return "invalid";
            }
        }
    }

    public String segment(URI url){
        String [] user = url.getQuery().split("&")[1].split("=");
        String [] message = url.getQuery().split("&")[0].split("=");
        if(message[0].equals("s") && user[0].equals("user")){
            return user[1] + ": " + message[0]+ "\n";
        }else {
            return "invalid";
        }

    }

}

class ChatServer {
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
### Using valid queries
![Valid2](ValidChatServer2.png)
- After the port number we can specify a custom path that the ```handleRequest(URI)``` will use to make requests like printing a conversation.
- The path specified was ```/add-message?``` which alerts the method that the following components of the URI will be a query.
- Then a segment method will take in the URI and segment the URL after the query into user and message variables.
- The ```segment(URI)``` will return a string with the user and message variables in ```user: message``` format.
- fields in the ```handleRequest(URI)``` are not changed. The URI will be sent to the segment method where ```.getQuery()``` and ```.split()``` methods are used to set the string value of the user/message fields.
  - However, if the server's URI is edited, the ```handleRequest(URI)``` will call ```segment(URI)``` and the message/user string fields will be updated to match the new inputs to the query. 
### Using invalid queries
![Invalid](InvalidChatServer.png)
- After the port number we can specify a custom path that the ```handleRequest(URI)``` will use to make requests like printing a conversation.
- If the path is unrecognized in the ```handleRequest(URI)``` it will return invalid
- If the path is recognized it will be sent to the ```segment(URI)```.
- The ```segment(URI)``` will return invalid if the user/message variables do not exist in the URI.
- In the server snippet above, the path was unrecognized as it was ```add?``` not ```add-message?```. Thus, it directly returned invalid without calling the ```segment(URI)```.
- The ```handleRequest(URI)``` does not change any fields because it detects if the URI has a recognized path, and a correct syntax for the query, and then sends the URI into the ```segment(URI)```.
- In case of an invalid query such as the one above, ```handleRequest(URI)``` will not call ```segment(URI)``` and the relevant user/message string fields will not be updated.
- In case of invalid inputs, ```handleRequest(URI)``` will call ```segment(URI)```. however, the inputs will not match the correct ones ```s= , user= ```, so it will return ```"invalid"``` directly without affecting relevant fields. 
## part 2
### Absolut path to private key
![Private](AbsolutePathPrivateKey.png)
```
ghida04@MacBook-Pro-5 .ssh % find $PWD -type f | grep "id_rsa"  
/Users/ghida04/.ssh/id_rsa
/Users/ghida04/.ssh/id_rsa.pub
```
- The path to the private key id_rsa is shown above. 
### Absolut path to public key
![Public](AbsolutePathPublicKey.png)
```
[galruwais@ieng6-203]:.ssh:90$ find $PWD -type f | grep "id_rsa.pub"
/home/linux/ieng6/oce/07/galruwais/.ssh/id_rsa.pub
```
- The path to the public key id_rsa.pub is shown above.
### Accessing ieng6 account without passcode
![Access](AccountLogIn.png)
## part 3
I didn't know how to create a Java web server using HTTP. Therefore, the number, search, and chat server showed me how to implement the server class with custom requests by utilizing getPath(), getQuery(), and split methods.
