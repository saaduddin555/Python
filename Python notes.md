# PYTHON

# Week 1

#  Programming concepts: 

# Functions:
A function is a piece of code that performs a unit of work. In the examples you've seen so far, you have only encountered the print() function, which outputs a message to the screen. 


# Keywords:
A keyword is a reserved word in a programming language that performs a specific purpose.These are some of the keywords,

        Values: True, False, None
        Conditions: if, elif, else
        Logical operators: and, or, not
        Loops: for, in, while, break, continue
        Functions: print, def, return

# Arithmetic operators: 
Python can calculate numbers using common mathematical operators, along with some special operators, too: 


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


# Order of operations:
The order of operations are to be calculated from left to right in the following order: 

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

# Expressions &  Variables

    * There are four data types ,

        * Integer : a number that is not a fraction; a whole number.

        * string : A string is a data type used in programming, that is used to represent text rather than numbers. A string is a sequence of characters and can contain letters, numbers, symbols and even spaces. It must be enclosed in quotation marks for it to be recognized as a string.

        * float : Float is a function or reusable code in the Python programming language that converts values into floating point numbers. Floating point numbers are decimal values or fractional numbers like 133.5, 2897.11, and 3571.213, whereas real numbers like 56, 2, and 33 are called integers.

        * boolean : It's used to represent the truth value of an expression. For example, the expression 1 <= 2 is True , while the expression 0 == 1 is False .


    print( 7 + "8")

    output is TypeError: unsupported operand type(s) for +: 'int' and 'str'


        * we cannot use a integer & a string together like this because adding a integer that is 7 with a string "8" is unsensical. adding 7 with a string "8" has no output so it is throughing an error.


# variables: 
the computer stores the given variable as a chuck of data in its memory. this lets computer to access the data to read.

script : 

length = 10                             # Assisgnment
width = 2                               # Assisgnment
area= length * width                    # Expression
print(area)


output is 20                     # this output is just for refferal

# Assisgnment:
the process of storing a value inside a variable is called assisgnment


#  Expression:
A combinations of nos,sysbols or other variables that produce a result when evaluated is called expression.



# valid & invalid variables: There are some restrictions for using 

i_am_a_variable is valid

i_am_a_variable2 is valid

1_am_a_variable is invalid  # this is invalid bcz a variable should begin with a letter or underscore.

apple_&_oranges is invalid  # this is invalid bcz it is using a special character. python variables are case-sensitive, so capitalization matters.but lowercase,uppercase & allcapsnameis all valid in variables


# Implicit conversion:
The Interpreter automatically converts one data type into another.

eg: 
print ("this"+ "is" + "pretty" + "neat!" )

output:
    this is pretty neat!   # this interpreter automatically indentifies the strings & add another string together. This is pretty neat! Just don't forget to add spaces to each word. Otherwise, the computer will run them all together.


# Explicit conversion :
In Python, to convert between one data type and another, we call a function with the name of the type we're converting to.


    eg :    In this scenario, we have a directory with 5 files in it. Each file has a different size: 2048, 4357, 97658, 125, and 8. Fill in the blanks to calculate the average file size by having Python add all the values for you, and then set the files variable to the number of files. Finally, output a message saying "The average size is: " followed by the resulting number. Remember to use the str() function to convert the number into a string. 

total = 2048 + ___ + ___ + ___ + ___
files = ___
average = total / files
print("___" + str(___))   


    * output :              # We combine one data type to another using explicit conversion. We can call str() function to do this .


# Implicit vs Explicit Conversion:
As we saw earlier in the video, some data types can be mixed and matched due to implicit conversion. Implicit conversion is where the interpreter helps us out and automatically converts one data type into another, without having to explicitly tell it to do so.

By contrast, explicit conversion is where we manually convert from one data type to another by calling the relevant function for the data type we want to convert to. We used this in our video example when we wanted to print a number alongside some text. Before we could do that, we needed to call the str() function to convert the number into a string. Once the number was explicitly converted to a string, we could join it with the rest of our textual string and print the result.


* Study Guide: 

* Expressions and Variables: This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

In the Expressions and Variables segment, you learned about expressions, variables, and the data types: string, integer, and float. You learned how to convert a value from one data type to another and you learned how to resolve a few common errors in Python.

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



# Returning Values:
This is keyword is used to use the value later the code.these keyword can be used multiple times the code to call the value of the keyword.

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

