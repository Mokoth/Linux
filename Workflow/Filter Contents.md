## less and more

- fundamental __pagers__ that allows us to scroll through the file in an interactive view.

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


