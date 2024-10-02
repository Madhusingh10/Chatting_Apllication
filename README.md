This chat application project is built in Java using a client-server architecture, where two programs (Client and Server) communicate over a network using sockets. The graphical user interface (GUI) is implemented using Swing components, while message formatting and transmission between the client and server occur through the use of input-output streams.

Tech Stack and Components:

Java:

Java is used for the overall implementation, including the networking and GUI. It provides libraries for socket programming, I/O streams, and threading, which are essential for building client-server applications.

Swing (GUI):

JFrame: The main window is created using JFrame for both client and server.
JPanel: Different sections like the header, message area, and input field are arranged using JPanel.
JTextField: Used for the message input field, allowing the user to type messages.
JButton: The "Send" button triggers the action to send the message.
JLabel: Labels are used to display various elements, such as user names, profile images, and the actual chat messages.
BoxLayout and BorderLayout: Used for organizing the components like the chat messages and input areas in a structured manner.

Sockets (Networking):

Socket (Client): The client connects to the server using a socket connection at IP 127.0.0.1 (localhost) and port 6166. It is responsible for sending and receiving messages.

ServerSocket (Server): The server listens for incoming client connections on port 6166 and accepts client requests, establishing communication.

DataOutputStream and DataInputStream: These streams are used to send and receive messages in UTF format between the client and server.

ActionListener (Event Handling):

The ActionListener interface is used to handle button click events, such as sending a message when the "Send" button is clicked. It is also responsible for adding the message to the chat interface and sending it to the server.

Message Formatting:

Messages are encapsulated in JPanel objects with customized formatting. The message is wrapped in an HTML-like structure for better text presentation using JLabel.

Time Stamps: Each message is appended with a timestamp generated using SimpleDateFormat and Calendar, which formats the current time of the message.

Code Breakdown:
Client:

The client initiates a connection with the server using sockets and provides a graphical interface where the user can input and send messages.
The GUI components are laid out using JPanel, and the "Send" button triggers the actionPerformed method to send the message.
Incoming messages from the server are continuously read using DataInputStream and displayed in the chat panel.
Server:

The server waits for a client to connect using ServerSocket and handles incoming messages from the client through DataInputStream.
Messages received from the client are displayed in the server's chat window using similar formatting to the client side.
The server also uses DataOutputStream to send messages back to the client.

Flow:
The Client connects to the Server using a socket.
Both Client and Server continuously listen for messages via DataInputStream and respond by sending messages through DataOutputStream.

The user interface on both sides updates dynamically as new messages are exchanged.
This project showcases the core principles of real-time messaging using sockets, basic UI design with Swing, and the handling of user interactions through event listeners.
