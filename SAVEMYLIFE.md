## BASH

- Find last day modified files on current path and subdirectories: \
`find . -mtime -1 -print`

- Sort files by modified date on directory $1: \
`find $1 -type f | xargs stat --format '%Y :%y %n' | sort -nr | cut -d: -f2- | head`

- Change permissions to all files on path $1 to 644: \
`find $1 -type f -exec chmod 644 {} \;`

- Change permissions to all directories on path $1 to 644: \
`find $1 -type d -exec chmod 644 {} \;`

- Get user's prefered shell: \
`echo $SHELL`

- Analize file, grep by `error` string and get only string after `Instrument not found:` string, then sort, get unique strings and save to `ERRORS.log` file: \
`cat 2016-02-26T13%3A35%3A51%3A817.log | grep -ni "error" | sed 's/.*Instrument not found://' | sort | uniq > ERRORS.log`

## VIM

- Delete everything within double quotes: \
 `di"`

- Delete blank lines: \
`:g/^$/d` (`:g` will execute a command on lines which match a regex. The regex is 'blank line' and the command is `:d` (delete))

- Sort lines: \
`:sort`

- Sort removing duplicated lines: \
`:%sort u`


