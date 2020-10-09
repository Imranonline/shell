**What is sed command in Linux?**
SED command in UNIX is stands for stream editor and it can perform lot’s of function on file like, searching, find and replace, insertion or deletion.

```
Syntax:

sed OPTIONS... [SCRIPT] [INPUTFILE...]

```

Example:

    1. $sed 's/imran/ansari/' abc.txt

    this will replace all the lines which will match imran with ansari in abc.txt

    2. $sed 's/imran/ansari/2' abc.txt (this will replace the 2nd occurance of imran with ansari in abc.txt)

    3. $sed 's/imran/ansari/g' abc.txt (this will replace all occurance of imran with ansari in abc.txt)

    4. $sed 's/imran/ansari/2g' abc.txt (this will replace from 2nd occrance of imran to all occurance of imran with ansari in abc.txt)

    5. $sed '4 s/imran/ansari/' abc.txt (it will replace imran to all occurance of imran with ansari in abc.txt on line number 4)

    6. sed '4d' abc.txt (it will delete 4th line in abc.txt)
