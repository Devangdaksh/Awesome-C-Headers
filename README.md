# Awesome-C-Headers
Emphasises both standard and non-standard C library headers.

# 📚 C Header Files Guide

A complete reference to **C header files** — both **standard** (ISO C) and **non-standard / library / user-defined** — including their origin, purpose, and when they were introduced.

---

## 📝 What Are Header Files?

In C, **header files** provide declarations of functions, macros, constants, and types.  
They’re included in source files with `#include <header.h>` or `#include "header.h"`.

There are three main kinds:

- **Standard headers**: Defined by the ISO C standard, guaranteed to exist on any conforming C implementation.
- **Non-standard headers**: Provided by an OS, compiler, or library. Not guaranteed to exist everywhere.
- **User-defined headers**: Created by you for your own projects.

---

## 🗂 Standard C Header Files Timeline

| Standard / Year | Headers Introduced | Committee | Notes |
|-----------------|-------------------|-----------|---------|
| **C89 / ANSI C (1989)** | `<assert.h>`, `<ctype.h>`, `<errno.h>`, `<float.h>`, `<limits.h>`, `<locale.h>`, `<math.h>`, `<setjmp.h>`, `<signal.h>`, `<stdarg.h>`, `<stddef.h>`, `<stdio.h>`, `<stdlib.h>`, `<string.h>`, `<time.h>` | ANSI X3J11 | The ANSI C (C89) header files were introduced as part of the formal standardization of the C programming language in 1989 by the ANSI X3J11 committee, shaping portability and the future of C development. Below is a detailed historical overview of their origin, committee process, timeline, and impact. |
| **C95 (Amendment 1)** | `<iso646.h>`, `<wchar.h>`, `<wctype.h>` | ISO/IEC WG14 | C95 (Amendment 1, 1995), developed by ISO/IEC WG14, enhanced the C standard by introducing <iso646.h> for alternative operators and <wchar.h>, <wctype.h> for improved multi-byte and wide character support, reflecting the committee's commitment to error correction and internationalization. |
| **C99 (1999)** | `<complex.h>`, `<fenv.h>`, `<inttypes.h>`, `<stdbool.h>`, `<stdint.h>`, `<tgmath.h>` | ISO/IEC WG14 | C99 (formalized as ISO/IEC 9899:1999) was developed by ISO/IEC WG14 to modernize C with features reflecting hardware and programming advances: it introduced headers for complex math, floating-point controls, precise integer types, boolean support, and type-generic math, marking a major expansion in expressiveness and reliability for C programmers. |
| **C11 (2011)** | `<stdalign.h>`, `<stdatomic.h>`, `<stdnoreturn.h>`, `<threads.h>`, `<uchar.h>` | ISO/IEC WG14 | C11 (ISO/IEC 9899:2011), created by ISO/IEC WG14, enhanced the C language by standardizing modern features such as thread support, atomic types, detailed alignment control, improved Unicode handling, and clear function exit attributes—all through headers with the goal of improving concurrency, portability, and safety for contemporary software development. |
| **C17 (2018)** | *(no new headers)* | ISO/IEC WG14 | C17, formally ISO/IEC 9899:2018, developed by ISO/IEC WG14 and published in 2018, is a revision of C11 that focused on fixing minor defects and clarifying ambiguities without introducing new language features or new standard headers; it primarily updated the macro __STDC_VERSION__ to 201710L and improved stability and reliability of the language.|
| **C23 (2024)** | `<stdbit.h>`, `<stdckdint.h>`, `<stdmem.h>`, `<stdfloat.h>` | ISO/IEC WG14 | C23, formally ISO/IEC 9899:2024, is the latest C standard developed by ISO/IEC WG14 and published in 2024, introducing new headers , among many other modern features such as bit-precise integer types, checked integer arithmetic, enhanced memory and floating-point utilities, improved Unicode support, new keywords, and extensive language and library enhancements aimed at improved safety, portability, and performance.|

These headers are implemented by compiler/runtime vendors (glibc, MSVC CRT, etc.) but specified by the standard.

---

## 🗂 Non-Standard & Common Library Headers

These headers are not part of the ISO C standard. They’re provided by operating systems, compilers, or third-party libraries:

