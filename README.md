This chat application is built in Java using a client-server architecture, where the Client and Server communicate via sockets. The GUI is designed with Swing components, including JFrame, JPanel, JTextField, JButton, and JLabel.

Java handles networking, I/O streams, and threading, using Socket for the client and ServerSocket for the server.
Swing creates a graphical interface with organized layouts (BoxLayout, BorderLayout), and buttons handle user interactions via ActionListener.

Networking: The client connects to localhost on port 6166, and the server listens and communicates via DataOutputStream and DataInputStream.

Message Formatting: Messages are encapsulated in JPanel objects and formatted with HTML-like structures, including timestamps.

The client sends and receives messages from the server, and both sides dynamically update the chat window in real time.
![Screenshot (1299)](https://github.com/user-attachments/assets/352ea9f6-3882-47e8-b0be-a6bddbfcc683)


