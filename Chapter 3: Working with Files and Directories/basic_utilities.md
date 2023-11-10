## Create, Move, and Copy

Create an empty file and a directory. 
Use touch to create an empty file and mkdir to create a directory.

cat: used to type out a file (or combine files).
head: used to show the first few lines of a file.
tail: used to show the last few lines of a file.
man: used to view documentation.


man head | head

Most input lines entered at the shell prompt have three basic elements

Command
Options -p --print
Arguments

# First bash script
#!/bin/bash
echo 'Hello $(whoami), your id: $(id)'

# TODO: Variables 
name='James'
age=21

echo "$(age) old me is older than $(name)."