| Header | Provider / Origin | Purpose |
|--------|-------------------|---------|
| `<conio.h>` | Borland/Turbo C, some Windows compilers | Console I/O like `clrscr()`, `getch()` |
| `<graphics.h>` | Borland/Turbo C graphics library | Functions like `initgraph()`, `circle()` |
| `<dos.h>` | MS-DOS compilers | Low-level DOS interrupts, time/date, etc. |
| `<malloc.h>` | Pre-ANSI C (now obsolete) | Memory allocation (use `<stdlib.h>` in standard C) |
| `<unistd.h>` | POSIX systems | System calls like `fork()`, `exec()`, `sleep()` |
| `<sys/socket.h>` | POSIX/BSD/Linux | Sockets API for network programming |
| `<pthread.h>` | POSIX | POSIX threads (pthreads) |
| `<windows.h>` | Microsoft Windows SDK | Windows API (GUI, file, registry, threads…) |
| `<gtk/gtk.h>` | GTK+ library | Cross-platform GUI development in C |
| `<curl/curl.h>` | libcurl library | Network requests (HTTP, FTP) |
| `<openssl/ssl.h>` | OpenSSL library | SSL/TLS cryptography |
| `<ncurses.h>` | ncurses library (Unix) | Advanced text UI in terminals |
| `<sqlite3.h>` | SQLite library | Embedded SQL database engine |

…and many more for specific libraries.

---
Here's a cross-platform availability summary for common C headers, using your suggested symbols and notes:

| Header       | Cross-Platform | Notes                             |
|--------------|----------------|----------------------------------|
| `<stdlib.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<stdio.h>`  | 🟢 Yes         | Standard C, available everywhere |
| `<string.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<stddef.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<stdint.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<stdbool.h>`| 🟢 Yes         | Standard C99, available everywhere |
| `<math.h>`   | 🟢 Yes         | Standard C, available everywhere |
| `<time.h>`   | 🟢 Yes         | Standard C, available everywhere |
| `<assert.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<errno.h>`  | 🟢 Yes         | Standard C, available everywhere |
| `<ctype.h>`  | 🟢 Yes         | Standard C, available everywhere |
| `<locale.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<float.h>`  | 🟢 Yes         | Standard C, available everywhere |
| `<setjmp.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<signal.h>` | 🟢 Yes         | Standard C, available everywhere |
| `<fenv.h>`   | 🟢 Yes         | Standard C99, mostly available   |
| `<uchar.h>`  | 🟢 Yes         | Standard C11, mostly available   |
| `<stdatomic.h>` | 🟢 Yes      | Standard C11, mostly available   |
| `<threads.h>` | 🟢 Yes        | Standard C11, mostly available   |
| `<tgmath.h>` | 🟢 Yes         | Standard C99, available everywhere |
| `<unistd.h>` | 🔴 No          | POSIX only (not available on Windows) |
| `<sys/socket.h>` | 🔴 No       | POSIX/BSD/Linux only                  |
| `<pthread.h>` | 🔴 No          | POSIX threads, POSIX only             |
| `<ncurses.h>` | 🔴 No          | UNIX-like terminal UI library only    |
| `<malloc.h>`  | 🟡 Limited    | Not standard, deprecated or OS-dependent |
| `<conio.h>`   | 🔴 No          | Windows/DOS-only (Borland, MSVC)      |
| `<windows.h>` | 🔴 No          | Windows SDK only                      |
| `<dos.h>`     | 🔴 No          | DOS/Windows compilers only             |
| `<graphics.h>`| 🔴 No          | Borland/Turbo C DOS graphics          |
| `<gtk/gtk.h>` | 🔴 No          | GTK+ GUI library, cross-platform but primarily Linux/Mac/Windows with GTK installed |
| `<curl/curl.h>`| 🟡 Limited    | Requires libcurl, platform-dependent but widely portable |
| `<openssl/ssl.h>`| 🟡 Limited   | Platform-dependent (but widely portable) |
| `<sqlite3.h>` | 🟢 Yes         | Cross-platform embedded DB library    |

