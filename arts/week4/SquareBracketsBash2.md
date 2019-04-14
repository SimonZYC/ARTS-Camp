# Using Square Brackets in Bash: Part 2

This article talked about square brackets [] as commands.

Square brackets act as testing commands. For example,

```bash
[ 'a' = 'a' ]
echo $?
# output: 0
```

Notice that there are **spaces** between the opening bracket `[` and the parameters `"a" = "a"`, and then between the parameters and the closing bracket `]`.



```bash
[ STRING1 = STRING2 ] # checks to see if the strings are equal
[ STRING1 != STRING2 ] # checks to see if the strings are not equal 
[ INTEGER1 -eq INTEGER2 ] # checks to see if INTEGER1 is equal to INTEGER2 
[ INTEGER1 -ge INTEGER2 ] # checks to see if INTEGER1 is greater than or equal to INTEGER2
[ INTEGER1 -gt INTEGER2 ] # checks to see if INTEGER1 is greater than INTEGER2
[ INTEGER1 -le INTEGER2 ] # checks to see if INTEGER1 is less than or equal to INTEGER2
[ INTEGER1 -lt INTEGER2 ] # checks to see if INTEGER1 is less than INTEGER2
[ INTEGER1 -ne INTEGER2 ] # checks to see if INTEGER1 is not equal to INTEGER2
etc...
```

More examples:

```bash
for i in {000..099};\
do\
 if [ ! -f file$i ];\
 then\
  touch file$i;\
  echo I made file$i;\
 fi;\
done
```

