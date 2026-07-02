# Chat Application in C++ (Winsock)

[![C++](https://img.shields.io/badge/Language-C++-blue.svg)](https://isocpp.org/)

A Windows-based chat application implemented in **C++** using **Winsock2**. This project supports:
- multi-room chat
- private messaging
- undo/redo on sent messages
- searchable room history
- multithreaded handling of multiple clients

---

## Features
- **Multi-room chat**: Join existing rooms or create new rooms dynamically
- **Private messaging**: Send direct messages between users
- **Undo / Redo**: Undo your last message and restore it if needed
- **Message history**: View recent messages inside the current room
- **Search**: Search room history for keywords
- **Help menu**: Built-in command list for client usage
- **Clean exit**: `/quit` closes the client gracefully

---

## Project Structure
- `main_client.cpp` — client application source
- `main_server.cpp` — server application source
- `README.md` — this documentation

---

## Requirements
- Windows 10 / 11
- C++ compiler with C++17 support
- Winsock2 library (`-lws2_32`)

---

## Build & Run

### Compile the server
```bash
g++ main_server.cpp -o server -lws2_32
```

### Compile the client
```bash
g++ main_client.cpp -o client -lws2_32
```

### Run the server
```bash
server
```

### Run the client
```bash
client
```

When the client starts, enter your username, the server hostname or IP (for example `127.0.0.1`), and the server port (for example `8080`).

---

## Client Commands

Use these commands inside the client after connecting to the server:

```text
/join <room>           - Join or create a chat room
/pm <user> <message>   - Send a private message to a user
/reply <user> <msg>    - Reply to a user in the current room
/undo                  - Undo your last message
/redo                  - Redo your last undone message
/history               - Display message history for the current room
/search <keyword>      - Search room messages for a keyword
/quit                  - Disconnect from the chat server
/help                  - Display this help menu
```

---

## Notes
- The server and client are designed for local Windows development and testing.
- Make sure the server is running before you connect with a client.
- If you use MinGW, install a compiler that supports Winsock and C++17.

---

## No Original Author Name
This README is updated to remove any original author credit and focus on how to build and use the application.

