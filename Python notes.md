            PYTHON

# Week 1

#  Programming concepts: 

* Functions: A function is a piece of code that performs a unit of work. In the examples you've seen so far, you have only encountered the print() function, which outputs a message to the screen. 


* Keywords: A keyword is a reserved word in a programming language that performs a specific purpose.These are some of the keywords,

        Values: True, False, None
        Conditions: if, elif, else
        Logical operators: and, or, not
        Loops: for, in, while, break, continue
        Functions: print, def, return

* Arithmetic operators: Python can calculate numbers using common mathematical operators, along with some special operators, too: 


        x + y            Addition + operator returns the sum of x plus y
        x - y             Subtraction - operator returns the difference of x minus y
        x * y            Multiplication * operator returns the product of x times y
        x / y             Division / operator returns the quotient of x divided by y
        x**e            Exponent ** operator returns the result of raising x to the power of e 
        x**2            Square expression returns x squared
        x**3            Cube expression returns x cubed
        x**(1/2)    Square root (½) or (0.5) fractional exponent operator returns the square root of x
        x // y           Floor division operator returns the integer part of the integer division of x by y
        x % y          Modulo operator returns the remainder part of the integer division of x by y


* Order of operations: The order of operations are to be calculated from left to right in the following order: 

        Parentheses ( ), { }, [ ]

        Exponents xe   (x**e)

        Multiplication * and Division /  

        Addition + and Subtraction -    

         You might find the PEMDAS mnemonic device to be helpful in remembering the order.   




* Examples of Python code


friend = 'joe'
enemy = 'saaduddin'
print("he is my friend " + friend , "& He is my enemy " + enemy)

    * output is he is my friend joe & He is my enemy saaduddin            # this output is just for refferal


friends = ['Taylor', 'Alex', 'Pat', 'Eli']
for friend in friends:
    print("Hi " + friend)


    * Output is Hi Taylor           # this output is just for refferal
                Hi Alex
                Hi Pat 
                Hi Eli


for i in range(10):
  print("Hello, World!")


    *output is 
        Hello, World!           #this output is just for refferal
Hello, World!
Hello, World!
Hello, World!
Hello, World!
Hello, World!
Hello, World!
Hello, World!
Hello, World!
Hello, World!


print(-1/4)

    * output is -0.25           # this output is just for refferal



print(1/3)
    * output is o. 3333333333333333         # this output is just for refferal


print (((1+2)*3)/4)

    * output is 2.25                                                      # this output is just for refferal


print (2**25)                                                             #'**' here refers to making 2 to the power of 25

    * output is 33554432                                                  # this output is just for refferal


# Multiplication, division, addition, and subtraction
print(3*8/2+5-1)
 
# Exponents
print(4**6) # Syntax means 4 to the power of 6
print(4**2) # To square a number
print(4**3) # To cube a number
print(4**0.5) # To find the square root of a number

# To calculate how many different possible combinations can be
# formed using a set of "x" characters with each character in "x"
# having "y" number of possible values, you will need to use an 
# exponent for the calculation:
x = 4
y = 26
print(y**x)


    * output 
            16.0
            4096
            16
            64
            2.0
            456976


# Assignment of values to the variables:
years = 10
weeks_in_a_year = 52
# This variable is assigned an arithmetic calculation:
weeks_in_a_decade = years * weeks_in_a_year
# Prints the calculation stored in the "weeks_in_a_decade" variable:
print(weeks_in_a_decade)



        * output 

            520


total_computers = 30*20
replacement_cycle = 5
computers_per_year = total_computers / replacement_cycle


print(computers_per_year) # Should print 120.0




Lists and summarizes Python’s built-in functions----> https://docs.python.org/3/library/functions.html

Lists Python’s reserved keywords and a brief description of what each keyword does ----> https://www.w3schools.com/python/python_ref_keywords.asp

Provides more examples of the proper syntax for using arithmetic operators in Python ----> https://flexiple.com/python/arithmetic-operators-in-python/


Online Python Compliler ----> https://rextester.com/l/python3_online_compiler



# week 2

* Expressions &  Variables

    * There are four data types ,

        * Integer : a number that is not a fraction; a whole number.

        * string : A string is a data type used in programming, that is used to represent text rather than numbers. A string is a sequence of characters and can contain letters, numbers, symbols and even spaces. It must be enclosed in quotation marks for it to be recognized as a string.

        * float : Float is a function or reusable code in the Python programming language that converts values into floating point numbers. Floating point numbers are decimal values or fractional numbers like 133.5, 2897.11, and 3571.213, whereas real numbers like 56, 2, and 33 are called integers.

        * boolean : It's used to represent the truth value of an expression. For example, the expression 1 <= 2 is True , while the expression 0 == 1 is False .


    print( 7 + "8")

    output is TypeError: unsupported operand type(s) for +: 'int' and 'str'


        * we cannot use a integer & a string together like this because adding a integer that is 7 with a string "8" is unsensical. adding 7 with a string "8" has no output so it is throughing an error.


*  variables: the computer stores the given variable as a chuck of data in its memory. this lets computer to access the data to read.

script : 

length = 10                             # Assisgnment
width = 2                               # Assisgnment
area= length * width                    # Expression
print(area)


output is 20                     # this output is just for refferal

* Assisgnment: the process of storing a value inside a variable is called assisgnment

*  Expression: A combinations of nos,sysbols or other variables that produce a result when evaluated is called expression.



# valid & invalid variables: There are some restrictions for using 

i_am_a_variable is valid

i_am_a_variable2 is valid

1_am_a_variable is invalid  # this is invalid bcz a variable should begin with a letter or underscore.

apple_&_oranges is invalid  # this is invalid bcz it is using a special character. python variables are case-sensitive, so capitalization matters.but lowercase,uppercase & allcapsnameis all valid in variables
