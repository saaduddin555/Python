# python notes 2

*  week 3:

* While Loops:A while loop will continuously execute code depending on the value of a condition. It begins with the keyword while, followed by a comparison to be evaluated, then a colon. On the next line is the code block to be executed, indented to the right. Similar to an if statement, the code in the body will only be executed if the comparison is evaluated to be true. What sets a while loop apart, however, is that this code block will keep executing as long as the evaluation statement is true. Once the statement is no longer true, the loop exits and the next line of code will be executed.

NOTE: Whenever you are writing a loop, check that you're initializing all the variables you want to use before you see them.

ex: 

x = 0
while x < 5:
  print("Not there yet, x=" + str(x))
  x = x + 1
print("x=" + str(x))

Explanantion: Check out this program. Can you guess what it does? Before we execute it to find out, let's go through it together line by line. 
In the first line we're assigning the value of 0 to the variable x. We call this action initializing, to give an initial value to a variable. 
In the line after that, we're starting the while loop. We're setting a condition for this loop that x needs to be smaller than 5. Right now we know that x is 0 since we've just initialized it, so this condition is currently true. On the next two lines, we have a block that's indented to the right. Here, we can use what we learned about functions and conditionals to identify that this is the while loop's body. There are two lines in the body of the loop. In the first line, we print a message followed by the current value of x. In the second line, we increment the value of x. We do this by adding 1 to its current value and assigning it back to x. So after the first execution of the body of the loop, x will be 1 instead of 0. Because this is a loop, the computer doesn't just continue executing with the next line in the script. Instead, it loops back around to re-evaluate the condition for the while loop. And because 1 here is still smaller than 5, it executes the body of the loop again. It then prints the message and once more increments x by 1. So the x is now 2. The computer will keep doing this until the condition isn't true anymore. In this example, the condition will be false when x is no longer smaller than 5. Once the condition is false, the loop finishes, and the next line is executed. And finally, the last line of our code prints the last value of x. So now that this code makes a bit more sense, what do you think will happen when we execute it? Ready to find out? Let's execute the code and see what happens.
So we had five lines with  transcript2:28the message, Not there yet, and then at the end of the script the value of x was 5. This was a simple example of how a while loop behaves. As we've said before, we're learning the building blocks of programming. Once you know those building blocks, you can combine them to create more complex expressions. As an IT specialist, while loops can be super helpful. You can use them to keep asking for a username if the one provided isn't valid, or maybe try an operation until it succeeds. Knowing how to construct these expressions can help you get your computer to do a whole lot with only a little bit of code. It's pretty powerful stuff we're learning here. Now that you've got an idea of how a while loop works, let's spice it up with another example.

Ex:Can you work out what this function does? Try passing different parameters to the attempts function to see what it does.

def attempts(n):
    x = 1
    while x <= n:
        print("Attempt " + str(x))
        x += 1
    print("Done")
    
attempts(5)


check your output

Explanantion:Let's now apply this knowledge to a similar example, but this time with a while loop inside a function. Can you work out what this function does? In this example, we start out by initializing a variable called x. In this case, we initialize it with a value of 1. Then, we enter our while loop which checks to see if the value inside of the x variable is less than the parameter n that the function received. If that comparison evaluates to true, then the code inside the while block is executed. Say we pass a value of 5 as a parameter to this function. In the first pass through the loop, x is always equal to 1, so the comparison: 1 smaller than or equal to 5 would be true and we then enter the body of the loop. In the body, we first print a message indicating that the current attempt number and then we increase the value of x by 1. To increment the number we're using a slightly different expression than before. x +=1 is a shorthand version of x = x+1. You can use either expression since they both mean the same thing. The process continues until the result of the comparison isn't true anymore, which happens when x is bigger than n. In our current example, this would be when the value of x is 6. Let's see it in action.


Ex:
username = get_username
while not valid_username(username):
    print("Invalid username")
    username = get_username()

Explanantion:

for example, to call a separate function that evaluates the condition, like this. In this case, there's a lot of code hidden behind functions and it's doing stuff we don't see. There's a get username function that asks the user for a username and a valid_username function that validates that username. And all this is happening in just a handful of characters. As you can see, you can pack a lot of punch into just a short line of code. In this case, the body of the while loop will be executed until the user enters a valid username. The important thing to remember is that the condition used by the while loop needs to evaluate to true or false. It doesn't matter if this is done by using comparison operators or calling additional functions. The conditions used in while loops can also become more complex if we use the logical operators that we encountered when looking into branching, and, or, and not. This lets us combine the values of several expressions to get the result we want. Okay, we've now covered what a while loop is and learned its syntax and basic behavior. Some of this stuff can be a bit tricky and you're doing great, keep sticking with it. Next, we're going to do a rundown of some of the most common pitfalls that you may come across when writing your own loops. Head on over to the next video to get started.

ex:

