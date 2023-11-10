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
echo Hello $whoami, your id: $id

# TODO: Variables 
name='James'
age=21

echo $age old me is older than $name

# TODO: Parameters
city=$1
state=$2

echo $1 $2 $3

# Get the number of supplied args
echo $#

# running the above
# ./test.sh Alex Noble Grace

# TODO: read
echo What is your city:
read city
echo You belong to one of the best cities, $city

# arrays
# create
transport=('Bike', 'Car', 'Cycle')

# access the indices
echo "${transport[@]}"

# @ - all args
# [] - index

unset transport[2]

transport[2] = 'Plane'

# conditionals
[[]] or []
-eq -ne -gt -lt
if []
then
else
fi