* code style: we can write code in our own style but using right words make the code more readable by you & to others.

    eg:

def calculate(d):
 q = 3.14
 z = q * (d**2)
 print (z)

 this above use is messer to read & understand as we dont know what we are doing with it. But you can re-write this code in a more readable format, like this one

 def circle_area(radius):
 pi = 3.14
 area = pi * (radius ** 2)
 print (area)

 circle_area(5)

        By doing this we are achieving a high read ability & understanding of the code.

        * output : 78.5


* Extra notes:

* Study Guide: Functions
This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

In the Functions segment, you learned how to define and call functions, utilize a function’s parameters, and return data from a function. You also learned how to differentiate and convert between different data types utilizing variables. Plus, you learned a few best practices for writing reusable and readable code. 

# Terms
    * return value - the value or variable returned as the end result of a function

    * parameter (argument) -  a value passed into a function for use within the function

    * refactoring code - a process to restructure code without changing functionality

* Knowledge
The purpose of the def() keyword is to define a new function. 

Best practices for writing code that is readable and reusable:

Create a reusable function - Replace duplicate code with one reusable function to make the code easier to read and repurpose.

Refactor code - Update code so that it is self-documenting and the intent of the code is clear.

Add comments - Adding comments is part of creating self-documenting code. Using comments allows you to leave notes to yourself and/or other programmers to make the purpose of the code clear.


# Quiz:

1.

Question 1
This function converts miles to kilometers (km).

Complete the code to return the result of the conversion.

NOTE: The following items occur outside of the function. Do not try to change the indentations on the associated code or you will receive an error. 

Call the function to convert the trip distance from miles to kilometers. 

Fill in the blank to print the result of the conversion. 

Calculate the round-trip in kilometers by doubling the result, and fill in the blank to print the result. 


# 1) Complete the function to return the result of the conversion
def convert_distance(miles):
	km = miles * 1.6  # approximately 1.6 km in 1 mile
	return km

# Do not indent any of the following lines of code as they are 
# meant to be located outside of the function above

my_trip_miles = 55

# 2) Convert my_trip_miles to kilometers by calling the function above
my_trip_km = 1.6 * (my_trip_miles)

# 3) Fill in the blank to print the result of the my_trip_km conversion
print("The distance in kilometers is " + str(my_trip_km))

# 4) Calculate the round-trip in kilometers by doubling the result of
#    my_trip_km. Fill in the blank to print the result.
print("The round-trip in kilometers is " + str(2*my_trip_km))

output : the code is right


2.

Question 2

This function compares two numbers and returns them in increasing order.

Fill in the blanks, so the print statement displays the result of the function call in order.

Hint: if a function returns multiple values, don't forget to store these values in multiple variables


# This function compares two numbers and returns them
# in increasing order.
def order_numbers(number1, number2):
	if number2 > number1:
		return number1, number2
	else:
		return number2, number1

# 1) Fill in the blanks so the print statement displays the result
#    of the function call
smaller, bigger = order_numbers(100, 99)
print(smaller, bigger)



3.
Question 3

What are the values passed into functions as input called?

Parameters


4.
Question 4

Complete the first line of the “print_seconds” function so that it accepts three parameters: hours, minutes, and seconds. Remember to use the “def” keyword to tell the Python interpreter the block of code is intended to define a function.

def print_seconds(hours, minutes, seconds):
    print(hours*3600+minutes*60+seconds)


print_seconds(1,2,3)

output: Here is your output:
3723

Correct. The formula should multiply the hours variable by
3600 and the minutes variable by 60, then add these two
products to the seconds variable.


* Comparison Operators with Equations
The following examples demonstrate how to use comparison operators with the data types int (integers, whole numbers) and float (number with a decimal point or fractional value). Comparison operators return Boolean results. As you learned previously, Boolean is a data type that can hold only one of two values: True or False.  

    * The comparison operators include: 

==    (equality) 

!=     (not equal to) 

>       (greater than)

<      (less than)

>=    (greater than or equal to)

<=    (less than or equal to)


PART 1: Equality == and Not Equal To != Operators
In Python, you can use comparison operators to compare values. When a comparison is made, Python returns a Boolean result: True or False. Note that Boolean data types are not string data types (Boolean True is not equal to the string "True").  

To check if two values are the same, use the equality operator: == 

To check if two values are not the same, use the not equal to operator: != 