In this code, there's an initialization problem that's causing our function to behave incorrectly. Can you find the problem and fix it?

def count_down(start_number):
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)

what is wrong with this script?


here is the solution

def count_down(start_number):
  current = 3
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)

Here is your output:
3
2
1
Zero!

You nailed it! By initializing the current variable you got
the function to behave correctly.


* Common Pitfalls With Variable Initialization
You'll want to watch out for a common mistake: forgetting to initialize variables. If you try to use a variable without first initializing it, you'll run into a NameError. This is the Python interpreter catching the mistake and telling you that you’re using an undefined variable. The fix is pretty simple: initialize the variable by assigning the variable a value before you use it.

Another common mistake to watch out for that can be a little trickier to spot is forgetting to initialize variables with the correct value. If you use a variable earlier in your code and then reuse it later in a loop without first setting the value to something you want, your code may wind up doing something you didn't expect. Don't forget to initialize your variables before using them!


* infinite loops:A loop that keeps executing & never stops.

EX:

while x % 2 == 0:
    x = x / 2

solution:

if x != 0:
  while x % 2 == 0:
    x = x / 2

or like this 

while x != 0 and x % 2 == 0:
    x = x / 2

Explananation:

Check out this example. It uses the modulo operator that we saw a while back. This cycle will finish for positive and negative values of x. But what would happen if x was zero? The remainder of 0 divided by 2 is 0, so the condition would be true. The result of dividing 0 by 2 would also be zero, so the value of x wouldn't change. This loop would go on forever, and so we'd get an infinite loop. If our code was called with x having the value of zero, the computer would just waste resources doing a division that would never lead to the loop stopping. The program would be stuck in an infinite loop circling background endlessly, and we don't want that. All that looping might make your computer dizzy. To avoid this, we need to think about what needs to happen for a loop to be successful. In this example, we said that x needs to be different than zero. So we could nest this while loop inside an if statement just like this. With this approach, the while loop is executed only when x is not zero. Alternatively, we could add the condition directly to the loop using a logical operator like in this example. This makes sure we only enter the body of the loop for values of x that are both different than zero and even.

ex:
The following code causes an infinite loop. Can you figure out what’s missing and how to fix it?

def print_range(start, end):
	# Loop through the numbers from start to end
	n = start
	while n <= end:
		print(n)

print_range(1, 5)  # Should print 1 2 3 4 5 (each number on its own line) 

find answer


* Infinite loops and Code Blocks
Another easy mistake that can happen when using loops is introducing an infinite loop. An infinite loop means the code block in the loop will continue to execute and never stop. This can happen when the condition being evaluated in a while loop doesn't change. Pay close attention to your variables and what possible values they can take. Think about unexpected values, like zero.

In the Coursera code blocks, you may see an error message that reads "Evaluation took more than 5 seconds to complete." This means that the code encountered an infinite loop, and it timed out after 5 seconds. You should take a closer look at the code and variables to spot where the infinite loop is.


# EXTRA NOTES:

*  Study Guide: while Loops
This study guide provides a quick-reference summary of what you learned in this segment and serves as a guide for the upcoming practice quiz.  

In the while Loops segment, you learned about the logical structure and syntax of while loops. You also learned about the importance of initializing variables and how to resolve infinite while loops with the break keyword.  


while Loops
A while loop executes the body of the loop while a specified condition remains True. They are commonly used when there’s an unknown number of operations to be performed, and a condition needs to be checked at each iteration.

Syntax:

while specified condition is True:
    body of loop

example for while loop:

multiplier = 1
result = multiplier*5
while result <= 50:
  print(result)
  multiplier += 1
  result = multiplier*5
print("Done")

# This while loop prints the multiples of 5 between 1 and 50. The
# "multiplier" variable is initialized with the starting value of 1. 
# The "result" variable is initialized with the value of the 
# "multiplier" variable times 5. 
 
# The while loop specifies that the loop must iterate while it is True 
# that the "result" is less than or equal to 50. Within the while loop, 
# the code tells the Python interpreter to print the value of the 
# "result" variable. Then, the "multiplier" is incremented by 1 and the
# "result" is assigned the new value of the "multiplier" times 5. 
 
# The end of the while loop is indicated by the indentation of the next 
# line of code moving one tab to the left. At this point, the Python
# interpreter automatically loops back to the beginning of the while
# loop to check the condition again with the new value of the "result"
# variable. When the while loop condition becomes False (meaning
# "result" is no longer less than or equal to 50), the interpreter exits
# the loop and reads the next line of code outside of the loop. In this 
# case, that next line tells the interpreter to print the string "Done". 
 
# Click the "Run" button to check the result of this while loop.  


* Common Errors in while Loops
If you get an error message on a loop or it appears to hang, your debugging checklist should include the following checks:

* Failure to initialize variables. Make sure all the variables used in the loop’s condition are initialized before the loop.

