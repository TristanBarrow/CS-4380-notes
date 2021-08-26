# August 25th 2021

## Project 0 Discussion

### Part 1

The idea behind point 1 is that we have a chunk of memory and we can interpret it how ever we want based on how we cast it.

If we have an array of integers with length 1 and we cast it to a char array we
end up with an array of length 4. We need to be careful not to try and access
information that is outside the definition of the array because we will be
overwriting data that may be important.

In this project we will be simulating the hardware of a computer with a series
of arrays or variables. We will need ways to simulate: 

- Registers
- RAM
- Disk memory
- IO

### Part 2

Our program will be an assembler and Virtual Machine combine. The assembler
portion of the program will need to read in assembly. When we run our program it
will end up looking something like this on the command line:

```
$ my-awesome-vm-assembler route/to/assembly/file 
```

Writing the logic to read files and do a little bit of lexing/parsing will be a
very useful thing to do now so you don't need to do it later in project 1.

### Part 3

In the our assembly language we will eventually need to get input from the user
so we can interact with our vm via command line. We will have an assembly
language instruction that tells our program to sit and wait for input from the
user. It would be very good to get the basic logic for interacting with the user
out of the way now.

### Part 4

Do a little bit of lexing so we don't have to do it later when we are focusing 
on more important things.

### Part 5

Make sure your program works using G++ or GCC instead of just using the default
compiler from a large IDE (Visual Studio). I'd recommend using VS Code, Atom,
NotePad++ or some other minimal editor so you can be sure it compiles without
weird dependencies. 

Also, if you run out of dummy assembly code make sure to end the program. You don't want your 
VM to hang because you will lose points for that.

## History Lecture

### Mechanical Computing

In class we also discussed a little bit about the history of computing. For a very long time we have always done math and calculations using mechanical devices, some of which are incredibly impressive in design but pail in comparison to how we do things with modern computers.

### Moore's Law and the Progression of Computing

This is an over simplified history.

In the early days of computing the main method of making a computer faster was
to just run the computers internal clock faster. eventually we got to the point
where if we tried to make the computers clock go faster we would be pumping so
much electricity through the circuits that they would melt. This boundary to 
speed was called the "Power Wall".

The next way to make computers faster was to decrease the size of the chip. This
was perfectly fine until we ran into physical limitations like atomic
restrictions. We physically cannot make transistors any smaller. 

The next way we can effect the speed of the chip is to use multi-core processing
which is currently being used as the primary method to reduce compute times. One
thing to think about is, while multi-threading is quite amazing, scheduling and
loading/unloading processors with parameters is quite expensive. Sometimes the
cost of using multi-threading out weighs the benefit especially if threads are
being spun up and torn down quite often. It may be worth it to consider a simpler
single threaded option over a more complicated multi-threaded option especially 
if you are looking for performance improvements.

Resources: 

[The End of Moore's Law](https://medium.com/@sgblank/the-end-of-more-the-death-of-moores-law-5ddcfd8439dd)