This notation helps clarify portability considerations when choosing headers for C projects across platforms.
---
## Standard C Header Examples (How to Extend for All Headers)

Repeat this structure for every standard, non-standard, and library-specific header, keeping examples concise and focused on core functionality.

- **Usage snippets**: Show the most common or representative API usage.
- **Minimal test case**: Provide a short `main()` demonstrating successful compile/run.


#### `<assert.h>`
**Usage Snippet**
```c
#include <assert.h>
assert(2 + 2 == 4); // Check assertion at runtime
```
**Minimal Test Case**
```c
#include <assert.h>
int main() {
    assert(5 > 3); // Program continues if true; aborts if false
    return 0;
}
```


#### `<stdio.h>`
**Usage Snippet**
```c
#include <stdio.h>
printf("Hello, C!\n"); // Output text to stdout
```
**Minimal Test Case**
```c
#include <stdio.h>
int main() {
    printf("Test Passed\n");
    return 0;
}
```


#### `<stdint.h>`
**Usage Snippet**
```c
#include <stdint.h>
int32_t num = 42; // Signed 32-bit integer
```
**Minimal Test Case**
```c
#include <stdint.h>
#include <stdio.h>
int main() {
    uint8_t b = 255;
    printf("%u\n", b); // Should print: 255
    return 0;
}
```


#### `<math.h>`
**Usage Snippet**
```c
#include <math.h>
double r = sqrt(25.0); // r is 5.0
```
**Minimal Test Case**
```c
#include <math.h>
#include <stdio.h>
int main() {
    printf("%f\n", pow(2.0, 3.0)); // Should print: 8.000000
    return 0;
}
```
### `<stdlib.h>`
**Usage Snippet**
```c
#include <stdlib.h>
int *arr = malloc(sizeof(int) * 10); // Allocate array of 10 ints
free(arr);
```
**Minimal Test Case**
```c
#include <stdlib.h>
int main() {
    int *p = calloc(1, sizeof(int));
    free(p);
    return 0;
}
```
### `<string.h>`
**Usage Snippet**
```c
#include <string.h>
size_t len = strlen("Hello"); // Get length of string
```
**Minimal Test Case**
```c
#include <string.h>
#include <stdio.h>
int main() {
    char s[5] = "abc";
    strcpy(s, "def");
    printf("%s\n", s); // Should print: def
    return 0;
}
```
### `<ctype.h>`
**Usage Snippet**
```c
#include <ctype.h>
int res = isdigit('8'); // Returns nonzero for digit char
```
**Minimal Test Case**
```c
#include <ctype.h>
int main() {
    return isalpha('A') ? 0 : 1; // Returns 0 for alphabetic
}
```

### `<time.h>`
**Usage Snippet**
```c
#include <time.h>
time_t now = time(NULL); // Get current time
```
**Minimal Test Case**
```c
#include <time.h>
#include <stdio.h>
int main() {
    printf("%ld\n", time(NULL)); // Print current Unix timestamp
    return 0;
}
```
### `<limits.h>`
**Usage Snippet**
```c
#include <limits.h>
int max = INT_MAX; // Maximum value for int
```
**Minimal Test Case**
```c
#include <limits.h>
int main() {
    return (CHAR_BIT == 8) ? 0 : 1; // Typical for most platforms
}
```

### `<errno.h>`
**Usage Snippet**
```c
#include <errno.h>
errno = 0; // Set errno manually
```
**Minimal Test Case**
```c
#include <errno.h>
#include <stdio.h>
#include <math.h>
int main() {
    double r = sqrt(-1);
    if (errno != 0)
        printf("Error: %d\n", errno);
    return 0;
}
```


***

### Non-Standard Example: `<conio.h>` (Borland/Turbo C)
**Usage Snippet**
```c
#include <conio.h>
getch(); // Get a character from keyboard
```
**Minimal Test Case**
```c
#include <conio.h>
int main() {
    clrscr(); // Clear screen
    return 0;
}
```


***

### Non-Standard Example: `<unistd.h>` (POSIX)
**Usage Snippet**
```c
#include <unistd.h>
sleep(1); // Pause for 1 second
```
**Minimal Test Case**
```c
#include <unistd.h>
int main() {
    return (isatty(0) ? 0 : 1); // Check if stdin is a terminal
}
```