* Unintended infinite loops. Make sure that the body of the loop modifies the variables used in the condition, so that the loop will eventually end for all possible values of the variables. You can often prevent an infinite loop by using the break keyword or by adding end criteria to the condition part of the while loop.

 

while Loop Terms

* while loop - Tells the computer to execute a set of instructions while a specified condition is True. In other words, while loops keep executing the same group of instructions until the condition becomes False.

* infinite loop - Missing a method for exiting the loop, causing the loop to run forever.

* break - A keyword that can be used to end a loop at a specific point. 

 

Math Concepts on the Practice Quiz:The coding problems on the upcoming practice quiz will involve a few math concepts. Don’t worry if you are rusty on math. You will have plenty of support with these concepts on the quiz. The following is a quick overview of the math terms you will encounter on the quiz:  

* prime numbers - Integers that have only two factors, which are the number itself multiplied by 1. The lowest prime number is 2.

* prime factors - Prime numbers that are factors of an integer. For example, the prime numbers 2 and 5 are the prime factors of the number 10 (2x5=10). The prime factors of an integer will not produce a remainder when used to divide that integer. 

* divisor - A number (denominator) that is used to divide another number (numerator). For example, if the number 10 is divided by 5, the number 5 is the divisor.

* sum of all divisors of a number - The result of adding all of the divisors of a number together.  

* multiplication table - An integer multiplied by a series of numbers and their results formatted as a table or a list. For example:

                 4x1=4
                 4x2=8
                 4x3=12
                 4x4=16
                 4x5=20


Coding skills
Skill Group 1

Initialize a variable

* Use a while loop that runs while a specific condition is true

* Ensure the while loop will not be an infinite loop

* Increment a value within a while loop

# This function counts the number of integer factors for a 
# "given_number" variable, passed through the function’s parameters.
# The "count" return value includes the "given_number" itself as a 
# factor (n*1). 
def count_factors(given_number):
 
  # To include the "given_number" variable as a "factor", initialize
  # the "factor" variable with the value 1 (if the "factor" variable
  # were to start at 2, the "given_number" itself would be excluded). 
  factor = 1
  count = 1
 
  # This "if" block will run if the "given_number" equals 0.
  if given_number == 0:
    # If True, the return value will be 0 factors. 
    return 0
 
  # The while loop will run while the "factor" is still less than
  # the "given_number" variable.
  while factor < given_number:
    # This "if" block checks if the "given_number" can be divided by
    # the "factor" variable without leaving a remainder. The modulo
    # operator % is used to test for a remainder.
    if given_number % factor == 0:
      # If True, then the "factor" variable is added to the count of
      # the "given_number"’s integer factors.
      count += 1
    # When exiting the if block, increment the "factor" variable by 1
    # to divide the "given_number" variable by a new "factor" value
    # inside the while loop.
    factor += 1
 
  # When the interpreter exits either the while loop or the top if
  # block, it will return the value of the "count" variable.
  return count
 
print(count_factors(0)) # Count value will be 0
print(count_factors(3)) # Should count 2 factors (1x3)
print(count_factors(10)) # Should count 4 factors (1x10, 2x5)
print(count_factors(24)) # Should count 8 factors (1x24, 2x12, 3x8,
# and 4x6). 


# Skill Group 2

* Initialize variables to assign data types before they are used in a while loop 

* Use the break keyword as an exit point for a while loop

# This function outputs an addition table. It is written to end after
# printing 5 lines of the addition table, but it will break out of the
# loop if the "my_sum" variable exceeds 20. 
 
# The function accepts a "given_number" variable through its 
# parameters.
def addition_table(given_number):
 
    # The "iterated_number" and "my_sum" variables are initialized with
    # the value of 1. Although the "my_sum" variable does not need any
    # specific initial value, it still must be assigned a data type
    # before being used in the while loop. By initializing "my_sum"
    # with any integer, the data type will be set to int.
    iterated_number = 1
    my_sum = 1
 
    # The while loop will run while it is True that the   
    # "iterated_number" is less than or equal to 5.
    while iterated_number <= 5:
 
        # The "my_sum" variable is assigned the value of the
        # "given_number" plus the "iterated_number" variables.
        my_sum = given_number + iterated_number
 
        # Test to see if the "my_sum" variable is greater than 20.
        if my_sum > 20:
            # If True, then use the break keyword to exit the loop. 
            break
        # If False, the Python interpreter will move to the next line 
        # in the while loop after the if-statement has ended.  
 
        # The print function will output the "given_number" plus
        # the "iterated_number" equals "my_sum".
        print(str(given_number), "+", str(iterated_number), "=", str(my_sum))
 
        # Increment the "iterated_number" before the while loop starts
        # over again to print a new "my_sum" value.
        iterated_number += 1
 
 
addition_table(5)
addition_table(17)
addition_table(30)

