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

## Syntax - Common mistakes

* White space and return carriages matter a lot!!


This will run
```
if (a -gt b)
then echo 'yes'
fi
```

This will NOT run
```
if (a -gt b) then echo 'yes'
fi
```

If you want it on the same line, add a semicolon to signify return carriage


## In conditionals, there are types of brackets for different use cases! To test regex, you must use double square brackets and there MUST be a white space after the inner most square brackets. Regex comparison is ~= and there must be whitespace

```
if [[ $thing =~ [0-9]{3} ]]
then SOMETHING
fi
```

## Read line loops syntax

```
while read line 
do
  echo $line
done > fileName.txt
```