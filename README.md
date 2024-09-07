# File/Folder Protection Software

This is a simple **File/Folder Protection Software** written in C, which allows you to hide and show files or folders on your system. This program uses the DOS `_chmod` function to change the file attributes, making files or folders hidden or visible.

## Features
- **Hide Files/Folders**: Enter the full path of a file or folder to make it hidden from the system.
- **Show Files/Folders**: Restore hidden files or folders by making them visible again.
- **Help Section**: A brief guide on how to input the correct file path and name.
  
## How to Use
1. **Launch the program**: The menu provides three options:
   - `1: Hide a file/folder`
   - `2: Show a file/folder`
   - `3: Help`

2. **Hide a File/Folder**:
   - Choose option `1`.
   - Input the full path of the file or folder you want to hide (e.g., `C:\folder\file.txt`).
   - If successful, the file/folder will be hidden.

3. **Show a File/Folder**:
   - Choose option `2`.
   - Input the full path of the hidden file or folder to restore it to visible.
   - If successful, the file/folder will become visible again.

4. **Help**: 
   - Option `3` provides guidance on how to enter file/folder paths correctly.
   - Ensure the file extension is included when entering file paths.

### Input Format
- When asked for a file or folder path, input it in the following format:
  - For files or folders on the **E drive**: `E:\\filename.txt` or `E:\\foldername`

> **Note**: Providing the correct file extension is necessary when hiding or showing files.

## Requirements
- **Turbo C** or **Borland C** Compiler with support for the DOS `conio.h` and `dos.h` libraries.
- Compatible with DOS-based systems.

### Compilation Command
```bash
gcc protection.c -o protection -lconio -ldos
```

## How It Works
The program makes use of the DOS function `_chmod()` to change file attributes:
- **Hiding a file/folder**: Changes the file's attributes to system, hidden, and read-only.
- **Showing a file/folder**: Resets the file's attributes, making it visible again.

### Functions Used:
- `_chmod()`: Modifies the attributes of a file or folder.
- `cprintf()`, `gotoxy()`: Functions for handling text output and positioning in a text-based user interface.
- `clrscr()`, `delay()`, `getch()`: Utility functions for clearing the screen, adding delays, and capturing user input.

## Future Enhancements
- **Password Protection**: Add an option to password protect the software to restrict access to hiding/showing files.
- **Logging**: Implement a log to track all hidden and shown files with timestamps.
- **Graphical Interface**: Move from a text-based interface to a simple graphical user interface (GUI).

## Contributing
Feel free to submit issues or feature requests, or open a pull request to contribute to the project.
