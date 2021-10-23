# UcuLib
A Microcontroller-centric Arithmetic, Cryptography, and Utility Library

(This project is just getting started, so nothing is usable yet.)

*UcuLib*:
- Is a traditional library, in that it is a library composed of one function
  or data structure per object module.  (In the traditional usage, the
  linker extracts only the minimum set of object modules it needs to
  resolve references, which gives the library a minimal footprint in
  the executable image.  This is important for embedded work, where memory
  of all types is at a premium.)
- Contains functions for:
  - Utility and miscellaneous operations (such as determining the
    version number of the library or the size of certain data types).
  - Block memory operations (setting, copying, shifting, etc.).
  - Searches (linear search, binary search, etc.)
  - Sorting.
  - Array manipulation.
  - Bit-mapped sets.
  - Vertical counters.
  - Integer arithmetic and utility functions that operate on basic
    (built into the compiler) character and integer types.
  - Integer mathematical functions that operate on basic
    (built into the compiler) character and integer types.
  - Fixed-point utility and arithmetic functions that operate on basic
    (built into the compiler) character and integer types.
  - Fixed-point mathematical functions that operate on basic
    (built into the compiler) character and integer types.
  - Floating-point arithmetic and utility functions that operate on
    basic (built into the compiler) data types.
  - Floating-point mathematical functions that operate on
    basic (built into the compiler) data types.
  - Integer arithmetic and utility functions that operate on large
    (sizes not necessarily supported by the compiler) integers.
  - Integer mathematical functions that operate on large
    (sizes not necessarily supported by the compiler) integers.
  - Fixed-point utility and arithmetic functions that operate on fixed-point
    values represented as large (sizes not necessarily supported by the
    compiler) integers.
  - Fixed-point mathematical functions that operate on fixed-point
    values represented as large (sizes not necessarily supported by the
    compiler) integers.
  - Floating-point arithmetic and utility functions that operate on
    large (sizes not necessarily supported by the compiler) data types.
  - Floating-point mathematical functions that operate on
    large (sizes not necessarily supported by the compiler) data types.
  - Linear filter and control system component functions.
  - Non-linear filter and control system component functions.
  - Pseudo-random number generation functions.
  - Non-cryptographic hash functions.
  - Cryptographic hash functions.
  - Symmetric cipher functions.
  - Asymmetric cipher functions.
- Supports C and C calling conventions.  (In practice, this means that the
  library can be used from both C and C++, as C++ compilers typically
  support C libraries and C code.)
- Contains core functions written in assembly-language, with a C fallback.
  (Large integer and cryptographic functions tend not to be very efficient
  when implemented in a high-level language.)
- Supports multi-core systems and systems with complex memory architectures (coherent
  and non-coherent caches).
- Can be used:
  - As a conventional binary library without source code.
  - As a conventional binary library with source code (some debuggers can use
    source code accompanying a library).
  - As a conventional library with source code that has been customized/modified
    by the end user.
  - By harvesting the library source code to create non-library software modules(s).
    - The library is designed so that the desired functions and data structures
      can be copied into source files and incorporated in a software project.
      (Usually, at least two source files are required:  a C source file
      containing the C functions and data structures and an assembly-language
      source file containing the assembly-language functions and data
      structures.)
    - This approach may be helpful when working with debuggers that don't
      support libraries well.
- Is provided under an extremely permissive license.
  - The license text is:<br><br>
    *Copyright 2021 David T. Ashley and Other Contributors<br><br>
    Permission is hereby granted, free of charge, to any person obtaining a copy of
    this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights to
    use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
    of the Software, and to permit persons to whom the Software is furnished
    to do so, subject to the following conditions:<br><br>
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software source code.  (This license does
    NOT require that this copyright and permission notice be included in source
    code derivatives that are not pure source code.  Source code derivatives
    that are NOT required to include this copyright and permission notice
    include but are not limited to
    assembly-language generated by compiling the source code and possibly
    containing the source code as compiler-generated comments, libraries, object code,
    machine code,
    executable images, or images derived from or substantially equivalent in
    function to executable images that are intended to execute on a computer
    processor.)<br><br>
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
    FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
    DEALINGS IN THE SOFTWARE.*

The source code of the library is maintained as a set of source code templates that are interpreted
to generate the customized source code for each target environment.  (This eliminates
code customized via C preprocessor conditionals.  Such conditionals often confuse
debuggers and also make the soure code difficult for a human to understand.)

The documentation for the library is contained in .PDF manual packaged with the library.  To avoid
redundancy of information, the interfaces of the functions and data structures of the library
are not documented in the source code (that information is in the *.PDF* manual).  The function
internals, however, are documented in the source code.

