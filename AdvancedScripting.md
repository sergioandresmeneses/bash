# Advanced Scripting

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

---
### Best Practices
 * Proper documentation.
 * Include all the options in your commands ` --help | -h ) `
 * Setting the env variables you need.
  * Setting UID Shell Script: A Bad Idea!!!