The print() function can be used to display the results of the comparisons.

Examples:

print(32 == 30+2)   # The == operator checks if the 2 values are 
True                # equal to each other. If they are equal, 
                    # Python returns a True result.


print(5+10 == 6+7)  # If the two values are not equal, as in the
False               # expression 5+10 == 6+7 (or 15 == 13), Python          
                    # returns a False result.


print(10-4 != 10+4) # The != operator checks if the 2 values are
True                # NOT equal to each other. If true, Python              
                    # returns a True result. 


print(9/3 != 3*1)   # In this last example, 9/3 != 3*1 (or 3 != 3)
False               # is false. So, Python returns a False value.

    

The equality == operator versus the equals = operator 
It is important to note that the equality == comparison operator performs a different task than the equals = assignment operator. The equals = operator assigns the value on the right side of the equals = to the object (e.g., a variable) on the left side of the equals = operator. 



# The = equals assignment operator is used to assign a value to a 
# variable.

my_variable = 3*5           # Assigns a value to my_variable      
print(my_variable)          # Printing the variable returns the 
15                          # value assigned to the variable.


                              
# The == equality comparison operator checks if the values of the two
# expressions on either side of the == operator are equivalent to one 
# another.
      
print(my_variable == 3*5)   # Printing the variable returns a Boolean 
True                        # True or False result. 


PART 2: Greater Than > and Less Than < Operators
The comparison operators greater than > and less than < also return a True or False Boolean result after comparing two values.

To check if one value is larger than another value, use the greater than operator: > 

To check if one value is smaller than another value, use the less than operator: < 

Examples:


print(11 > 3*3)         # The > operator checks if the left value is
True                    # greater than the right value. If true, it
                        # returns a True result.


print(4/2 > 8-4)        # If the > operator finds that the left value
False                   # is NOT greater than the right value, the
                        # comparison will return a False result.


print(4/2 < 8-4)        # The < operator checks  if the left value is
True                    # less than the right side. If true, the
                        # comparison returns a True result.


print(11 < 3*3)         # If the < operator finds that the left side is False                   # NOT less than the right value, Python returns
                        # a False result.


PART 3: Greater Than or Equal to >= and Less Than or Equal to <= Operators
Like the other comparison operators, the greater than or equal to >= and less than or equal to <= operators return a True or False Boolean result when a comparison is made.

To check if one value is larger than or equal to another value, use the greater than or equal to operator: >= 

To check if one value is smaller than or equal to another value, use the less than or equal to operator: <= 

Examples:



print(12*2 >= 24)   # The >= operator checks if the left value is
True                # greater than or equal to the right value. 
                    # If one of these conditions is true,  
                    # Python returns a True result. In this case  
                    # the two values are equal. So, the comparison
                    # returns a True result.


print(18/2 >= 15)   # If the >= comparison determines that the left False
False               # value is NOT greater than or equal to the
                    # right, it returns a False result.

print(12*2 <= 30)   # The <= operator checks if the left value is
True                # less than or equal to the right value. In 
                    # this case, the left value is less than the
                    # right value. Again, if one of the two 
                    # conditions is true, Python returns a True
                    # result.


print(15 <= 18/2)   # If the <= comparison determines that the left 
False               # value is NOT less than or equal to the right
                    # value, the comparison returns a False result. 


# Comparison Operators with Strings
In this reading, you will learn more about what comparison operators can and cannot do. If you use the == (equality) and != (not equal to) operators with strings, you can check if two strings contain the same text or not. You can also alphabetize strings using > (greater than), < (less than), >= (greater than or equal to), <= (less than or equal to) comparison operators. As with numeric data types, comparison operators used with strings will return Boolean (True, False) results.  

  

PART 1: Equality == and Not Equal to != Operators with Strings
In Python, you can use comparison operators to compare strings. The equality == and the not equal to != operators are helpful when you need to search for a specific string in a body of text, a log file, a spreadsheet, a database, and more. You can also check user input strings to compare them to another string. Note that Boolean data types are not string data types (Boolean True is not equal to the string "True").  

Examples:

# The == operator can check if two strings are equal to each other. 
# If they are equal, the Python interpreter returns a True result.
print("a string" == "a string")
True


# In this example, the equality == comparison is between "4 + 5" and
# 4 + 5. Since the left data type is a string and the right data type
# is an integer, the two values cannot be equal. So, the comparison
# returns a False result.
print("4 + 5" == 4 + 5)
False


