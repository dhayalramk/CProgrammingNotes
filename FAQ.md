# Group FAQ

1. What books or other resources should I use to learn C?
  
   You can find a list of resources [here](https://github.com/aleksandar-todorovic/awesome-c#learning-reference-and-tutorials)
 
2. What compiler is best?

   You can find a list of Free and Open Source Compilers [here](https://www.facebook.com/notes/c-programming/a-beginners-guide-to-using-freeopen-source-software-development-tools-and-enviro/676277512460549/) or [here](https://github.com/aleksandar-todorovic/awesome-c#compilers)
  
3. How do I use random numbers in C?
  
   You need to 
    
   1. Initialize the seed. 
    The seed is a number that multiplies with a couple random numbers (internally). You should use time(NULL) as the input parameter of the srand function (seed random). 
   2. Initialize the random variable with the rand() function. 
     If you need a range (numbers 0-20 or whatever) use the modulus ('%') 
     operator to generate your number. Example:
  
```c
#include <time.h>
#include <stdlib.h>

srand(time(NULL));   // should only be called once
int foo = rand();      // returns a pseudo-random integer between 0 and RAND_MAX
int bar = rand() % 55; //returns a pseudo-random integer between 0 and 54
int baz = (rand() % 55) + 1; // returns a psuedo-random integer between 1 and 55
```


4. Why should I not use Turbo-C/Turbo-C++
   
   You should never use this IDE because it is outdated. It uses header files that are deprecated , 
and havent been used since the mid-90's. These headers include:
   
   1. dos.h
   2. conio.h
   3. graphics.h
   4. iostream.h (for C++)
   
   Those header files are never used in modern C runtime libraries. As a matter of fact, 
C++ requires you to use iostream (without the .h), the iostream.h will never compile 
correctly (on modern compilers). This makes code highly unportable (as a matter of fact, 
it sets up an emulated dos enviornment for you to actually run your programs). This 
makes the user spend twice the time learning things, when they could have learned it 
correctly the first time.


## Another-C-FAQ

   [C-FAQ](http://c-faq.com/questions.html)
