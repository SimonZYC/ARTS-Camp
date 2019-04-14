**Review**

# Using Square Brackets in Bash: Part 1

[Link](<https://www.linux.com/blog/2019/3/using-square-brackets-bash-part-1>)

This article talks about square brackets [] in bash.

## Globbing（通配）

The author first mentioned other characters that could be used for globbing.

### Asterisk * —— 0 or more characters

```bash
ls d*k*
```

### Question mark ? —— 1 character

```bash
ls d*k?
```

### Curly Braces {}

```bash
# create file000 to file099
touch file0{0..9}{0..9}
```

Then came the square brackets:

### Square Brackets []

To list *file022*, *file027*, *file028*, *file052*, *file057*, *file058*, *file092*, *file097*, and *file98* you can do this:

```bash
ls file0[259][278]
```

if we want to create duplicates of files *file010* through *file029* and call the copies *archive010*, *archive011*, *archive012*, etc..

The following are incorrect:

```bash
cp file0[12]? archive0[12]?
cp file0[12]? archive0[1..2][0..9]
```

Because globbing is for matching against existing files and directories and the *archive...* files don't exist yet.

Instead we could use

```bash
for i in file0[12]?; do

cp $i archive${i#file};

done
```

`#` can be used to lop off the beginning of a string contained in a variable.

