So uh, I kinda made a libfttester. It is quite complete, with its own limitations. It will test all the madatory functions of the libft.
To use it, put the tester .c file in your libft folder, run make, and "gcc [tester].c libft.a && ./a.out" (or "gcc *.c && ./a.out" if your makefile is not ready).

Some perks of using this one :
- When an unexpected result is encountered, the program will show directly what the expected result was compareed to the obtained one. This might not always work properly with e.g. empty strings.
- Playing with the tests is easy, you just need to be in the right section of the program (ctrl+f will come in handy).
- Some tests are very thorough (like on atoi).

Limitations :
- Idk how to use file descriptors nor how to check the size of a malloc.
- If a test provokes a bus error or a segfault, you will have to search for it by yourself by fiddling with the tester.
- The tester will often segfault when your function sends back NULL instead of something else, since it will try to use said NULL in strcmp.
- If you don't have all your functions ready, you will have to silence the associated tests in the tester so that it doesn't crash.
