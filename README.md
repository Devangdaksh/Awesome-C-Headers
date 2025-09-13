# c-library-headers
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

