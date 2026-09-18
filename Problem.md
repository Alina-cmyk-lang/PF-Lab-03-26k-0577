# Lab 03 - Pseudocode Solutions

## Problem 1: Display student information using different data types
```text
START
    DECLARE string student_name = "Your Name" 
    DECLARE integer roll_number = 12345
    DECLARE character section = 'A'
    DECLARE float gpa = 3.75

    PRINT "Student Name: ", student_name
    PRINT "Roll Number: ", roll_number
    PRINT "Section: ", section
    PRINT "Current GPA: ", gpa
END
```

## Problem 2: Read and display a character using getchar() and putchar()
```text
START
    DECLARE character input_char
    PRINT "Enter a single character: "
    READ input_char USING getchar()
    
    PRINT "The character you entered is: "
    WRITE input_char USING putchar()
END
```

## Problem 3: Display a floating-point value using different precision settings
```text
START
    DECLARE float pi_value = 3.14159265
    PRINT "Default precision: ", pi_value
    PRINT "Precision to 2 decimal places: ", FORMAT pi_value TO 2 DECIMAL PLACES
    PRINT "Precision to 4 decimal places: ", FORMAT pi_value TO 4 DECIMAL PLACES
END
```
