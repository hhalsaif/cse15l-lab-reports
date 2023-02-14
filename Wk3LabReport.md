# Part 1
Server.java file
```
import java.io.IOException;
import java.io.OutputStream;
import java.net.InetSocketAddress;
import java.net.URI;

import com.sun.net.httpserver.HttpExchange;
import com.sun.net.httpserver.HttpHandler;
import com.sun.net.httpserver.HttpServer;

interface URLHandler {
    String handleRequest(URI url);
}
class ServerHttpHandler implements HttpHandler {
    URLHandler handler;
    ServerHttpHandler(URLHandler handler) {
      this.handler = handler;
    }
    public void handle(final HttpExchange exchange) throws IOException {
      HttpServer server = HttpServer.create(new InetSocketAddress(port), 0);

          //create request entrypoint
          server.createContext("/", new ServerHttpHandler(handler));

          //start the server
          server.start();
          System.out.println("Server Started! Visit http://localhost:" + port + " to visit.");
      }
}
```
StringServer.java file
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
class Handler implements URLHandler {
    // The one bit of state on the server: a number that will$
    // various requests.
    ArrayList<String> messages = new ArrayList<>();
    public String handleRequest(URI url) {
        String[] messagePart = url.getQuery().split("=");
        messages.add(String.format("%s\n", messagePart[1]));
        String message = "";
        for(String i:messages)
          message += i;
        return message;
    }
}
class StringServer {
    public static void main(String[] args) throws IOException$ {
       if(args.length == 0){
        System.out.println("Missing port number! Try any $
        return;
       }

      int port = Integer.parseInt(args[0]);
      Server.start(port, new Handler());
      }
}
```

![image](https://user-images.githubusercontent.com/53378715/218650435-f4ffa944-009b-477e-9856-4f7bca074f54.jpeg)

![image](https://user-images.githubusercontent.com/53378715/218651908-d58a96a8-8ab6-458c-bd37-291ec7c0f35b.jpeg)

The code start by running the main method and then goes on to call the Server class and run the start command and passing it a handler object and the port number which is specified during runtime. Finally it gets triggered when the server call is recieved. When a new server query is triggered it takes in the query and saves it to a predefined array list which is finally turned into a response and sent back to the user client.

# Part 2

Test
```
  @Test
  public void testReverseInPlace() {
    int[] input1 = { 0, 1, 0 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 0,1,0 }, input1);
	}
```

```
  @Test 
  public void testReverseInPlace2(){    
    int[] input2 = {1, 2, 3};
    ArrayExamples.reverseInPlace(input2);
    int[] answer2 = {3, 2, 1};
    assertArrayEquals(input2, answer2);
  }
```
Bugs
![image](https://user-images.githubusercontent.com/53378715/218646517-7a30836a-913f-475b-b449-698d279c78d6.png)

Code Before Fix

```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
```

Code After Fix
```
  static void reverseInPlace(int[] arr) {
    int[] tempArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
       tempArray[i] = arr[arr.length - i - 1];
    }
    for(int i=0; i < tempArray.length; i++)
         arr[i] = tempArray[i];
  }
```
![image](https://user-images.githubusercontent.com/53378715/218649990-ab17d331-2c14-4976-82cf-c80631975847.jpeg)


# Part 3
I learned how to split a query in java to create a URL handler. The way the web works has always been interesting to me and while I know how URLs work and how to handle them in languages like python and javascript through this class and throughout the last two weeks I now know how to handle URLs in java.