# The != operator can check if the two strings are NOT equal to each
# other. If they are indeed not equal, then Python returns a True result.
print("rabbit" != "frog")
True


# In this example, the variable event_city has been assigned the string 
# value "Shanghai". This variable is compared to a static string, 
# "Shanghai", using the != operator. As, the strings "Shanghai" and 
# "Shanghai" are the same, the comparison of "Shanghai" != "Shanghai" 
# is false. Accordingly, Python will return a False result.
event_city = "Shanghai"
print(event_city != "Shanghai")
False

# This last example illustrates the result of trying to compare two
# items of different data types using the equality == operator. The
# two items are not equal, so the comparison returns False.
print("three" == 3)
False


PART 2: The Greater Than > and Less Than < Operators
The comparison operators greater than > and less than < can be used to alphabetize words in Python. The letters of the alphabet have numeric codes in Unicode (also known as ASCII values). The uppercase letters A to Z are represented by the Unicode values 65 to 90. The lowercase letters a to z are represented by the Unicode values 97 to 122. 

    * To check if the first letter(s) of a string have a larger Unicode value (meaning the letter is closer to 122 or lowercase z) than the first letter of another string, use the greater than operator: >

    * To check if the first letter(s) of a string have a smaller Unicode value (meaning the letter is closer to 65 or uppercase A) than the first letter of another string, use the less than operator: < 

Like numeric comparisons with the greater than > and less than < operators, comparisons between strings also return Boolean True or False results.  

Examples: 

# The greater than > operator checks if the left string has a higher 
# Unicode value than the right string. If true, the Python interpreter
# returns a True result. Since W has a Unicode value of 87, and you can 
# easily calculate that F has a Unicode value of 70, this comparison is
# the same as 87 > 70. As this is true, Python will return a True 
# result.
print("Wednesday" > "Friday")
True
 
 
# The less than < operator checks if the left string has a lower 
# Unicode value than the right string. If you reference the Unicode 
# chart above, you can see that all lowercase letters have higher 
# Unicode values than uppercase letters. We can see that B has a 
# Unicode value of 66 and b has a Unicode value of 98. This 
# comparison is the same as 66 < 98, which is true. So, Python will 
# return a True result.
print("Brown" < "brown")
True


# If the strings have the same first few letters, the comparison will 
# cycle through each letter of each string, from left to right until it 
# finds two letters that have different Unicode values. In this example, 
# both strings share the initial substring "sun", but then have 
# different letters with different Unicode values in the fourth place 
# in each string. So, the fourth letters 'b' and 't' of the two
# strings are used for the comparison. Since 'b' does not have a higher
# Unicode value than 't', the comparison returns a False result.
print("sunbathe" > "suntan")
False


# If two identical strings are compared using the less than < comparison
# operator, this will produce a False result because they are equal.
print("Lima" < "Lima")
False


