# Task0
### Make a server and a client. Start the server on port 12345. Establish a client connection to it. The client should send a textual message on a line to the server. The server should send the line back, and the client should print it

## Client side
### Client accept a number or word fron the user.
### 1. Scanner Object is needed.
#### Scanner sc = new Scanner(System.in);
### 2. We need a Socket("for communicateion between the Client and Server")
#### simple socket takes two parameter(port number and ip address).
Socket s = new Socket(12345,"127.0.0.1")
### 3. Accepting something from the server.
#### Scanner sc1 = new Scanner(s.getInputStream());
### 4 . Enter number or word from the user.
System.out.println("Enter a number");
#### use Scanner to accept the number.
number = sc.nextInt();
#### store the number in a number variable
int number;
### 5 . passing the number to the Server.create a printStream object.
PrintStream p = new PrintStream(s.getOutputStream());
#### passing the number to the client.
p.println(number);
#### Accepting and printing out the result.
Create another int to store the result
int temp = sc1.nextInt();
System.out.println(temp);


