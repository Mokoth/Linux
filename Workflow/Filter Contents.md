## Less and More



- Fundamental __pagers__ that allows us to scroll through the file in an interactive view.



### More

`more /etc/passwd`

- after reading the content using __cat__ and directed it to __more__, the __pager__ opens, and will automatically start at the beginning of the file

[Q] - to leave pager

- N/B - output remains in the terminal



### Less

`less /etc/passwd`

- N/B - unlike more, less output does not remain in the terminal.



### Head

- By default, it prints the 1st 10 lines of the given file/input, if not specified otherwise.

`head /etc/passwd`

- N/B - if specified:

`head -n 3 /etc/passwd`



### Tail

- Returns the last parts of a file/results - 10, ofcourse (conterpart of head)

`tail /etc/passwd`

`tail -n 3 /etc/passwd`



### Sort

- Sort desired results alphabetically or numerically to get a better overview. 

`cat /etc/passwd | sort`  -> -r/-h/-n options



### Grep

- Useful when only searching for specific results that contain patterns we have defined.

`cat /etc/passwd | grep '/bin/bash'` -> search for users who have the default shell '/bin/bash' set

- N/B - to exclude specific results, use the option __-v__

`cat /etc/passwd | grep -v 'false\|nologin'` -> excluded false and nologin from the desired result.



### Cut

- Separate characters as delimiters - d: and define with the option -f the position in the line we want to output

`cat /etc/passwd | grep -v 'false\|nologin' | cut -d: -f1`



### Tr

- Replace certain characters from a line with characters defined by us.

- 1st option, define which character we want to replace.

- 2nd option, define the character we want to replace it with.

`cat /etc/passwd | grep 'false\|nologin' | tr ':' ' '`



### Column

- To help display results in a well suited tabular form using the '-t'

`cat /etc/passwd | grep -v 'false\|nologin' | tr ':' ' ' | column -t`



### Awk

- In an instance where we do have one row too many, example for a user, using awk will help sort such result and display the 1st ($1) and last ($NF) result of the line

`cat /etc/passwd | grep -v 'false\|nologin' | tr ":" " "  | awk '{print $1, $NF}'`



### Sed

- Helpful when we want to change specific names in the whole file/standard input. -> substituting text

- sed looks for patterns we have defined in the form of regular expressions and replaces them with another pattern that we have also defined.

`cat /etc/passwd | greop -v 'false\|nologin' | tr ":" " " | awk '{print $1, $NF}' | sed 's/bin/HTB/g'` -> 'g' flag - replace all (global)



### Wc

- To count lines. With -l option, we specify that only the lines are counted

`cat /etc/passwd | grep -v 'false\|nologin' | tr ":" " " | awk '{print $1, $NF}' | wc -l`