# This last example illustrates the result of trying to compare two
# items of different data types using the less than < operator. The 
# greater than > and less than operators < cannot be used to compare
# two different data types. 
print("Five" < 6)
'''
Error on line 1:
    print("Five" < 6)
TypeError: '<' not supported between instances of 'str' and 'int'


PART 3: The Greater Than or Equal To >= and Less Than or Equal To <= Operators
The greater than or equal to >= and less than or equal to <= operators can be used with strings as well. Like the other comparison operators, they will return a True or False Boolean result when a comparison is made between two strings. 

    * To check if a string has a larger or equal Unicode value than the first letter(s) of another string, use the greater than or equal to operator: >= 

    * To check if a string has a smaller or equal Unicode value than the first letter(s) of another string, use the less than or equal to operator: <=

At this point, you should be familiar with how comparison operators work in Python. Can you determine what the results will be from the comparisons listed below? When you are ready to check your answers, click Run.

    1. "my computer" >= "my chair"

    2. "Spring" <= "Winter"

    3. "pineapple" >= "pineapple"



# Use the Unicode chart in Part 2 to determine if the Unicode values of 
# the first letters of each string are higher, lower, or equal to one
# another. 


var1 = "my computer" >= "my chair"
var2 = "Spring" <= "Winter"
var3 = "pineapple" >= "pineapple"
 
print("Is \"my computer\" greater than or equal to \"my chair\"? Result: ", var1)
print("Is \"Spring\" less than or equal to \"Winter\"? Result: ", var2)
print("Is \"pineapple\" less than or equal to \"pineapple\"? Result: ", var3)



# Logical Operators

Logical operators are used to construct more complex expressions. You can make complex comparisons by joining comparison statements together using the logical operators: and, or, not. Complex comparisons return a Boolean (True or False) result. 

and 

Both sides of the statement being evaluated must be True for the whole statement to be True. 

Example: (5 > 1 and 5 < 10) = True

or 

If either side of the comparison is True, then the whole statement is True. 

Example: (color = "blue" or color = "green") = True

not 

Inverts the Boolean result of the statement immediately following it. So, if a statement evaluates to True, and we put the not operator in front of it, it would become False. 

Example: (not "A" == "A") = False


* PART 1: The and Logical Operator
In Python, you can use the logical operator and to connect more than one comparison. This type of complex comparison is used to check if two comparison statements are both True or not. You might use the and operator when you need to execute a block of code, but only if two different conditions are true. For example, you might want to write a script  that automates sending you an emergency alert if a server stops responding and there is an unusual increase in employees opening trouble tickets.  

Example 1:

The following model demonstrates the use of the and logical operator to join comparisons between two mathematical expressions. The description below the example explains the order in which Python will process the line of code. 


# Example 1

print((6*3 >= 18) and (9+9 <= 36/2))

 In the example above, the following activities were completed by Python in the following order:  

Python solves the numerical expressions using the order of operations. (6*3 >= 18) and (9+9 <= 36/2) becomes (18 >= 18) and (18 <= 18)

Python compares the results of the numerical expressions using the comparison operators (in this case >= and <=). (18 >= 18) and (18 <= 18) becomes True and True

Python checks if both sides of the logical operator "and" are true. True and True become True

Python returns a Boolean value: True or False. The complex comparison returns a True result.


* Example 2:

In this next example, "Nairobi" < "Milan" and "Nairobi" > "Hanoi", the and logical operator is connecting two string comparison statements. You learned previously that using the greater than and less than operators on strings will test the alphabetical order (technically Unicode values) of the strings. So, this complex comparison is checking if "Nairobi" is alphabetized before "Milan" (False) AND after "Hanoi" (True). 

This comparison returns a False result because both sides of the logical operator are not True. A comparison statement like this might be used to iterate through a list of names to check if they are alphabetized in the correct order.


# Example 2

print("Nairobi" < "Milan" and "Nairobi" > "Hanoi")


PART 2: The or Logical Operator
The or logical operator tests two conditions to determine if at least one side of the or logical operator is True. The result of the test can be used to trigger a block of code if at least one condition is present.

Syntax:

Expression1 or Expression2


# True or True returns True
print((15/3 < 2+4) or (0 >= 6-7))
True

# False or True returns True
print(country == "New York City" or city == "New York City")
True

# True or False returns True
print(16 <= 4**2 or 9**(0.5) != 3)
True

# False or False returns False
print("B_name" > "C_name" or "B_name" < "A_name”)
False


* PART 3: The not Logical Operator
The not logical operator inverts the value of the comparison expression. This is a helpful tool when you want to execute a block of code as long as a certain condition is not present.

If the conditional  expression is True, the not logical operator can be added to make the expression not True (False). 

If the conditional  expression is False, the not logical operator can be added to make the expression not False (True).  

Syntax:

not expression


Example 1:

# Test Example 1:

x = 2*3 > 6
print("The value of x is:")
print(x)

print("")  # Prints a blank line

print("The inverse value of x is:")
print(not x)


Example 2:

Can you determine the result of the following comparison?  

# What happens when you negate a False statement? 
# Click Run when you are ready to check your answer.


today = "Monday"
print(not today == "Tuesday") 


# The "today" variable states today is Monday. This makes the comparison
# "today == Tuesday" False. The logical operator "not" inverts the False
# result to become True. In other words, this expression asks if it is
# false that today is not Tuesday. More succinctly, "not False" means 
# True."



# if Statements Recap:

We can use the concept of branching to have our code alter its execution sequence depending on the values of variables. We can use an if statement to evaluate a comparison. We start with the if keyword, followed by our comparison. We end the line with a colon. The body of the if statement is then indented to the right. If the comparison is True, the code inside the if body is executed. If the comparison evaluates to False, then the code block is skipped and will not be run.

ex:
def hint_username(username):
    if len(username) < 3:
        print("Invalid username. Must be atleast 3 characters long")
    else:
        print("Valid Username")


# else Statements and the Modulo Operator
We just covered the if statement, which executes code if an evaluation is true and skips the code if it’s false. But what if we wanted the code to do something different if the evaluation is false? We can do this using the else statement. The else statement follows an if block, and is composed of the keyword else followed by a colon. The body of the else statement is indented to the right, and will be executed if the above if statement doesn’t execute.

We also touched on the modulo operator, which is represented by the percent sign: %. This operator performs integer division, but only returns the remainder of this division operation. If we’re dividing 5 by 2, the quotient is 2, and the remainder is 1. Two 2s can go into 5, leaving 1 left over. So 5%2 would return 1. Dividing 10 by 5 would give us a quotient of 2 with no remainder, since 5 can go into 10 twice with nothing left over. In this case, 10%2 would return 0, as there is no remainder.


example for else :
The is_positive function should return True if the number received is positive and False if it isn't. Can you fill in the gaps to make that happen?

def is_positive(number):
  if number > 0:
    return True
  else:
    return False


example of module:

def is_even(number):
  if number % 2 == 0:
    return True
  return False


# Complex Branching with elif Statements
Building off of the if and else blocks, which allow us to branch our code depending on the evaluation of one statement, the elif statement allows us even more comparisons to perform more complex branching. Very similar to the if statements, an elif statement starts with the elif keyword, followed by a comparison to be evaluated. This is followed by a colon, and then the code block on the next line, indented to the right. An elif statement must follow an if statement, and will only be evaluated if the if statement was evaluated as false. You can include multiple elif statements to build complex branching in your code to do all kinds of powerful things!

Ex:

def hint_username(username):
    if len(username) < 3:
        print("Invalid username. Must be atleast 3 characters long")
    elif len(username) > 15:
        print("Username should atleast have 15 characters")
    else:
        print("Valid Username")

* Extra notes:

Study Guide: Conditionals
This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz.  

In the Conditionals segment, you learned about the built-in Python operators used for comparing values and the logical operators for making complex comparisons. You also learned how to use operators in if-else-elif blocks. 

 

Knowledge
Comparison operators with numerical values
Comparison expressions return a Boolean result (True or False). 

x == y        If x is equal to y, return True. Else, return False.

x != y         If x is not equal to y, return True. Else, return False.

x < y          If x is less than y, return True. Else, return False.

x <= y        If x is less than or equal to y, return True. Else, return False.

x > y          If x is greater than y, return True. Else, return False.

x >= y        If x is greater or equal to y, return True. Else, return False.

Comparison operators with strings
Comparison expressions with strings also return a Boolean result (True or False).

"x" == "y"  If the words are the same, return True. Else, return False.

"x" != "y"   If the words are not the same, return True. Else, return False.

When used with strings, the following comparison expressions will alphabetize the strings.

"x" < "y"   	If string "x"  has a smaller Unicode value than string "y", return True.  Else, return False.

"x" <= "y" 	If the Unicode value for string "x" is smaller than or equal to the Unicode value of string "y", return True. Else, return False.

"x" > "y"    	If string "x" has a larger Unicode value than string "y", return True. Else, return False.

"x" >= "y"  	If the Unicode value for string "x" is greater than or equal to the Unicode value of string "y", return True. Else, return False.



# Logical operators
Logical operators are used to combine comparison expressions and also return Boolean results (True or False).

comparison1 and comparison2 

Returns a True result if both comparison1 and comparison2 are true. 

If they are not both true, return False.

comparison1 or comparison2 

Returns a True result if either comparison1 and/or comparison2 are True. 

If neither comparison is true, return False.

not comparison1

Returns the inverse Boolean value of the comparison. 

Returns a True result if comparison1 is false. 

If comparison1 is true, then returns False.

 

Syntax of an if-elif-else block

if condition1:
    action1
elif condition2:
    action2
else:
    action3

If condition1 is True:

* Then perform action1 and exit if-elif-else block

If condition2 is True:

* Then perform action2 and exit if-elif-else block

If neither condition1 nor condition2 are True:

* Then perform action3 and exit if-elif-else block

Coding skills

Skill Group 1

* Use a comparison operator with numbers

* Use a comparison operator to alphabetize strings

code:

# The value of 10*4 (40) is greater than 14+23 (37), therefore this 
# comparison expression will return the Boolean value of True.


print(10*4 > 14+23) # Should print True

# The letter "t" has a Unicode value of 116 and the letter "s" has a
# Unicode value of 115. Since 116 is not less than 115, the 
# comparison of "tall" < "short" (or 116 < 115) is False. 

print("tall" < "short")  # Should print False

Skill Group 2

* Use a function with the def() keyword

* Pass a parameter to the function

* Use an if-elif-else statement

* Assign strings to variables 

* Use conditional operators

* Return a value

code:


# This function accepts one variable as a parameter
def translate_error_code(error_code):
 
# The if-elif-else block assesses the value of the variable
# passed to the function as a parameter. The if statement uses 
# the equality operator == to test the value of the variable.
# This test returns a Boolean (True/False) result.
    if error_code == "401 Unauthorized":
# If the comparison above returns True, then the indented 
# line(s) inside the if-statement will run. In this case, the
# action is to assign a string to the translation variable.
# The remainder of the if-elif-else block will not run.
# The Python interpreter will skip to the next line outside of 
# the if-elif-else block. In this case, the next line is the 
# return value statement.  
        translation = "Server received an unauthenticated request"
 
# If the initial if-statement returns a False result, then the
# first elif-statement will run a different test on the value
# of the variable.
    elif error_code == "404 Not Found":
# If the first elif-statement returns a True result, then the
# indented line(s) inside the first elif-statement will run. 
# After this line, the remainder of the if-elif-else block will
# not run. The Python interpreter will skip to the next line
# outside of the if-elif-else block. 
        translation = "Requested web page not found on server"
 
# If both the initial if-statement and the first elif-statement 
# return a False result, then the second elif-statement will
# run.
    elif error_code == "408 Request Timeout":
# If the second elif-statement returns a True result, then the
# indented line(s) inside the second elif-statement will run. 
# After this line, the remainder of the if-elif-else block will
# not run. The Python interpreter will skip to the next line
# outside of the if-elif-else block. 
        translation = "Server request to close unused connection"
 
# If the conditional tests above do not produce a True result
# then the else-statement will run. 
    else:
        translation = "Unknown error code"
# The if-elif-else block ends.

# The next line outside of the if-elif-else block will run
# after exiting the block. In this case, the next line returns
# the output from the if-elif-else block.
    return translation

# The print() function allows us to display the output of the
# function. To call a function in a print statement, the syntax
# is print(name_of_function(parameter))
print(translate_error_code("404 Not Found"))

# Expected output:
# Requested web page not found on server


Skill Group 3

Use an if-elif-else statement with:

* comparison operators

* logical operators

code:

# Sets value of the "number" variable
number = 25

# The "number" variable will first be compared to 5. Since it is 
# False that "number" is not less than or equal to 5, the expression indented 
# under this line will be ignored. 
if number <= 5: 
   print("The number is 5 or smaller.")
 
# Next, the "number" variable will be compared to 33. Since it is 
# False that "number" is equal to 33, the expression indented under 
# this line will be ignored. 
elif number == 33:
   print("The number is 33.")
 
# Then, the "number" variable will be compared to 32 and 6. Since it 
# is True that 25 is less than 32 and greater than 6, the Python 
# interpreter will print "The number is less than 32 and/or greater
# than 6." Then, it will exit the if-elif-else statement and the remainder 
# of the if-elif-else statement will be ignored.
elif number < 32 and number >= 6:
   print("The number is less than 32 and greater than 6.")
 
else:
   print("The number is " + str(number))
 
# Expected output is: 
# The number is less than 32 and greater than 6.


Skill Group 4

* Use an if statement to calculate a return value

* Use conditional operators

* Recall the arithmetic operators // and %

# This function rounds a variable number up to the nearest 10x value
def round_up(number):
  x = 10
# The floor division operator will calculate the integer value of
# "number" divided by x: 35 // 10 will return the integer 3.
  whole_number = number // x
# The modulo operator will calculate the remainder value of "number"
# divided by x: 35 % 10 will return the remainder value 5.
  remainder = number % x
# If the remainder is greater than 0: 
  if remainder >= 5: 
# Return x multiplied by the (whole_number+1) to round up
    return x*(whole_number+1)
# Else, return x multiplied by the whole_number to round down
  return x*whole_number
 
# Calls the function with the parameter value of 35.
print(round_up(35)) # Should print 40


Coding skills

Skill Group 1

* Use a function with the def() keyword

* Pass a parameter to the function

* Use an if-elif-else block to set specific conditions for a variety of actions

* Assign strings to variables 

* Use comparison operators

* Return a value

* Call the function in a print statement and pass parameter to the function

code:

# A function is created with the def() keyword. The parameter
# variable "time_as_string" is passed to the function through a 
# call to the function.
def task_reminder(time_as_string):

    # The following if-elif-else block assigns various strings to
    # the variable "task" depending on specific conditions. The
    # test conditions are set using the == equality comparison 
    # operator. In this case, the time passed through the 
    # "time_as_string" parameter variable is tested as the 
    # specific condition. So, if the time  is "11:30 a.m.", then 
    # "task" is assigned the value: "Run TPS report".
    if time_as_string == "8:00 a.m.":
        task = "Check overnight backup images"
    elif time_as_string == "11:30 a.m.":
        task = "Run TPS report"
    elif time_as_string == "5:30 p.m.":
        task = "Reboot servers"
    # The else statement is a catchall for all other values of 
    # the "time_as_string" parameter variable not listed in the
    # if-elif block of code.
    else:
        task = "Provide IT Support to employees"

    # This line returns the value of "task" to the function call.
    return task

# This line calls the function and passes a parameter  
# ("10:00 a.m.") to the function.
print(task_reminder("10:00 a.m."))
# Should print "Provide IT Support to employees"

Skill Group 2

* Predict the output of expressions written with Python’s syntax. 

* Requires an understanding of:

    Arithmetic and logical operators 

    How functions return and print values

    How if-elif-else statements work

    Comparison operators

code:

# Example 1
# Evaluate the output of this print statement

def product(a, b):
        return(a*b)

print(product(product(2,4), product(3,5)))
 
#################################

# Example 2 
# Evaluate the output of this print statement

def difference(a, b):
        return(a-b)

def sum(a, b):
        return(a+b)

print(difference(sum(2,2), sum(3,3)))


#################################


# Example 3
# Evaluate the Boolean output of this comparison


print((5 >= 2*4) and (5 <= 4*3))


#################################


# Example 4 
# Evaluate the value of the comparison in the if statement 


x = 3
if x+5 > x**2 or x % 4 != 0:
        print("This comparison is True")


#################################


# Example 5 
# Evaluate the output of this if-elif-else statement


number = 6
if number * 2 < 14:
        print(number * 6 % 3)
elif number > 7:
        print(100 / number)
else:
        print(7 - number)


# Click Run to check your answers. If you are having trouble 
# calculating the correct answers manually, please review the
# Practice Quiz Study Guides, videos, and readings in this Module.


Skill Group 3

Create an if-elif-else statement with: 

* a complex conditional statement using both comparison and logical operators

*  values assigned to variables 

* arithmetic operators, including the modulo % operator

code:

def get_remainder(x, y):
 
  if x == 0 or y == 0 or x ==y:
    remainder = 0
  else:
    remainder = (x % y) / y
  return remainder


print(get_remainder(10, 3))


Reminder: Correct syntax is critical
Using precise syntax is critical when writing code in any programming language, including Python. Even a small typo can cause a syntax error and the automated Python-coded quiz grader will mark your code as incorrect. This reflects real life coding errors in the sense that a single error in spelling, case, punctuation, etc. can cause your code to fail. Coding problems caused by imprecise syntax will always be an issue whether you are learning a programming language or you are using programming skills on the job. So, it is critical to start the habit of being precise in your code now. 

No credit will be given if there are any coding errors on the automated graded quizzes - including minor errors. Fortunately, you have 3 optional retake opportunities on the graded quizzes in this course. Additionally, you have unlimited retakes on practice quizzes and can review the videos and readings as many times as you need to master the concepts in this course.  

Now, before starting the graded quiz, please review this list of common syntax errors coders make when writing code.

Common syntax errors:
Misspellings

Incorrect indentations

Missing or incorrect key characters:

Parenthetical types - ( curved ), [ square ], { curly }

Quote types - "straight-double" or 'straight-single', “curly-double” or ‘curly-single’

Block introduction characters, like colons - :

Data type mismatches

Missing, incorrectly used, or misplaced Python reserved words

Using the wrong case (uppercase/lowercase) - Python is a case-sensitive language

