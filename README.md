**Linux Shell - README**

**Overview**

This project is a custom shell application built in C. It allows users to execute various commands, including basic shell commands, file editing using a built-in vi-like editor, vector operations using threads, and handling pipes and background tasks. The shell also supports multi-line commands and offers some advanced features.

****Features****

**Basic Shell Commands:**

pwd: Print the current working directory.

cd <directory>: Change the working directory.

mkdir <directory>: Create a new directory.

ls <options>: List the contents of a directory.

exit: Exit the shell.

help: Display a list of supported commands.

**vi-like Editor:**

Open and edit files directly within the shell using the vi <filename> command.

Tracks and displays the number of lines, words, and characters in the file.

Save the file using Ctrl+S.

Exit the editor using Esc.

Vector Operations:

Perform addition, subtraction, and dot product operations on vectors stored in files.

**Commands:**

addvec <file1> <file2> -<threads>: Add vectors from two files using multithreading.

subvec <file1> <file2> -<threads>: Subtract vectors from two files.

dotprod <file1> <file2> -<threads>: Compute the dot product of vectors.

Specify the number of threads with the -<threads> option.

Piping:

Execute piped commands (e.g., ls | grep .c).

Background Execution:

Run commands in the background using &.

Multi-line Commands:

Support for multi-line input using \.

**Compilation and Execution**

**Prerequisites**

**GCC compiler**

ncurses and readline libraries installed on your system.

**Compilation**

To compile the program, use the following command:

gcc shell.c -o shell -lncurses -lreadline -lpthread -lm

Run the compiled shell using:

./shell

When you run the shell, you'll see a prompt: shell>.

Enter commands directly at the prompt.

**Example Commands**

**File Commands**

Display current directory: pwd

Change directory: cd /path/to/directory

Create a directory: mkdir my_directory

List files: ls -l

**Using the vi Editor**

Open a file for editing: vi myfile.txt

Edit the file, save changes using Ctrl+S, and exit using Esc.

**Vector Operations**

Add vectors from two files: addvec file1.txt file2.txt -4

Subtract vectors: subvec file1.txt file2.txt -2

Compute the dot product: dotprod file1.txt file2.txt -3

**Background Execution**

Run a command in the background: ls &

**Piped Commands**

Chain multiple commands: ls | grep .txt

**Multi-line Commands**

Use \ for multi-line input: echo "This is \
a multi-line \
command"

**Limitations**

The built-in vi editor is a simplified version and does not fully replicate the functionality of the standard vi editor.

Vector operations require the files to have the same number of elements.

Limited error handling for malformed input.

Background processes do not provide notifications upon completion.

**Future Improvements**

Expand vi editor features to include more standard functionality (e.g., search, delete, etc.).

Improve multi-threaded support for vector operations.

Add more advanced command parsing and error handling.

Support for redirection (>, <, >>).

**License**

This project is open-source and free to use. Modify and distribute as needed. Attribution is appreciated but not required.