# Expected output:
# 5 + 1 = 6
# 5 + 2 = 7
# 5 + 3 = 8
# 5 + 4 = 9
# 5 + 5 = 10
# 17 + 1 = 18
# 17 + 2 = 19
# 17 + 3 = 20
# None

# practice quiz

3.
Question 3
 The following code contains an infinite loop, meaning the Python interpreter does not know when to exit the loop once the task is complete. To solve the problem, you will need to:  

* Find the error in the code

* Fix the while loop so there is an exit condition

Hint: Try running your function with the number 0 as the input and observe the result. 

Note that Coursera’s code blocks will time out after 5 seconds of running an infinite loop. If you get this timeout error message, it means the infinite loop has not been fixed. 

def is_power_of_two(number):
  # This while loop checks if the "number" can be divided by two
  # without leaving a remainder. How can you change the while loop to
  # avoid a Python ZeroDivisionError?
  while number % 2 == 0:
    number = number / 2
  # If after dividing by 2 "number" equals 1, then "number" is a power
  # of 2.
  if number == 1:
    return True
  return False
  

# Calls to the function
print(is_power_of_two(0)) # Should be False
print(is_power_of_two(1)) # Should be True
print(is_power_of_two(8)) # Should be True
print(is_power_of_two(9)) # Should be False


4.
Question 4
Fill in the blanks to complete the while loop so that it returns the sum of all the divisors of a number, without including the number itself. As a reminder, a divisor is a number that divides into another without a remainder. To do this, you will need to:

* Initialize the "divisor" and "total" variables with starting values

* Complete the while loop condition

* Increment the "divisor" variable inside the while loop

* Complete the return statement


# Fill in the blanks so that the while loop continues to run while the
# "divisor" variable is less than the "number" parameter.

def sum_divisors(number):
# Initialize the appropriate variables
  ___ = ___
  ___ = ___

  # Avoid dividing by 0 and negative numbers 
  # in the while loop by exiting the function
  # if "number" is less than one
  if number < 1:
    return 0 

  # Complete the while loop
  while ___:
    if number % divisor == 0:
      total += divisor
    # Increment the correct variable
    ___ += 1

  # Return the correct variable 
  return ___


print(sum_divisors(0)) # Should print 0
print(sum_divisors(3)) # Should print 1
# 1
print(sum_divisors(36)) # Should print 1+2+3+4+6+9+12+18
# 55
print(sum_divisors(102)) # Should print 1+2+3+6+17+34+51
# 114


5.
Question 5
Fill in the blanks to complete the function, which should output a multiplication table. The function accepts a variable “number” through its parameters. This “number” variable should be multiplied by the numbers 1 through 5, and printed in a format similar to “1x6=6” (“number” x “multiplier” = “result”). The code should also limit the “result” to not exceed 25. To satisfy these conditions, you will need to:

* Initialize the “multiplier" variable with the starting value

* Complete the while loop condition

* Add an exit point for the loop

* Increment the “multiplier" variable inside the while loop

def multiplication_table(number):
    # Initialize the appropriate variable
    ___ = ___

    # Complete the while loop condition.
    while ___:
        result = number * multiplier 
        if  result > 25 :
            # Enter the action to take if the result is greater than 25
            ___
        print(str(number) + "x" + str(multiplier) + "=" + str(result))
        
        # Increment the appropriate variable
        ___ += 1


multiplication_table(3) 
# Should print: 
# 3x1=3 
# 3x2=6 
# 3x3=9 
# 3x4=12 
# 3x5=15

multiplication_table(5) 
# Should print: 
# 5x1=5
# 5x2=10
# 5x3=15
# 5x4=20
# 5x5=25

multiplication_table(8) 
# Should print:
# 8x1=8
# 8x2=16
# 8x3=24


# FOR LOOP: 
Interates over a sequence of values.

ex:
for x in range(5):
    print(x)


explanation: The first line indicates the distinguishing keyword. In this case, that's for. And it ends with a colon. The body of the loop is indented to the right, like we saw in the while loop, the if block, and the function definitions. What's different in this case is that we have the keyword in. Also, between the for keyword and in keyword, we have the name of a variable. This variable will take each of the values in the sequence that loop iterates through. So in this example, it'll iterate through a sequence of numbers generated using the range function. There are two important things I want to call out about this range function.
* First, in Python and a lot of other programming languages, a range of numbers will start with the value 0 by default.

* Second, the list of numbers generated will be one less than the given value. In the simple example here, x will take the values 0, 1, 2, 3, and 4. Let's check this out.

So there, we have a very basic for loop. It iterates over a sequence of numbers generated by the range function. When using a for loop, we point the variable defined between for and in, in this case, x, at each element of the sequence. This means on the first iteration x points at 1. On the second iteration, it points at 2, and so on. Whatever code we put in the body of the loop will be executed on each of the values, one value at a time.

