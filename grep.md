**What is grep in Linux?**
If you want to search a particular information the postal code from a text file you can use grep command on command line.

```
Syntax - grep search_string
grep [options] pattern [files]
```

What is a Pipe in Linux?
The Pipe is a command in Linux that lets you use two or more commands such that output of one command serves as input to the next. The symbol is '|'

Example:

    1. cat filename | grep a
    this will output all the lines which will match the grep criteria "a"

    2. cat filename | grep -v a (this will search everything which will not match grep criteria "a")

**Options Description**

    -c : This prints only a count of the lines that match a pattern
    -h : Display the matched lines, but do not display the filenames.
    -i : Ignores, case for matching
    -l : Displays list of a filenames only.
    -n : Display the matched lines and their line numbers.
    -v : This prints out all the lines that do not matches the pattern
    -e exp : Specifies expression with this option. Can use multiple times.
    -f file : Takes patterns from file, one per line.
    -E : Treats pattern as an extended regular expression (ERE)
    -w : Match whole word
    -o : Print only the matched parts of a matching line,
    with each such part on a separate output line.
