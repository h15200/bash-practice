# Bash notes

## Set up

* `#!/bin/bash` on all files
* No extension like .sh
* `chmod -x <filename>`     
* In commandline, edit with nano scriptname but maybe just better to open up vscode
* in the beginning of session add  `export PATH=$PATH:/Users/bla bla` to be able to call the script from anywhere 

## Commands

* `date`
* `head -n 3 filename`   first 3 three lines of script
* `tail filename` last 10 lines (default without -n) of script
* `echo $PATH | tr ":" "\n" | tail -n 3` print the PATH but replace : with a newline, and just the last 3 entries
