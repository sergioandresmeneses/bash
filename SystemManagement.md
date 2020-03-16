# System Management
---
### Text
 * Cat: showing file's data. `cat /etc/passwd`
 * Cut: Cutting out data from a text `cut -d : -f 1,5 /etc/passwd`
 * Join: Merging files ` join file1 file2 `
 * Awk: Rearranging fields ` awk -F: '{ print $1, $5 }' /etc/passwd `
 * Sort: 
 * uniq:
 * wc:

---
### Documents
 * Pipelines `|`
 * Read: reading documents
 ```
    while read line; do echo $line; done < file
 ```
 * Finding files: ` locate - find -  `
 * FileSystem: ` DF - DU `


---
### Processes

Listing all the processes in your systems ` $ ps aux `

Killing processes ` $ kill -9 <PID> `

Delay a process ` $ sleep <TimeInSeconds> `

The */proc* FileSystem, each process has its own directory in here. ` $ cat -v /proc/16521/cmdline ` or ` head -n 5 /proc/meminfo `
