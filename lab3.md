# Lab Report 3

## Researching commands: *find* and some of its options

*find* is a Linux command used for searching through file hierarchies and finding files and directories. 
This makes it a useful command, especially if you have a large number of files and nested directories and you want to find a particular file or directory with as few commands as possible.
In this lab report, I look up some of the most interesting options for *find*.

### 1. __-size__ option

This option allows us to filter the search output for files based on their size. We can use this look for files that are larger or smaller than a particular size or within a certain size range. 

We would run the following command to find all files that are between 10 bytes and 100 kilobytes in size inside of ```technical/biomed/```: <br /><br />
```find technical/biomed/ -size +10b -size -100k```



