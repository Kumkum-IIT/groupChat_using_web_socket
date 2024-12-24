# Group Chat Django

This project is a real-time group chat application built using Django, Django Channels, and WebSockets. Users can create or join chat rooms and exchange messages instantly.

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/group-chat-django.git
   cd group-chat-django
## Install requiements
pip install -r requirements.txt

## Run the application using Daphne:
daphne -b 0.0.0.0 -p 8001 web_socket.asgi:application
(if server is running on port 8001)

## Project Structure
1. views.py: Contains views for creating chat rooms and rendering the chat room page.
2. consumers.py: Defines the WebSocket consumer that handles real-time communication between clients in a chat room.
3. models.py: Contains the Room model representing a chat room.
4. urls.py: Maps the URLs to the corresponding views.
5. routing.py: Defines the routing for WebSocket connections.
6. templates/: Contains HTML templates for the chat interface.
7. 
# WebSocket Communication
The real-time chat functionality is implemented using Django Channels and WebSockets. Below is an overview of how WebSocket communication is handled:

Connection: When a user connects to a chat room, a WebSocket connection is established, and the user is added to a group corresponding to that room.

# Message Handling:

- receive: When a message is received from a client, it is broadcasted to all clients in the same group (chat room).
- chat_message: This method handles sending the message to the WebSocket, which is then displayed to all connected users.
- Disconnection: When a user disconnects, they are removed from the group.

Running the Application
Create or Join a Chat Room:

Go to the home page and enter a room name to create or join a chat room.
Send Messages:

Once in a room, users can send messages in real-time that will be visible to all participants in the room.

## Contributing
Contributions are welcome! Please submit a pull request or open an issue if you have any suggestions or find any bugs.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.
