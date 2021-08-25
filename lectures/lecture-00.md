# August 23rd 2021

For this course we will be using C/C++ to write the VM and Assembler.

If you really wish to not use C/C++ you can write things in another language and
use a IDL to translate it into C++. THIS IS NOT RECOMMENDED. It's honestly
probably better to just write it in C++. 

## Two Pass Assembler

An assembly language has its own version of variables which are called symbols
(not an exact comparison). If you are to only use a single pass Assembler you
must define a symbol before using it, otherwise the assembler will not know 
about the symbol. 

In a Two Pass Assembler you first go through the assembly language and make 
sure you know about all the symbols, then you go through and start translating
opcodes into raw assembly-bytes.

Resources: 
[Two Pass Assemblers: Advantages, Working, Design](https://www.entcengg.com/two-pass-assemblers/)

## Options for Testing

TL;DR - If you've never done it, *don't try it for this class* but learn it for
your job after you get an A in this class. If you really want to do it you'll
probably need to find your own testing method.

--------

Testing is awkward in C++. If you have not already worked with a testing
framework in another language, it is probably best to not do unit testing for
this class. It will take longer for you to complete the assignments and it will
add a significant amount more information and overhead that you will need to
worry about. Be aware though, this is not a sustainable approach for production
code that will have livelihoods depending on it functioning correctly. It is
irresponsible for developers who have people depending on them to not
effectively test their code.

Options:

Feel free to add to this list if you are interested.

- (DIY) Write lots of files with "main" in them and generate each one as a new executable and run each one of the executables as a test 
- CMake has an option to add tests to your code this is the second simplest option
- XCTest is xCode's frame work
- VS Code has a rather minimal extension
- Google Test is an option 
    - Its on the bleeding edge so it may not be compatible with older versions of C++
- CppUnit is a port of JUnit (a little out dated) 