### `<locale.h>`
**Usage Snippet**
```c
#include <locale.h>
setlocale(LC_ALL, ""); // Use environment's locale settings
```
**Minimal Test Case**
```c
#include <locale.h>
#include <stdio.h>
int main() {
    setlocale(LC_ALL, "");
    printf("Locale set\n");
    return 0;
}
```
### `<float.h>`
**Usage Snippet**
```c
#include <float.h>
double d = DBL_MAX; // Largest double value
```
**Minimal Test Case**
```c
#include <float.h>
#include <stdio.h>
int main() {
    printf("%e\n", DBL_MIN); // Print smallest positive double
    return 0;
}
```
### `<setjmp.h>`
**Usage Snippet**
```c
#include <setjmp.h>
jmp_buf buf;
if (setjmp(buf)) { /* handle jump */ }
```
**Minimal Test Case**
```c
#include <setjmp.h>
#include <stdio.h>
jmp_buf buf;
void jump() { longjmp(buf, 42); }
int main() {
    if (setjmp(buf) == 0) {
        jump();
    } else {
        printf("Jumped!\n");
    }
    return 0;
}
```
### `<signal.h>`
**Usage Snippet**
```c
#include <signal.h>
signal(SIGINT, SIG_IGN); // Ignore Ctrl+C
```
**Minimal Test Case**
```c
#include <signal.h>
#include <stdio.h>
int main() {
    signal(SIGINT, SIG_IGN);
    printf("SIGINT ignored\n");
    return 0;
}
```

### `<sys/socket.h>` (POSIX)
**Usage Snippet**
```c
#include <sys/socket.h>
int sock = socket(AF_INET, SOCK_STREAM, 0);
```
**Minimal Test Case**
```c
#include <sys/socket.h>
int main() {
    int s = socket(AF_INET, SOCK_STREAM, 0);
    return (s < 0 ? 1 : 0);
}
```
### `<pthread.h>` (POSIX)
**Usage Snippet**
```c
#include <pthread.h>
pthread_t tid;
pthread_create(&tid, NULL, thread_fn, NULL);
```
**Minimal Test Case**
```c
#include <pthread.h>
void *thread_fn(void *arg) { return NULL; }
int main() {
    pthread_t tid;
    return pthread_create(&tid, NULL, thread_fn, NULL);
}
```

## 🗂 User-Defined Headers

You can create your own header files for your project:

`mymath.h`
```c
int add(int a, int b);
int sub(int a, int b);
````

Then include it:

```c
#include "mymath.h"
```

This is how you share declarations across multiple `.c` files.

---

## 🏛 Who Defines and Implements Headers?

* **ISO/IEC JTC1/SC22/WG14**: Defines the C language and standard headers.
* **ANSI X3J11 Committee**: Defined the first ANSI C standard (C89).
* **Compiler Vendors** (GCC, Clang/LLVM, Microsoft, Intel): Implement the standard headers for their runtime libraries.
* **Operating Systems** (Linux, BSD, Windows): Ship their own headers for system calls and APIs.
* **Library Authors**: Create custom headers for their libraries (GTK, OpenSSL, libcurl, SQLite…).
* **You**: Create user-defined headers for your own project.

---

## 📚 Sources & References

* [Wikipedia: C standard library](https://en.wikipedia.org/wiki/C_standard_library)
* [cppreference.com C headers](https://en.cppreference.com/w/c/header)
* [Wikipedia: ANSI C](https://en.wikipedia.org/wiki/ANSI_C)
* [ISO/IEC 9899: C standards](https://www.iso.org/standard/82073.html)
* [Dennis Ritchie on the development of C](https://www.nokia.com/bell-labs/about/dennis-m-ritchie/chist.html)

---

## 📂 About This Repository

This repository is a **reference guide to C header files**, including:

* ✅ Standard headers (ISO C)
* ✅ Non-standard headers (OS/compiler-specific)
* ✅ Third-party library headers
* ✅ How and when they were introduced
* ✅ Who maintains them

Contributions welcome! Feel free to open issues or pull requests for corrections or additions.

---