Bringing this all together, the range(5) function will create a sequence of numbers from 0 to 4. Our for loop will iterate over this sequence of numbers, one at a time, making the numbers accessible via the variable x and the code within our loop body will execute for each iteration through the sequence. So for the first loop, x will contain 0, the next loop, 1, and so on until it reaches 4. Once the end of the sequence comes up, the loop will exit and the code will continue.

The power of for loops comes from the fact that it can iterate over a sequence of any kind of data, not just a range of numbers. You can use for loops to iterate over a list of strings, such as usernames or lines in a file.

Not sure whether to use a for loop or a while loop? Remember that a while loop is great for performing an action over and over until a condition has changed. A for loop works well when you want to iterate over a sequence of elements. 

* detail explanation: 
      Similar to if statements and while loops, for loops begin with the keyword for with a colon at the end of the line. Just like in function definitions, while loops and if statements, the body of the for loop begins on the next line and is indented to the right. But what about the stuff in between the for keyword and the colon? In our example, we’re using the range() function to create a sequence of numbers that our for loop can iterate over. In this case, our variable x points to the current element in the sequence as the for loop iterates over the sequence of numbers. Keep in mind that in Python and many programming languages, a range of numbers will start at 0, and the list of numbers generated will be one less than the provided value. So range(5) will generate a sequence of numbers from 0 to 4, for a total of 5 numbers.


Ex:

values = [ 23, 52, 59, 37, 48 ]
sum = 0
length = 0
for value in values:
    sum += value
    length +=1

print ("total sum : " + str(sum) + " - Average: " + str(sum/length))

explanantion:
    For example, we could iterate over a list of numbers to calculate the total sum and average. Here's one way of doing this. Here, we're defining a list of values. After that, we're initializing two variables, sum and length, that will update in the body of the for loop. In the for loop, we're iterating over each of the values in the list, adding the current value to the sum of values, and then also adding 1 to length, which calculates how many elements there are in the list. Once we've gone through the whole list, we print out the sum and the average. We'll keep using for loops in our examples every time we want to iterate over the elements of any sequence and operate with them.


Ex:

product = 1
for n in range(1,10):
    product = product * n

print(product)

Explanation:
Product = 1 for n in range(1,10): product = product * n print(product). In this example, we're calculating the products of all numbers from 1 to 10. For this operation, it's important that we start with one and not with zero. If we'd started with zero, the whole product would be zero. Additionally, we can specify a third parameter to change the size of each step. This means that instead of going one by one, we could have a larger difference between the elements.

Ex:
def to_celsius(x):
    return (x-32)*5/9

for x in range(0,101,10):
    print(x, to_celsius(x))

Explanation:Let's check out this example when you might want to do something like this. First, we're defining a function that converts a temperature value from Fahrenheit to Celsius, and we're simply using a conversion formula to do that. Then we have a for loop that starts at zero, and goes up to 100 in steps of 10. Notice that we're using 101 for the upper limit instead of 100. We're doing this because the range never includes the last element, and we want to include 100 in our range. The body of the for-loop prints the value in Fahrenheit and the value in Celsius creating a conversion table. Let's see this in action.

for x in range(0,101,10):

That example got you feeling the heat. Don't worry, there's a quick rundown of what we've learned. The range function can receive one, two or three parameters. If it receives one parameter, it will create a sequence one by one from zero until one less than the parameter received. If it receives two parameters, it will create a sequence one by one from the first parameter until one less than the second parameter. Finally, if it receives three parameters, it will create a sequence starting from the first number and moving towards the second number. But this time, the jumps between the numbers will be the size of the third number, and again, it will stop before the second number. 

* A Closer Look at the Range() Function
The in keyword, when used with the range() function, generates a sequence of integer numbers, which can be used with a for loop to control the start point, the end point, and the incremental values of the loop.  

Syntax:

for n in range(x, y, z):
    print(n)


The range() function uses a set of indices that point to integer values, which start at the number 0. The numeric values 0, 1, 2, 3, 4 correlate to ordinal index positions 1st, 2nd, 3rd, 4th, 5th. So, when a range call to the 5th index position is made using range(5) the index is pointing to the numeric value of 4.
----------------------------------------------------------------------------------
Index Number      1st index    2nd index     3rd index     4th index    5th index
----------------------------------------------------------------------------------
Value                 0             1           2              3            4
----------------------------------------------------------------------------------

The range() function can take up to three parameters:  range(start, stop, step) 

Start :

The first item in the range() function parameters is the starting position of the range. The default is the first index position, which points to the numeric value 0. This value is included in the range. 

Stop :

