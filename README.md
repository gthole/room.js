RoomJS 3.x Game Engine
======================

This repository contains the RoomJS game engine (or server).

RoomJS is a modern Node.js-based [MUD](https://en.wikipedia.org/wiki/MUD)/[MOO](https://en.wikipedia.org/wiki/MOO) engine, where (privileged) players can extend everything while in game. The basic idea is that one can create and edit objects, locations and code from inside the game.

The engine includes built-in WebSocket (SocketIO) communication, user account management, flexible command parsing system and persistent on-disk storage.

Prerequisites
=============

The RoomJS server requires **Node.js 6.0** or upper.

Clone the repository or download a ZIP archive. 

Installation steps are straightforward:

1. `npm install`
2. Edit the `.env` file to customize the server listening port and the debug level (if need be), and just source it. (Also edit the path to the User DB and the path to world directory, if not using the lightweight demonstration world bundled with the project.)
3. `npm start`

To interact with the server, you must use a web client application. The standard [client](https://github.com/doughsay/room.js-client) is provided in a separate repository.

Main features
=============

These are but a few of all the things that you get just out-of-the-box:

- Modern **Playing**:
  - Connect and play simply using a web browser. *No need for good old telnet or third-party MUD client.*
  - Fully enjoy the leveraged experience, with colors and clickable links!

- Advanced **Scripting**:
  - Code your game in plain modern JavaScript (ES6), using a nice oriented-object design with inheritable traits, with all scripts running in sandboxes. *No need for proprietary custom programming languages.*
  - Edit your code directly in the browser, using the well-known in-browser code editor [CodeMirror](https://codemirror.net/) with syntax coloring and other neat features. *No need to leave the game in order to add features and hotboot your changes.*

- Flexible On-Disk  **Structure**:
  - All objects are stored in JSON format, in subdirectories along with their attached scripts in JS files: real easy to work with, or to parse for external usage if you ever need to quit the in-browser editing for any reason. *No need for custom file formats, YAML entities or other weird things.*
  - Name and organize your assets logically according to your own needs, without strong restrictions. *No imposed directory structure.*

- Easy **Communication** Channels:
  - Out-of-the box "Say" channel for the chatty ones, "Chat" channel and "Eval" mode for the developers.
  - Extensible and easily customizable mode system.

- Powerfull **Debugging**:
  - The game relies on [Bunyan](https://github.com/trentm/node-bunyan), a simple and fast JSON logging library, with a nice CLI for viewing and analyzing logs.

- Lightweight **Demonstration**:
  - The server is bundled with but a small demonstration, to illustrate a few possible ways of coding your own world. *No huge codebase with so many specific combat or leveling rules, or complex skill systems, that one would immediately get lost.*
  - Use it as a base, or wholly replace it, focussing on your own gaming logic! 

Demonstration world
===================

Live demonstration: http://roomjs.tk/

Documentation
=============

And it even comes with documentation...

- [Building and programming your own RoomJS MUD/MOO](doc/PROGRAMMING.md)
- [Organizing and customizing your world objects](doc/CUSTOMIZING.md)
- [A brief description of the demonstration mudlib](doc/DEMO_MUDLIB.md)
