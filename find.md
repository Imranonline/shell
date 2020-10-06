**What is find command ?**

The find command is used to locate/search file on unix/linux system mostly used in shell scripting.
find will search any set of directories you specify for files that match the given search criterua. You can search for files by name,owner,group,type,permissions,date, and other criteria. The search is recursive i that it will search all subdirectories too.

find syntax:

```
find <path> <search criteria> <action>
```

eg :

    1. find (it will display the path of all files in the directory and subdirectory)

    2. find -type f (this will only search files)

    3. find -type d (this will only search directory)

    4. find . -type f -name abc.txt (this will look for all the files name as abc.txt in the same directory and its case sensitive)

    5. find . -type f -iname abc.txt (this will look for all the files name as abc.txt in the same directory and its case insensitive)

    6. find . -type f -iname "*.txt" (this is a wildcard search which will give me list of files)

    7. find . -type f -perm 0777 (this will find all files with permission 0777)

    8. find . -type f -perm 0777 -exec chmod 755 {} \; (this command will look for all the files with permission 0777 and execute and change the perission to 755)

    9. find . -mtime +1 (will find all the files which got modified in one day. time corresponds to 24 hrs =1)

    10. find . -mmin +1 (will find all the files which got modified in last 1 min)

    11. find / -size -1M (will find all the files with size less than 1MB)

    12. find / -size +10M -size -20M (this will look for all the files which has a size range of 10 to 20 MB)

    13. find / -maxdepth 3 -name "*log" (this will look for wildcard search log but will only go 3 level down in folders)