The second item in the range() function parameters is the ending position of the range. There is no default index position, so this index number must be given to the range() parameters. For example, the line for n in range(4) will loop 4 times with the n variable starting at 0 and looping 4 index positions: 0, 1, 2, 3. As you can see, range(4) (meaning index position 4) ends at the numeric value 3. In Python, this structure may be phrased as “the end-of-range value is excluded from the range.” In order to include the value 4 in  range(4), the syntax can be written as range(4+1) or range(5). Both of these ranges will produce the numeric values 0, 1, 2, 3, 4. 

Step:

The third item in the range() function parameters is the incremental step value. The default increment is +1. The default value can be overridden with any valid increment. However, note that the loop will still end at the end-of-range index position, regardless of the incremental value. For example, if you have a loop with the range: for n in range(1, 5, 6), the range will only produce the numeric value 1. This is because the incremental value of 6 exceeded the ending point of the range.


Practice Exercise

You can use the code block below to test the values of n with various range() parameters. A few suggestions to test are:

range(stop)

* range(3) 

* range(3+1) 

range(start, stop)

* range(2, 6)     

* range(5,10+1) 

range(start, stop, step)

* range(4, 15+1, 2)         

* range(2*2, 25, 3+2) 

* range(10, 0, -2)  

  for n in range(1, 5, 6):  
    print(n)


Examples of the range() function in code:
* Example 1

# This loop iterates on the value of the "n" variable in a range
# of 0 to 10 (the value of the end-of-range index 11 is excluded).
# The incremental value for the loop is 2. The print() function will 
# output the resulting value of "n" as the loop counts from 0 to 10 
# (end-of-range index 11) in incremental steps of 2. This is one 
# method that can be used in Python to print a list of even numbers.


for n in range(0,11,2):
    print(n)


# The loop should print 0, 2, 4, 6, 8, 10


Ex 2:

# This loop iterates on the value of the "number" variable in a range
# of 2 to 7+1 (the value of the end-of-range index 7 is excluded, so 
# +1 has been added to the parameter to include the numeric value 7 in 
# the range). The incremental value for the loop is the default of +1.
# The print() function will output the resulting value of "number" 
# multiplied by 3.


for number in range(2,7+1):
    print(number*3)


# The loop should print 6, 9, 12, 15, 18, 21


Ex 3:

# This loop iterates on the value of the "x" variable in a range
# of 2 to -1 (the end-of-range index -2 is excluded). The third 
# parameter is also a negative number, making it a decremental value
# of -1. The print() function will output the resulting value of
# "x" as it starts at 2 and counts down to -1 (index -2).


for x in range(2, -2, -1):
    print(x)


# The loop should print 2, 1, 0, -1

* Key takeaways
The roles of the range(start, stop, step) function parameters are:

* Start - Beginning of range

* value included in range

* default = 0

* Stop - End of range

value excluded from range (to include, use stop+1)

* no default

must provide the ending index number 

* Step - Incremental value 

default = 1


# NESTED FOR LOOP:
      Nested for loop is nothing but using for loop inside a for loop like this.


for left in range(7):
    for right in range(left,7):
        print("[" + str(left) + "|" + str(right) + "]" , end=" ")
    print()

-------------------
end=" "

In this code, we're using a new parameter that we passed to the print function. This parameter is called end=" ". Normally, once print has taken the content we passed and written it to the screen, then it writes a special character that creates a new line called the newline character. If we want print to write something else instead of the newline character, we use the end=" " parameter, like we see in this example.


ex:

teams = [ 'Dragons' , 'wolves' , 'pandas' , 'unicorns']
for home_team in teams:
    for away_team in teams:
        if home_team !=  away_team:
            print(home_team + " Vs " + away_team)


explanation:
 Let's say you run a local girl's basketball league in your town. You have four teams that will play against each other in the league, both at home and away. You've stored the names of the teams in a list, like this: teams = [ ‘Dragons’, ‘Wolves’, ‘Pandas’, ‘Unicorns’] We want to write a script that will output all possible team pairings. For this, the order of the names matters because for each game, the first name will be the home team and the second name is the away team. Of course, what we don't want to do is have a team playing against itself. So what statement do we need to use to avoid that? To do this, we need to use a conditional that makes sure we only print the pairing when the names are different. Check out what this looks like. for home_team in teams: for away_team in teams: if home_team != away_team: print(home_team + “ vs ” + away_team) Success! As you can see, nested loops are super useful for solving certain problems, like pairing teams.


* Study Guide: for Loops
This study guide provides a summary of what you learned in this segment and serves as a guide for the upcoming practice quiz.  

In the for Loops segment, you learned about the logical structure and syntax of for loops. You took a closer look at the range() function. You learned about nested for loops and complex nested for loops with if statements. You also learned how to fix common errors in for loops.


* for Loops vs. while Loops
for loops and while loops share several characteristics. Both loops can be used with a variety of data types, both can be nested, and both can be used with the keywords break and continue. However, there are important differences between the two types of loops: 

while loops are used when a segment of code needs to execute repeatedly while a condition is true

for loops iterate over a sequence of elements, executing the body of the loop for each element in the sequence

