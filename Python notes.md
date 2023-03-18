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


* Implicit conversion: The Interpreter automatically converts one data type into another.

eg: 
print ("this"+ "is" + "pretty" + "neat!" )

output:
    this is pretty neat!   # this interpreter automatically indentifies the strings & add another string together. This is pretty neat! Just don't forget to add spaces to each word. Otherwise, the computer will run them all together.


* explicit conversion : In Python, to convert between one data type and another, we call a function with the name of the type we're converting to.


    eg :    In this scenario, we have a directory with 5 files in it. Each file has a different size: 2048, 4357, 97658, 125, and 8. Fill in the blanks to calculate the average file size by having Python add all the values for you, and then set the files variable to the number of files. Finally, output a message saying "The average size is: " followed by the resulting number. Remember to use the str() function to convert the number into a string. 

total = 2048 + ___ + ___ + ___ + ___
files = ___
average = total / files
print("___" + str(___))   


    * output :              # We combine one data type to another using explicit conversion. We can call str() function to do this .


* Implicit vs Explicit Conversion:As we saw earlier in the video, some data types can be mixed and matched due to implicit conversion. Implicit conversion is where the interpreter helps us out and automatically converts one data type into another, without having to explicitly tell it to do so.

By contrast, explicit conversion is where we manually convert from one data type to another by calling the relevant function for the data type we want to convert to. We used this in our video example when we wanted to print a number alongside some text. Before we could do that, we needed to call the str() function to convert the number into a string. Once the number was explicitly converted to a string, we could join it with the rest of our textual string and print the result.


* Study Guide: 

* Expressions and Variables: This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

In the Expressions and Variables segment, you learned about expressions, variables, and the data types: string, integer, and float. You learned how to convert a value from one data type to another and you learned how to resolve a few common errors in Python.

* Terms

* expression - a combination of numbers, symbols, or other values that produce a result when evaluated

* data types - classes of data (e.g., string, int, float, Boolean, etc.), which include the properties and behaviors of instances of the data type (variables)

* variable - an instance of a data type class, represented by a unique name within the code, that stores changeable values of the specific data type

* implicit conversion - when the Python interpreter automatically converts one data type to another

* explicit conversion - when code is written to manually convert one data type to another using a data type conversion function:

        str() - converts a value (often numeric) to a string data type

        int() - converts a value (usually a float) to an integer data type

        float() - converts a value (usually an integer) to a float data type

 

* Coding skills
* Skill Group 1

    Use the assignment operator =  to assign values to variables

    Use basic arithmetic operators with variables to create expressions

    Use explicit conversion to change a data type from float to string


    # The following lines assign the variable to the left of the = 
    # assignment operator with the values and arithmetic expressions 
    # on the right side of the = assignment operator.
    hotel_room = 100
    tax = hotel_room * 0.08
    total = hotel_room + tax
    room_guests = 4
    share_per_person = total/room_guests 
 
    # This line outputs the result of the final calculation stored
    # in the variable "share_per_person"
    print("Each person needs to pay: " + str(share_per_person)) # change a data type


    * output: Each person needs to pay: 27.0


* Skill Group 2

    Output multiple string variables on a single line to form a sentence

    Use the plus (+) connector or a comma to connect strings in a print() function

    Create spaces between variables in  a print() functionv


    # The following 5 lines assign strings to a list of variables.
salutation = "Dr."
first_name = "Prisha"
middle_name = "Jai"
last_name = "Agarwal"
suffix = "Ph.D."
 
print(salutation + " " + first_name + " " + middle_name + " " + last_name + ", " + suffix) 
# The comma as a string ", " adds the conventional use of a comma plus a 
# space to separate the last name from the suffix.
 
# Alternatively, you could use commas in place of the + connector:
print(salutation, first_name, middle_name, last_name,",", suffix)
# However, you will find that this produces a space before a comma within a string.


* output : Dr. Prisha Jai Agarwal, Ph.D.
Dr. Prisha Jai Agarwal , Ph.D.


* Skill Group 3

Resolve TypeError caused by a data type mismatch issue

Use an explicit conversion function

    print("5 * 3 = " + str(5*3)) 
 
