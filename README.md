# Simple C++ Chat App (Winsock)

A lightweight Windows chat app built with **C++** and **Winsock2**. This repository contains a server and a client that communicate over TCP, support multiple chat rooms, private messages, undo/redo, and message search.

## What This Project Does
- Creates a TCP chat server using Winsock
- Allows multiple clients to connect concurrently
- Supports chat rooms and private messaging
- Keeps recent message history for each room
- Lets users undo and redo their last message
- Provides search inside room history

## Files Included
- `main_server.cpp` — chat server logic and room/message handling
- `main_client.cpp` — interactive chat client
- `README.md` — this documentation

## Requirements
- Windows OS
- C++ compiler with C++17 support
- Winsock2 library (`-lws2_32`)
- Optional: MinGW or Visual Studio command prompt

## Build Instructions
Open a command prompt in the project folder and run:

Compile the server:
```bash
g++ main_server.cpp -o server -lws2_32
```

Compile the client:
```bash
g++ main_client.cpp -o client -lws2_32
```

## Run the App
1. Start the server:
```bash
server
```
2. Start one or more clients:
```bash
client
```
3. Enter your username and server details when prompted.

## Client Usage
After connecting, use these commands:

```text
/join <room>           - Join or create a chat room
/pm <user> <message>   - Send a private message to a user
/reply <user> <msg>    - Reply to a user in the current room
/undo                  - Undo your last message
/redo                  - Redo your last undone message
/history               - Show recent messages in the current room
/search <keyword>      - Search messages in the current room
/quit                  - Leave the chat and exit
/help                  - Display the help menu
```

## Example Workflow
1. Run `server`
2. Open a second prompt and run `client`
3. Join a room: `/join lobby`
4. Send a message by typing normally
5. Use `/history` to view recent room messages
6. Use `/search hello` to find messages containing `hello`

- Use the same port on all clients.
- Use `/help` in the client anytime for the full command list.

## Cleanup Note
This README has been rewritten to remove any original author metadata and give a clean, easy-to-follow guide for this project.

