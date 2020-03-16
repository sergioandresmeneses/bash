# Advanced Scripting

---
### Special files; /dev/null /dev/tty

```
    if grep pattern file > /dev/null
    then
        ...
```

```
    read pass < /dev/tty
```

---
### Diff & Patch

` $ diff file1 file2 `
```
1c1
< file1
---
> file2
```

*Patch* is used to reconstruct other file using diff as source
` $ patch file.dif `

---
### Execution Tracing

When you script doesn't work as expected!

```
    $ sh -x myscrypt.sh
```

```
    set -x          #Enabling Tracing  
    echo $(pwd)     #Command to be tracked

    set +x          #Turnning Off Tracing
    $(ls -lah)
```

---
### Cron
It allows you to executte scripts at specifed time.

` $ crontab -l` teh crontab files are stored at ` /var/spool/cron/crontabs/ `

You can also use the `/etc/cron.[time]/` subdirectories to scheduled it

_The following crontab removes any log files from the user's home directory at 1:00 a.m. every Sunday morning._
```
    # crontab -e jones 
    1 0 * * 0 rm /home/sergio.meneses/*.log > /dev/null 2>&1    #This command helps clean up user accounts.
```
 > Further details about the time fields at https://docs.oracle.com/cd/E19253-01/817-0403/sysrescron-62861/index.html
---
### Best Practices
 * Proper documentation.
 * Include all the options in your commands ` --help | -h ) `
 * Setting the env variables you need.
 * Setting UID Shell Script: A Bad Idea!!!