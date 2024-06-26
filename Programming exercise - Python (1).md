1 Week to complete
# Linux mini-utils
The goal of this exercise is to test your understanding of both python
and Linux systems by re-implementing (minimal versions of) common
utilities.

Here are 3 little programs/functions that you should provide:
## "mini-grep"

Usage:

    ./mini-grep [-q] -e PATTERN [FILE...]

`mini-grep` goes through every argument in FILE and prints the whole 
line in which PATTERN is found. By default `mini-grep` also outputs
the line number of each printed line.
- PATTERN has to be a valid regex
- FILE can be zero or more arguments. If zero args are given, 
  `mini-grep` will parse entries from the standard input.
- If given, the `-q` options only outputs lines but omits the matching
  line numbers.
## "mini-ls"

Usage:  

    ./mini-ls [-r] [FILE...]

`mini-ls` lists information about the paths given in FILE. The
information required are: Owner, Permission, Modified Time.
- FILE can be zero or more arguments. If zero args are given, 
  `mini-ls` will list information about the current directory.
- If given, the `-r` option will make `mini-ls` run recursively on any
  directory it comes across.
## "mini-df"

Usage:

    ./mini-df [-h] [PATH...]

`mini-df` outputs the file system disk space usage of each entry in
PATH. The information required is: Total Space, Free Space, Used
Space. The result should be in Bytes.
- PATH can be zero or more arguments. IF zero args are given,
  `mini-df` will list the disk space usage of the current directory.
- If given `-h` will output the result in human-readable format.
## General Requirements

* You only need to implement *one* of the 3 utilities. We won’t have time to discuss more than one.
* These scripts should all be written in a modern version of Python3
* These scripts should be executable from command line
* You're expected to provide tests for each of these
* You're expected to provide at least some basic level of error handling. 
  E.g. the script shouldn't crash when running with wrong or unexpected arguments.
* Python code has to be PEP8 compliant
* Commit these scripts in a publicly available git repository I can pull from
* You are not allowed to use 3rd party libs, but all the modules of the standard library can be used.
* All the scripts have to print out short instructions about how to use them when started with the '--help' parameter.