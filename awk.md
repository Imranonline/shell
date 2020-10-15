**What is awk command in Linux?**
Awk is mostly used for pattern scanning and processing. It searches one or more files to see if they contain lines that matches with the specified patterns and then performs the associated actions.
Awk is abbreviated from the names of the developers – Aho, Weinberger, and Kernighan.

```

1. AWK Operations:
(a) Scans a file line by line
(b) Splits each input line into fields
(c) Compares input line/fields to pattern
(d) Performs action(s) on matched lines

2. Useful For:
(a) Transform data files
(b) Produce formatted reports

3. Programming Constructs:
(a) Format output lines
(b) Arithmetic and string operations
(c) Conditionals and loops


Syntax:

awk options 'selection _criteria {action }' input-file > output-file

```

Example:

    1. $ awk '{print}' abc.txt (By default Awk prints every line of data from the specified file abc.txt)

    2. $ awk '/imran/ {print}' abc.txt (the awk command prints all the line which matches with the ‘imran’.)

    3. awk '{print $1,$4}' abc.txt (For each record i.e line, the awk command splits the record delimited by whitespace character by default and stores it in the $n variables. If the line has 4 words, it will be stored in $1, $2, $3 and $4 respectively. Also, $0 represents the whole line.)

**Built In Variables In Awk**

Awk’s built-in variables include the field variables—$1, $2, $3, and so on ($0 is the entire line) — that break a line of text into individual words or pieces called fields.

**NR**: NR command keeps a current count of the number of input records. Remember that records are usually lines. Awk command performs the pattern/action statements once for each record in a file.

**NF**: NF command keeps a count of the number of fields within the current input record.

**FS**: FS command contains the field separator character which is used to divide fields on the input line. The default is “white space”, meaning space and tab characters. FS can be reassigned to another character (typically in BEGIN) to change the field separator.

**RS**: RS command stores the current record separator character. Since, by default, an input line is the input record, the default record separator character is a newline.

**OFS**: OFS command stores the output field separator, which separates the fields when Awk prints them. The default is a blank space. Whenever print has several parameters separated with commas, it will print the value of OFS in between each parameter.

**ORS**: ORS command stores the output record separator, which separates the output lines when Awk prints them. The default is a newline character. print automatically outputs the contents of ORS at the end of whatever it is given to print.

```
4. $ awk '{print NR,$0}' abc.txt (This will add the line number / Display line number as first column \$0)

5. $ awk '{print $1,\$NF}' abc.txt (This will print column 1 and last field value)

```
