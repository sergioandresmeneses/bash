# System Management
---
### Texts
 * Cat: showing file's data. `cat /etc/passwd`
 * Cut: Cutting out data from a text `cut -d : -f 1,5 /etc/passwd`
 * Join: Merging files ` join file1 file2 `
 * Awk: Rearranging fields ` awk -F: '{ print $1, $5 }' /etc/passwd `
 * Sort: Sorting text from an output
 * uniq: 
 * wc:
 * Head & Tail: Extract the first and last lines ` [head | tail] -n <value> -f /etc/passwd `
 * Pipelines `|`

---
### Documents
 * Read: reading documents
 ```
    while read line; do echo $line; done < file
 ```
  > Read can be used for reading data from the user: ` $ echo "What is your name?"; read name; echo "Welcome $name" `
 * Finding files: ` locate - find `
 * FileSystem: ` DF - DU `
 * Permissions: ` chmod `
 * Ownership: ` chown `

---
### Processes

Listing all the processes in your systems ` $ ps aux `

Killing processes ` $ kill -9 <PID> `

Delay a process ` $ sleep <TimeInSeconds> `

The */proc* FileSystem, each process has its own directory in here. ` $ cat -v /proc/16521/cmdline ` or ` head -n 5 /proc/meminfo `