# Resolution: 
# print("5 * 3 = " + str(5*3))
#
# To avoid a type error between the string and the integer within the
# print() function, you can make an explicit data type conversion by
# using the str() function to convert the integer to a string. 

    * output : 5 * 3 = 15


* Skill Group 4

Resolve a ZeroDivisionError caused by an attempt to divide by 0

numerator = 7
denominator = 2   # Possible resolution: Change the denominator value 
result = numerator / denominator
print(result)
 
# One possible assumption for a number divided by zero error might
# include the issue of a null value as a denominator (could happen when
# using a loop to iterate over values in a database). In such cases, the
# desired outcome may be to leave the numerator value intact. The
# numerator value can be preserved by reassigning the denominator with 
# the integer value of 1. The result would then equal the numerator

 * output : 3.5


* Define your own function: We can define our own set of keywords in python using "def" keyword like this,

def greeting(name):
    print("Welcome, " + name)               # print functions should be under def(indentation)

            after we define this function we have to call the greeting defined above like this,

greeting("mirza")

    output: Welcome, mirza          # this def keyword achieves what we defined in the code as greeting.


    eg: def greeting (name, department):
 print( "Welcome, " + name )
 print("You are department of " + department)

greeting ("mirza","IT sector")

output: Welcome, mirza
You are department of IT sector


* Extra notes: We looked at a few examples of built-in functions in Python, but being able to define your own functions is incredibly powerful. We start a function definition with the def keyword, followed by the name we want to give our function. After the name, we have the parameters, also called arguments, for the function enclosed in parentheses. A function can have no parameters, or it can have multiple parameters. Parameters allow us to call a function and pass it data, with the data being available inside the function as variables with the same name as the parameters. Lastly, we put a colon at the end of the line.

After the colon, the function body starts. It’s important to note that in Python the function body is delimited by indentation. This means that all code indented to the right following a function definition is part of the function body. The first line that’s no longer indented is the boundary of the function body. It’s up to you how many spaces you use when indenting -- just make sure to be consistent. So if you choose to indent with four spaces, you need to use four spaces everywhere in your code.



* Returning Values: this is keyword is used to use the value later the code.these keyword can be used multiple times the code to call the value of the keyword.

def area_triangle(base,height):
 return base*height/2                   #the return keyword doesnt print the value rightaway but stores the value to be used later in the code.

area_a= area_triangle(5,7)
area_b=area_triangle(7,3)
sum=area_a+ area_b              #
print("the sum of both area is " + str(sum))

* output : 20.5

Another example for returning value: 

def convert_seconds(seconds):
 hours = seconds //3600         # here // (floor division) means which will take the value of hours as an integer instead of decimal.eg : if the result value of hours is 2.5 , the floor division value will take 2 (integer)as the result 
 minutes = (seconds - hours * 3600) //60
 remaining_seconds = seconds - hours * 3600 - minutes *60
 return hours, minutes, remaining_seconds

hours, minutes, seconds = convert_seconds(5000)
print (hours , minutes , seconds)


output : 1 23 20

* None: A special data type in python used to indicate that things are empty or that they returned nothing.Sometimes we don't want a function to simply run and finish. We may want a function to manipulate data we passed it and then return the result to us. This is where the concept of return values comes in handy. We use the return keyword in a function, which tells the function to pass data back. When we call the function, we can store the returned value in a variable. Return values allow our functions to be more flexible and powerful, so they can be reused and called multiple times.

Functions can even return multiple values. Just don't forget to store all returned values in variables! You could also have a function return nothing, in which case the function simply exits.

    eg : 

def greeting(name):
 print("welcome, " + name)

result = greeting("christine")
welcome, christine
print(result)


* The Principles of Code Reuse: 
name="kay"
number= len(name) * 9       # len : this a length of the paranthesis
print("hello "+ name+ ". Your lucky number is " + str(number))

name="cameron"
number= len(name) * 9
print("hello "+ name+ ". Your lucky number is " + str(number))

    output : hello kay. Your lucky number is 27
hello cameron. Your lucky number is 63 

    This above code can be written in a simple way for the code to be used in multiple places, Like this 


def lucky_number(name):
 number=len(name) * 9
 print ("Hello " + name + ". Your lucky number is " + str(number))

 lucky_number('sujay")
 lucky_number("john")