Syntax 
The syntax of a for loop with the in keyword:

for variable in sequence:
    body of loop


* Common for Loop Structures 
for Loop with range()
The in keyword with the range() function generates a sequence of integer numbers, which can be used with a for loop to configure the iterations of the code. The range of numbers [0, 1, 2] correlates to ordinal index positions (1st, 2nd, 3rd), rather than the cardinal (quantity) values of the numbers 0, 1, and 2. For example, range(5) means the five index positions in the range [0, 1, 2, 3, 4]. 

The range() function can take up to three parameters. The roles of the three possible range(x,y,z) parameters are:

x = Start - Starting index position of the range 

* Default index position is 0.

* The starting index position is included in the range. 

*  Example syntax: range(2, y, z) or range(x+3, y, z) 

y = Stop - Ending index position of range

* No default index position. Must include the ending index position in the range() parameters.

  * Example syntax: range(y)

* The value of the ending index position is excluded from the range. 

* To include the ending index number, use the expression: y+1 (index + 1)

* Example syntax: range(x, y+1, z)

* Alternatively, if y = 10, you can write: range(x, 11, z)

z = Step - Incremental value

* Default increment is +1.

* The default value can be overridden with any valid increment.

* The incremental value will end the for loop before it reaches the end of range index position (end of range index minus 1).


Example of a for loop with the in keyword and the range() function:

# This loop iterates on the value of the "number" variable in a range
# of 1 to 6+1 (the upper range limit of 6 is excluded, so +1 has
# been added to it to include 6 in the range). The incremental value
# for the loop is 2 (number+2). The print() function will output the
# resulting value of "number" multiplied by 3.


for number in range(1,6+1,2):
    print(number*3)


# The loop should print 3, 9, 15


* Common pitfalls when using the range() function:
Forgetting that the upper limit of a range() isn’t included in the range.

Iterating over non-sequences. For example, strings are iterable letter by letter, but not word by word. 

# This loop iterates on the value of the "number" variable in a range
# of 2 to 7 (the upper range limit of 8 is excluded). The print() 
# function will output the resulting value of "number" squared.


for number in range(2,8):
    print(number**2)


# The loop should print 4, 9, 16, 25, 36, 49


* Nested for Loops 
The syntax of nested for loops:

for x in sequence:
    # start of the outer loop body
    for y in sequence:
        # start of the inner loop body

        # end of of the inner loop body
    # continue body of the outer loop
    # end of the outer loop body



Example of nested for loops:  

# This code demonstrates the outer and inner loop iterations of a pair 
# of nested for loops. Click "Run" to see the results. The outer loop
# will run twice for the range pointer positions [0, 1] in range(2).
# The inner loop will run 4 times for the range pointer positions 
# [0, 1, 2, 3] in range(3+1) or range(4) each time the outer loop runs.
# So, the inner loop will execute 8 times in total.


for x in range(2):
    print("This is the outer loop iteration number " + str(x))
    for y in range(3+1):
        print("Inner loop iteration number " + str(y))
    print("Exit inner loop") 


* for Loop with nested if Statement
The syntax of a for Loop with nested if Statement:

for x in sequence:
    # start of body of for loop
    if condition is true:
        # start of body of if-statement

        # end of body of if-statement
    # continue body of for loop
    # end of body of for loop


ex:
a for Loop with Nested if Statement:  

# This for loop iterates through the numbers 0 to 6. The if statement
# uses the modulo operator to test if the "x" variable is divisible by
# 2. If True, the if statement will print the value of "x" and exit
# back into the for loop for the next iteration of "x". Since no 
# incremental value is specified in the range() parameters, the default
# increment is +1. 


for x in range(7):
    if x % 2 == 0:
        print(x)


# The loop should print 0, 2, 4, 6


# PRACTICE QUIZ

2.
Question 2
Which option would fix this for loop to print the numbers 12, 18, 24, 30, 36?

for n in range(6,18,3):
    print(n*2)


3.
Question 3
Which for loops will print all even numbers from 0 to 18? Select all that apply.



4.
Question 4
Fill in the blanks so that the for loop will print the first 10 cube numbers (x**3) in a range that starts with x=1 and ends with x=10.


for __ in range(__,__):
  print(__)



5.
Question 5
Write a for loop with a three parameter range() function that prints the multiples of 7 between 0 and 100. Print one multiple per line and avoid printing any numbers that aren't multiples of 7. Remember that 0 is also a multiple of 7. 


for ___: 
    print(___)


# common error:

for x in 25:
    print(x)

what went wrong : As you see here: for x in 25: print(x) In this example, we're trying to iterate over the number 25. Python prints a TypeError telling us that integers are not iterable.

solution:

for x in range(25):
    print(x)


