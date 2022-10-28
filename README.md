Creating our own version of 'printf'

This repository contains our own version of the function printf, originally included in the library stdio.h.

## Introduction
Emulates the operation of the printf function which delivers an output according to a format composed by zero or more directives and conversion specifiers:

Specifier | Input example | Output example
| --- | --- | --- |
%c | "Printing a char: [%c]\n", 'X' | Printing a char: [X]
%s | "Printing a string: [%s]\n", "Hello, World" | Printing a string: [Hello, World]
%d or %i | "Printing a number: [%i]\n", 386 | Printing a number: [386]
%% | "Printing a percent sign: [%%]\n", % | Printing a percent sign: [%]


## Files in this repository

|File| Description |
|--|--|
| **main.h** | the header file for all the prototypes and the structure we use. |
| **_printf.c** | the main program.||
| **man_3_printf**| man-page for the program _printf.|
| **_putchar.c** | here is the function to print one by one character.|
| **get_match_func.c** | This is the function that finds the match between the char ("c","s","d","i", "%") in struct st_format and the format string. and also if there is not match it will print the % and the next character that is different to the ones in the struct.|
## Compilation

```c
gcc -Wall -Werror -Wextra -pedantic *.c
````

## Examples to use it


    #include "holberton.h"
    /**
     * main - main function
     * Return: always 0
    **/
    int main()
    {
        _printf("Hello World!/n");
        return (0);
    }

    output: Hello World!
---

    #include "holberton.h"
    /**
     * main - main function
     * Return: always 0
    **/
    int main()
    {
            char string[7] = "World!"

        _printf("Hello %s/n", string);
        return (0);
    }

    output: Hello World!
---


    #include "holberton.h"
    /**
     * main - main function
     * Return: always 0
    **/
    int main()
    {
            int num = 1006

        _printf("This is a number: %d/n", num);
        return (0);
    }

    output: This is a number: 1006


