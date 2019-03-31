# fatal error: 'malloc.h' file not found

When we compile C project for Linux on MacOS, sometimes we may encounter the error `fatal error: 'malloc.h' file not found`.

## Solution

Change error file:

```c
#include <malloc.h>
```

to

```c
#include <sys/malloc.h>
```



If you need to write C programs that are cross-platform, you can refer to

[C/C++ cross platform](https://blog.csdn.net/itas109/article/details/81193432)

Or you can define Macro in Makefile.



## Reference:

[fatal error: 'malloc.h' file not found](https://www.cnblogs.com/chaolee/archive/2013/01/05/2846936.html)