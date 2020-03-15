# Basic Overview

---
### Background

---
### Basic Syntax

 * if-elif-else-fi
 ```
 if grep pattern myfile > /dev/nul
 then
    ...
 else
    ...
 fi
 ```

 * Test command
 ```
    if test "$str1" = "$str2"
    then
        ...
    fi
 ```

 ```
    if [ "$str1" = "$str2" ]
    then
        ...
    fi
 ```

 * The CASE Statement

 ```
 case $1 in
 -f)
    ...
    ;;
 -d | ..directory)
    ...
    ;;
 *)
    echo $1: unknown option >&2
    exit 1
 esac
 ```

 * LOOPS
    * For

    ```
    for i in <place>
    do
        ... [break|continue]
    done
    ```
    * While and Until
    ```
    [while|until] _condition_
    do
        ...
    done
    ```

 * Exit Status: There is a number code for each status, the most common are: ` 0 for success and 1 for failure `

 > command:
 > exit [ value ] "You can define the status for the executtion of the script/program"

---
### Functions

` function_name () {...} `

return [ _exit-value_ ]

---
### Variabless

* Export: Handles the env variables

```
$export -p

$PATH=$PATH:/usr/bin
$export PATH
``` 
 * Unset: Removes the variables from the current shell

```
$ unset var
```

 * Special Variables

Variable | Value
--- | --- 
$@ | all script parameters
$1 ... $n | script parameters
$? | status of the previous command
$0 | name of the shell program
HOME | home directory
IFS | Internal Field Separator
PWD | current directory
PPID | process ID of parent process

* Arithmetic Expansion

Operator | Meaning
--- | --- 
++-- | increment and decrement
+ - | addition and subtraction
== != | equal and not equal
< <= => > | Comparisons
&& | Logical AND
|| | Logical OR


---
### RE -regular expressions

Special Characters:
` \ . * ^ $ [...] + ?   `

```
 $ sed 's/:.*//' /etc/passwd | sort -u
```

> Commands:
> grep, egrep, find, sed, awk