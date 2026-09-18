# Lab 03 - C Programming Language Basics 

## 1. Data Types
The table below highlights the standard fundamental data types used in C programming along with their typical structural usage descriptions:

| Data Type | Description |
| :--- | :--- |
| `int` | Stores whole numbers (integers) without decimals (e.g., 5, -100). |
| `float` | Stores single-precision fractional numbers/floating-point values (up to 6–7 decimal digits). |
| `double` | Stores double-precision fractional numbers/floating-point values (up to 15 decimal digits). |
| `char` | Stores a single character, letter, or ASCII value enclosed in single quotes (e.g., 'A'). |
| `bool` | Stores a boolean value representing either `true` (1) or `false` (0). *(Requires `<stdbool.h>`)* |
| `void` | Represents the absence of a value or type; commonly used as a function return type when no value is returned. |

---

## 2. Format Specifiers
Format specifiers are used during input and output operations to tell the compiler what type of data it is processing:

| Format Specifier | Data Type / Representation |
| :--- | :--- |
| `%d` | Signed decimal integer |
| `%u` | Unsigned decimal integer |
| `%o` | Unsigned octal integer |
| `%x` | Unsigned hexadecimal integer (lowercase letters) |
| `%X` | Unsigned hexadecimal integer (uppercase letters) |
| `%f` | Decimal floating-point number |
| `%e` | Scientific notation (exponential notation with lowercase 'e') |
| `%c` | Single character |
| `%s` | String of characters (text array) |
| `%ld` | Signed long decimal integer |

---

## 3. Input/Output Functions
C provides several built-in standard library functions under `<stdio.h>` to handle reading from and writing to terminal consoles:

* **`scanf()`**: A formatted input function that reads standard user input from the console and stores it into specified variables using format specifiers and address pointers (`&`).
* **`printf()`**: A formatted output function used to print variables, strings, numbers, or expressions directly to the screen.
* **`getchar()`**: A dedicated input function that reads exactly one single character from the console buffer and returns its integer ASCII value.
* **`putchar()`**: A dedicated output function that writes a single character argument straight onto the user console screen.
* **`fgets()`**: A safe string input function that reads a full line of text or up to a maximum buffer limit from a stream, effectively preventing buffer overflow vulnerabilities.
* **`puts()`**: A streamlined string output function that outputs a string array onto the screen and automatically appends a newline character (`\n`) at the end.

---

## 4. Escape Sequences
Escape sequences are sequences of characters used to format the structure of output strings. They begin with a backslash (`\`) followed by a command character:

* **`\n` (Newline)**: Moves the cursor to the beginning of the next line.
* **`\t` (Horizontal Tab)**: Inserts a uniform horizontal tab spacing.
* **`\\` (Backslash)**: Prints a literal backslash character onto the terminal.
* **`\"` (Double Quote)**: Inserts a literal double quote inside an already quoted string block.
* **`\b` (Backspace)**: Moves the terminal cursor back by one position to erase or overwrite text.

---

## 5. Precision Control in Floating-Point Output
In C, the precision of a floating-point value during output is specified within a `printf()` format specifier by adding a dot (`.`) followed by an integer argument right before the `f` or `e` specifier character. 

By default, `%f` prints up to 6 decimal places. Using the structure `%.Nf` allows you to override this to exactly `N` places. 

```c
float value = 5.123456;
printf("%.2f", value); // Outputs exactly two decimal points: 5.12
printf("%.4f", value); // Outputs exactly four decimal points: 5.1235 (rounded up)
```