There are two solutions to this problem, depending on what we're trying to do. If we want to go from zero to 25, then we use the range function: for x in range(25): print(x)


 for x in [25]:
    print(x)

 but if we're trying to iterate over a list that has 25 as the only element, then it needs to be a list and that means writing it between square brackets: for x in [25]: for x in [25]: print(x) You might be wondering why you'd ever want to iterate over a list of one element and that's a good question. Well, this kind of issue usually happens when you have a function with a for loop inside it, which is iterating over the elements of a list received by parameter. Say for example, you have a function that fixes the permissions of a list of files received by parameter, and you want to call this function to fix the permissions of just one specific file. To do that, you need to pass the file as the single element of a list. 

ex:


def greet_friends(friends):
    for friend in friends:
        print("Hi " + friend)

greet_friends(['Mirza' , 'saad ' , 'joe'])


explanantion:We're going to modify it to have the greetings inside a function. We've defined a greet friends function, that receives a list by parameter and iterates over that list, greeting each friend. But what if we only want to greet one friend instead of four? Well, we still need to define a list, but with only one element. But first, let's see what would happen if we don't do that: greet_friends("Barry")


greet_friends("Barry")

output:
Hi b
Hi a
Hi r
Hi r
Hi y

This happens because strings are iterable, the for loop will go over each letter of the string and do the operation we asked it to do, which in this case, print a greeting. Depending on what you're trying to do, you may actually want to iterate through the letters of a string. But in this case, we don't. So to sum it up, if you get an error that a certain type isn't iterable, you need to make sure the for loop is using a sequence of elements and not just one, and if you find your code iterating through each letter of a string when you want it to do it for the whole string, you probably want to have that string be a part of a list.


* Recursion:
    Recursion is the repeated application of the same procedure to a smaller problem.Recursion lets us tackle complex problems by reducing the problem to a simpler one. Well, in programming, recursion is a way of doing a repetitive task by having a function call itself. A recursive function calls itself usually with a modified parameter until it reaches a specific condition. This condition is called the base case.

Sample:
def factorial(n):
    if n < 2:
        return 1
    return n * factorial (n-1)

Explanantion:
Here, we're defining a function called factorial. At the beginning of the function, we have a conditional block defining the base case, [on screen] def factorial(n): where n is smaller than 2. [on screen] if n < 2: It simply returns the value 1. [on screen] return 1 After the base case, we have a line where the factorial function is calling itself with n minus 1. [on screen] return n * factorial(n-1) This is called the recursive case. This creates a loop. Each time the function is executed, it calls itself with a smaller number until it reaches the base case. Once it reaches the base case, it returns the value 1. Then the previously called function multiplies that by two and the previously called function multiplies it by three and so on. This loop will keep going until the first factorial function called returns the desired result. It's a bit complex. Let's add a few print statements to see exactly how this works.

EX:
def factorial(n):
    print("Factorial called with" + str(n))
    if n < 2:
        print("Returning 1")
        return 1
    result = n * factorial (n-1)
    print("Returning" + str(result) + "for factorial of " + str(n))
    return result
factorial(4)

print(“Returning ” + str(result) + “ for factorial of ” + str(n)) return result So here we can see the function kept calling itself until it reached the base case. After that, each function returned the value of the previous function multiplied by n until the original function returned.

Ex:2

The function sum_positive_numbers should return the sum of all positive numbers between the number n received and 1. For example, when n is 3 it should return 1+2+3=6, and when n is 5 it should return 1+2+3+4+5=15. Fill in the gaps to make this work:

def sum_positive_numbers(n):
    # The base case is n being smaller than 1
    if n < 1:
        return ___

    # The recursive case is adding this number to 
    # the sum of the numbers smaller than this one.
    return ___ + sum_positive_numbers(___)

print(sum_positive_numbers(3)) # Should be 6
print(sum_positive_numbers(5)) # Should be 15

* EXTRA NOTES

Additional Recursion Sources
In the past videos, we visited the basic concepts of recursive functions.

A recursive function must include a recursive case and base case. The recursive case calls the function again, with a different value. The base case returns a value without calling the same function.

A recursive function will usually have this structure:

def recursive_function(parameters):
    if base_case_condition(parameters):
        return base_case_value
    recursive_function(modified_parameters)

* Recursion in Action in the IT Context:
Another IT-focused example of a recursive structure is anything that deals with groups of users that can contain other groups. We see this situation a lot when using administrative tools like active directory or LDAP. Say your group management software allows you to create groups that have both users and other groups as their members. And you want to list all human users that are part of a given group. Here you would use a recursive function to go through the groups. The base case would be a group that only includes users listing all of them. The recursive case would mean going through all the groups contained listing all the users in them and then listing any users contained in the current group.

It's important to call out that in some languages there's a maximum amount of recursive calls you can use. In Python by default, you can call a recursive function 1,000 times until you reach the limit. That's fine for things like subdirectories or user groups that aren't thousands of levels deep.


