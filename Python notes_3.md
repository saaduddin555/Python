# week 4

# STRINGS:
Learning Objectives:

* Manipulate strings using indexing, slicing, and formatting
* Use lists and tuples to store, reference, and manipulate data
* Leverage dictionaries to store more complex data, reference data by keys, and manipulate data stored
* Combine the String, List, and Dictionary data types to construct complex data structures

Explanantion:A string is a data type in Python that's used to represent a piece of text. It's written between quotes, either double quotes or single quotes, your choice. It doesn't matter which type of quotes you use as long as they match. If we mix up double and single quotes, Python won't be too happy, and it'll return a syntax error, telling us it couldn't find the end of the string. A string can be as short as zero characters, usually called an empty string or really long. We also learned that we can use strings to build longer strings using the plus sign and action called concatenating. A less common operation is to multiply the string by a number, which multiplies the content of the string that many times like this. If we want to know how long a string is, we can use the len function which we saw in earlier videos. The len function tells us the number of characters contained in the string. We can use strings to represent a lot of different things. They can hold a username, the name of a machine, an email address, the name of a file, and any other text. A lot of the data that we'll interact with will be stored in strings, so it's important to know how to use them. There are tons of things we could do with strings in our scripts.

For example, we can check if files are named a certain way by looking at the filename and seeing if they match our criteria, or we can create a list of emails by checking out the users of our system and concatenating our domain. I recently wrote a script that worked with a bunch of files and took different actions according to the name of each file. So the file ended in a certain extension say, .TXT , then my script would print it. If the file had a certain string and the name, say, test, then my script would ignore it and move on to the next thing and so on. The contents of a text file are also strings.


# string indexing

If we have a text that's too long to display and we want to show just a portion of it. Or if we want to make an acronym by taking the first letter of each word in a phrase. We can do that through an operation called string indexing. This operation lets us access the character in a given position or index using square brackets and the number of the position we want.

name = "Jaylen"
print(name[1])

output:
a

This might seem confusing at first, like Python is acting up. We're asking for the first character, and it's giving us the second. What gives Python? Well, what's happening here is that Python starts counting indexes from 0 not 1. Just like it does with the range function. So if we want the first character, we need to access the one at index 0. Knowing that indexes start at 0, which one do you think will be the last index in the string? It'll always be one less than the length of the string.

EX:

name = "Jaylen is not here to entertain us"
print(name[-1])


In this example, we don't know the length of the string, but it doesn't matter. Using negative indexes lets us access the positions in the string starting from the last. Nice, right?

output:
s

# Slice:
A slice is the portion of a string that can contain more than one character, also sometimes called a substring. We do that by creating a range using a colon as a separator. Let's see an example of this.

color = "Orange"
print(color[1:4])


The range we use when accessing a slice of a string works just like the one created by the range function. It includes the first number, but goes up to one less than the last number. In this case, we start with indexed one, the second letter of the string, and go up to index three, the fourth letter of the string. Another option for the range is to include only one of the two indexes. In that case, it's assumed that the other index is either 0 for the first value or the length of the string for the second value. Check this out.


color = "Orange"
print(color[1:4])


color = "Orange"
print(color[4:])

Accessing the slice from nothing to 4 takes the first four characters of the string, indexes 0 to 3. Accessing the slice from 4 to nothing takes everything from index four onward.


# EXTRA NOTES
* String Indexing and Slicing
String indexing allows you to access individual characters in a string. You can do this by using square brackets and the location, or index, of the character you want to access. It's important to remember that Python starts indexes at 0. So to access the first character in a string, you would use the index [0]. If you try to access an index that’s larger than the length of your string, you’ll get an IndexError. This is because you’re trying to access something that doesn't exist! You can also access indexes from the end of the string going towards the start of the string by using negative values. The index [-1] would access the last character of the string, and the index [-2] would access the second-to-last character.

You can also access a portion of a string, called a slice or a substring. This allows you to access multiple characters of a string. You can do this by creating a range, using a colon as a separator between the start and end of the range, like [2:5]. 

This range is similar to the range() function we saw previously. It includes the first number, but goes to one less than the last number. For example:

>>> fruit = "Mangosteen"
>>> fruit[1:4]
'ang'

The slice includes the character at index 1, and excludes the character at index 4. You can also easily reference a substring at the start or end of the string by only specifying one end of the range. For example, only giving the end of the range:

>>> fruit[:5]
'Mango'

This gave us the characters from the start of the string through index 4, excluding index 5. On the other hand this example gives is the characters including index 5, through the end of the string:

>>> fruit[5:]
'steen'

You might have noticed that if you put both of those results together, you get the original string back!

>>> fruit[:5] + fruit[5:]
'Mangosteen'

Cool!


# CREATING A NEW STRING

Imagine you have a string with a character that's wrong and you want to fix it, like this one. Taking into account what you learned about string indexing, you might be tempted to fix it by accessing the corresponding index and changing the character. Let's see what happens if we try that.

message = "A Kong string with a silly typo"
printmessage[2] = "l"

These pesky type errors, right? In this case, we're told that strings don't support item assignment. This means that we can't change individual characters because strings in Python are immutable, which is just a fancy word meaning they can't be modified. What we can do is create a new string based on the old one, like this.

message = "A Kong string with a silly typo"
new_message = message[0:2] + "l" + message[3:]
print(new_message)

Nice, we fixed the typo. But does this mean the message variable can never change? Not really. We can assign a new value to the same variable. Let's do that a couple of times to see how it works.

message = "A Kong string with a silly typo"
new_message = message[0:2] + "l" + message[3:]
print(new_message)
message = "this a new message"
print(message)

What we're doing here, is giving the message variable a whole new value. We're not changing the underlying string that was assigned to it before. We're assigning a whole new string with different content. If this seems a bit complex, that's okay. You don't need to worry about this right now. We'll call this out whenever it's relevant for the programmer writing. So, we figured out how to create a new message from the old one.lets try

pets = "cats & dogs"
print(pets.index("&"))



In this case, we're using a method to get the index of a certain character.So the index method returns the index of the given substring, inside the string. The substring that we pass, can be as long or as short as we want. What if there's more than one of the substring?

pets = "cats & dogs"
print(pets.index("s"))

Here, we know there are two s characters, but we only get one value. That's because the index method returns just the first position that matches. And what happens if the string doesn't have the substring we're looking for? The index method can't return a number because the substring isn't there, so we get a value error instead.

* Method
A method is a function associated with a specific class. We'll talk a lot more about classes and methods later. For now, what you need to know is that this is a function that applies to a variable. And we can call it by following the variable with a dot.

EX:
Using the index method, find out the position of "x" in "supercalifragilisticexpialidocious".

word = "supercalifragilisticexpialidocious"
print(word.index("x"))

----

We said that if the substring isn't there, we would get an error. So how can we know if a substring is contained in a string to avoid the error? Let's check this out.

pets = "cats & dogs"
print("dragons" in pets)

output:
false

pets = "cats & dogs"
print("cats" in pets)

output:
true

We can use the key word in to check if a substring is contained in a string. We came across the keyword in, when using four loops. In that case, it was used for iteration. Here, it's a conditional that can be either true or false. It'll be true if the substring is part of the string, and false if it's not. So here, the Dragons substring isn't part of the string, and sadly, we can't have a Dragon as a pet. 


EX:
def replace_domain(email, old_domain,new_domain):       #
    if "@" + old_domain in email:                       #
      index = email.index("@" + old_domain)             #
      new_email = email[:index] + "@" + new_domain      #
    return new_email                                    #
replace_domain('theboss@gmail' , 'gmail' ,'fmail')      #

In the first line of the body of the function, we check if the concatenation of the @ sign and the old domain are contained in the email address, using the keyword in. We check this to make sure the email has "old domain" on the portion that comes after the @ sign. If the condition is true, the email address needs to be updated. To do that, we first find out the index where the old domain, including the @ sign starts. We know that this index will be a valid number because we've already checked that the substring was present. So, using this index, we create the new email. This is a string that contains the first portion of the old email, up until the index we had calculated, followed by the @ sign and the new domain. Finally, we return this new email. If the email didn't contain the new domain, then we can just return it, which is what we do in the last line.

# EXTRA NOTES

* Basic String Methods
In Python, strings are immutable. This means that they can't be modified. So if we wanted to fix a typo in a string, we can't simply modify the wrong character. We would have to create a new string with the typo corrected. We can also assign a new value to the variable holding our string.

If we aren't sure what the index of our typo is, we can use the string method index to locate it and return the index. Let's imagine we have the string "lions tigers and bears" in the variable animals. We can locate the index that contains the letter g using animals.index("g"), which will return the index; in this case 8. We can also use substrings to locate the index where the substring begins. animals.index("bears") would return 17, since that’s the start of the substring. If there’s more than one match for a substring, the index method will return the first match. If we try to locate a substring that doesn't exist in the string, we’ll receive a ValueError explaining that the substring was not found.

We can avoid a ValueError by first checking if the substring exists in the string. This can be done using the in keyword. We saw this keyword earlier when we covered for loops. In this case, it's a conditional that will be either True or False. If the substring is found in the string, it will be True. If the substring is not found in the string, it will be False. Using our previous variable animals, we can do "horses" in animals to check if the substring "horses" is found in our variable. In this case, it would evaluate to False, since horses aren’t included in our example string. If we did "tigers" in animals, we'd get True, since this substring is contained in our string.

# DIFFERENT TYPES OF STRING METHODS:

we've seen ways you can access portions of strings using the indexing technique, create new strings by slicing and concatenating, find characters and strings using the index method, and even test if one string contains another. On top of all this string processing power, the string class provides a bunch of other methods for working with text. Now, we'll show you how to use some of these methods.

* Upper & lower class:

answer = 'yes'
if answer.lower() =="yes":
    print("user said yes")

output:
used said yes

Some string methods let you perform transformations or formatting on the string text, like upper, and its opposite, lower. These methods are really useful when you're handling user input. Let's say you wanted to check if the user answered yes to a question. How would you know if the user typed it using upper or lower case? You don't need to, you just transform the answer to the case you want.

* strip method:

" yes " .strip()

output:
'yes'

" yes " .lstrip()

output:
'yes '

" yes " .rstrip()

output:
' yes'

Another useful method when dealing with user input is the strip method. This method will get rid of surrounding spaces in the string. If we ask the user for an answer, we usually don't care about any surrounding spaces. So it's a good idea to use the strip method to get rid of any white space. This means that strip doesn't just remove spaces, it also removes tabs and new line characters, which are all characters we don't usually want in user-provided strings. There are two more versions of this method, lstrip rstrip, to get rid of the whitespace characters just to the left or to the right of the string instead of both sides.

* count of substring inside a string:

"the number of times e occurs in this string is 4".count("e")

output:
4

The method count returns how many times a given substring appears within a string.

* endswith string:

"forest".endswith("rest")

output:
true

The method endswith returns whether the string ends with a certain substring.

* isnumeric:

"forest".isnumeric()

output:
false

"12345".isnumeric()

output:
true

The method isnumeric returns whether the string's made up of just numbers. Adding to that, if we have a string that is numeric, we can use the int function to convert it to an actual number.like this

int("12345) + int("54321")

output:

66666

* join method:

" ".join(["this","is","a","phrase","joined","by","spaces"])

output:
this is a phrase joined by spaces

"...".join(["this","is","a","phrase","joined","by","dots"])

output:
this...is...a...phrase...joined...by...dots

To use the join method, we have to call it on the string that'll be used for joining. In this case, we're using a string with a space in it. The method receives a list of strings and returns one string with each of the strings joined by the initial string. Let's check out another example.

* split method:

"this is another example".split()

output:
['this','is','another','example']

The split method returns a list of all the words in the initial string and it automatically splits by any whitespace. It can optionally take a parameter and split the strings by another character, like a comma or a dot.

# EXTRA NOTES

* Advanced String Methods:

Advanced String Methods
We've covered a bunch of String class methods already, so let's keep building on those and run down some more advanced methods.

The string method lower will return the string with all characters changed to lowercase. The inverse of this is the upper method, which will return the string all in uppercase. Just like with previous methods, we call these on a string using dot notation, like "this is a string".upper(). This would return the string "THIS IS A STRING". This can be super handy when checking user input, since someone might type in all lowercase, all uppercase, or even a mixture of cases.

You can use the strip method to remove surrounding whitespace from a string. Whitespace includes spaces, tabs, and newline characters. You can also use the methods  lstrip and rstrip to remove whitespace only from the left or the right side of the string, respectively.

The method count can be used to return the number of times a substring appears in a string. This can be handy for finding out how many characters appear in a string, or counting the number of times a certain word appears in a sentence or paragraph.

If you wanted to check if a string ends with a given substring, you can use the method endswith. This will return True if the substring is found at the end of the string, and False if not.

The isnumeric method can check if a string is composed of only numbers. If the string contains only numbers, this method will return True. We can use this to check if a string contains numbers before passing the string to the int() function to convert it to an integer, avoiding an error. Useful!

We took a look at string concatenation using the plus sign, earlier. We can also use the join method to concatenate strings. This method is called on a string that will be used to join a list of strings. The method takes a list of strings to be joined as a parameter, and returns a new string composed of each of the strings from our list joined using the initial string. For example, " ".join(["This","is","a","sentence"]) would return the string "This is a sentence".

The inverse of the join method is the split method. This allows us to split a string into a list of strings. By default, it splits by any whitespace characters. You can also split by any other characters by passing a parameter.


* Formatting Strings:





Modify the student_grade function using the format method, so that it returns the phrase "X received Y% on the exam". For example, student_grade("Reed", 80) should return "Reed received 80% on the exam".

def student_grade(name, grade):
	return ""

print(student_grade("Reed", 80))
print(student_grade("Paige", 92))
print(student_grade("Jesse", 85))







* String Formatting:
You can use the format method on strings to concatenate and format strings in all kinds of powerful ways. To do this, create a string containing curly brackets, {}, as a placeholder, to be replaced. Then call the format method on the string using .format() and pass variables as parameters. The variables passed to the method will then be used to replace the curly bracket placeholders. This method automatically handles any conversion between data types for us. 

If the curly brackets are empty, they’ll be populated with the variables passed in the order in which they're passed. However, you can put certain expressions inside the curly brackets to do even more powerful string formatting operations. You can put the name of a variable into the curly brackets, then use the names in the parameters. This allows for more easily readable code, and for more flexibility with the order of variables.

You can also put a formatting expression inside the curly brackets, which lets you alter the way the string is formatted. For example, the formatting expression {:.2f} means that you’d format this as a float number, with two digits after the decimal dot. The colon acts as a separator from the field name, if you had specified one. You can also specify text alignment using the greater than operator: >. For example, the expression {:>3.2f} would align the text three spaces to the right, as well as specify a float number with two decimal places. String formatting can be very handy for outputting easy-to-read textual output.


* String Reference Guide:

In Python, there are a lot of things you can do with strings. In this guide, you’ll find the most common string operations and string methods.

String operations
len(string) - Returns the length of the string

for character in string - Iterates over each character in the string

if substring in string - Checks whether the substring is part of the string

string[i] - Accesses the character at index i of the string, starting at zero

string[i:j] - Accesses the substring starting at index i, ending at index j minus 1. If i is omitted, its value defaults to 0. If j is omitted, the value will default to len(string).



String methods
string.lower() - Returns a copy of the string with all lowercase characters

string.upper() - Returns a copy of the string with all uppercase characters

string.lstrip() - Returns a copy of the string with the left-side whitespace removed

string.rstrip() - Returns a copy of the string with the right-side whitespace removed

string.strip() - Returns a copy of the string with both the left and right-side whitespace removed

string.count(substring) - Returns the number of times substring is present in the string

string.isnumeric() - Returns True if there are only numeric characters in the string. If not, returns False.

string.isalpha() - Returns True if there are only alphabetic characters in the string. If not, returns False.

string.split() - Returns a list of substrings that were separated by whitespace (whitespace can be a space, tab, or new line)

string.split(delimiter) - Returns a list of substrings that were separated by whitespace or a delimiter

string.replace(old, new) - Returns a new string where all occurrences of old have been replaced by new.

delimiter.join(list of strings) - Returns a new string with all the strings joined by the delimiter 

Check out the official documentation for all available String methods.  https://docs.python.org/3/library/stdtypes.html#string-methods


* Formatting Strings Guide:

Python offers different ways to format strings. In the video, we explained the format() method. In this reading, we'll highlight three different ways of formatting strings. For this course you only need to know the format() method. But on the internet, you might find any of the three, so it's a good idea to know that the others exist.

Using the format() method
The format method returns a copy of the string where the {} placeholders have been replaced with the values of the variables. These variables are converted to strings if they weren't strings already. Empty placeholders are replaced by the variables passed to format in the same order.


# "base string with {} placeholders".format(variables)

example = "format() method"

formatted_string = "this is an example of using the {} on a string".format(example)

print(formatted_string)

"""Outputs:
this is an example of using the format() method on a string
"""

* If the placeholders indicate a number, they’re replaced by the variable corresponding to that order (starting at zero).

# "{0} {1}".format(first, second)

first = "apple"
second = "banana"
third = "carrot"

formatted_string = "{0} {2} {1}".format(first, second, third)

print(formatted_string)

"""Outputs:
apple carrot banana
"""

* If the placeholders indicate a field name, they’re replaced by the variable corresponding to that field name. This means that parameters to format need to be passed indicating the field name.

# "{var1} {var2}".format(var1=value1, var2=value2)


"{:exp1} {:exp2}".format(value1, value2)



* If the placeholders include a colon, what comes after the colon is a formatting expression. See below for the expression reference.

Official documentation for the format string syntax

# {:d} integer value
'{:d}'.format(10.5) → '10'


Formatting expressions

Expr                    Meaning                                                           Example

{:d}                    integer value                                               '{:d}'.format(10.5) → '10'

{:.2f}                  floating point with that many decimals                      '{:.2f}'.format(0.5) → '0.50'

{:.2s}                  string with that many characters                             '{:.2s}'.format('Python') → 'Py'

{:<6s}                  string aligned to the left that many spaces                 '{:<6s}'.format('Py') → 'Py    '

{:>6s}                  string aligned to the right that many spaces                '{:>6s}'.format('Py') → '    Py'

{:^6s}                  string centered in that many spaces                         '{:^6s}'.format('Py') → '  Py  '


 Check out the official documentation for all available expressions.

https://docs.python.org/3/library/string.html#format-specification-mini-language


Old string formatting (Optional)
The format() method was introduced in Python 2.6. Before that, the % (modulo) operator could be used to get a similar result. While this method is no longer recommended for new code, you might come across it in someone else's code. This is what it looks like:

 "base string with %s placeholder" % variable

The % (modulo) operator returns a copy of the string where the placeholders indicated by %  followed by a formatting expression are replaced by the variables after the operator.


 "base string with %d and %d placeholders" % (value1, value2)

To replace more than one value, the values need to be written between parentheses. The formatting expression needs to match the value type.

 

"%(var1) %(var2)" % {var1:value1, var2:value2}

Variables can be replaced by name using a dictionary syntax (we’ll learn about dictionaries in an upcoming video).

 

"Item: %s - Amount: %d - Price: %.2f" % (item, amount, price)

The formatting expressions are mostly the same as those of the format() method. 

Check out the official documentation for old string formatting.

Formatted string literals (Optional)
This feature was added in Python 3.6 and isn’t used a lot yet. Again, it's included here in case you run into it in the future, but it's not needed for this or any upcoming courses.

A formatted string literal or f-string is a string that starts with 'f' or 'F' before the quotes. These strings might contain {} placeholders using expressions like the ones used for format method strings.

The important difference with the format method is that it takes the value of the variables from the current context, instead of taking the values from parameters.

 Examples:

>>> name = "Micah"

>>> print(f'Hello {name}')

Hello Micah

 

>>> item = "Purple Cup"

>>> amount = 5

>>> price = amount * 3.25

>>> print(f'Item: {item} - Amount: {amount} - Price: {price:.2f}')

Item: Purple Cup - Amount: 5 - Price: 16.25

 Check out the official documentation for f-strings. https://docs.python.org/3/reference/lexical_analysis.html#f-strings
----


Study Guide: Strings

This study guide provides a quick-reference summary of what you learned in this lesson and serves as a guide for the upcoming practice quiz. The string readings in this section are great syntax guides to help you on the Strings Practice Quiz.

In the Strings segment, you learned about the parts of a string, string indexing and slicing, creating new strings, string methods and operations, and formatting strings. 


Knowledge

String Operations and Methods

    * .format() - String method that can be used to concatenate and format strings. 

            * {:.2f} - Within the .format() method, limits a floating point variable to 2 decimal places. The number of decimal places can be customized.

* len(string) - String operation that returns the length of the string.

* string[x] - String operation that accesses the character at index [x] of the string, where indexing starts at zero.

* string[x:y] - String operation that accesses a substring starting at index [x] and ending at index [y-1]. If x is omitted, its value defaults to 0. If y is omitted, the value will default to len(string).

* string.replace(old, new) - String method that returns a new string where all occurrences of an old substring have been replaced by a new substring.

* string.lower() - String method that returns a copy of the string with all lowercase characters.


Coding skills:

Skill Group 1:
. Use a for loop to iterate through each letter of a string.

. Add a character to the front of a string.

. Add a character to the end of a string.

. Use the .lower() string method to convert the case (uppercase/lowercase) of the letters within a string variable. This method is often used to eliminate cases as a factor when comparing two strings. For example, all lowercase “cat” is not equal to “Cat” because “Cat” contains an uppercase letter. To be able to compare the two strings to see if they are the same word, you can use the .lower() string method to remove capitalization as a factor in the string comparison.


# This function accepts a given string and checks each character of 
# the string to see if it is a letter or not. If the character is a
# letter, that letter is added to the end of the string variable
# "forwards" and to the beginning of the string variable "backwards".
def mirrored_string(my_string):

    # Two variables are initialized as string data types using empty 
    # quotes. The variable "forwards" will hold the "my_string"
    # minus any character that is not a letter. The "backwards" 
    # variable will hold the same letters as "forwards", but in  
    # in reverse order.
    forwards = ""
    backwards = ""

    # The for loop iterates through each character of the "my_string"
    for character in my_string:

        # The if-statement checks if the character is not a space.
        if character.isalpha():

            # If True, the body of the loop adds the character to the
            # to the end of "forwards" and to the front of
            # "backwards". 
            forwards += character
            backwards = character + backwards

        # If False (meaning the character is not a letter), no action
        # is needed. This coding approach results prevents any 
        # non-alphabetical characters from being written to the
        # "forwards" and "backwards" variables. The for loop will 
        # restart until all characters in "my_string" have been
        # processed.
        
    # The final if-statement compares the "forwards" and "backwards"
    # strings to see if the letters are the same both forwards and
    # backwards. Since Python is case sensitive, the two strings will 
    # need to be converted to use the same case for this comparison. 
    if forwards.lower() == backwards.lower():
        return True
    return False
 
print(mirrored_string("12 Noon")) # Should be True
print(mirrored_string("Was it a car or cat I saw")) # Should be False
print(mirrored_string("'eve, Madam Eve")) # Should be True


Skill Group 2:

. Use the format() method, with {} placeholders for variable data, to create a new string.

. Use a formatting expression, like {:.2f}, to format a float variable and configure the number of decimal places to display for the float. 

# This function converts measurement equivalents. Output is formatted 
# as, "x ounces equals y pounds", with y limited to 2 decimal places. 
def convert_weight(ounces):

    # Conversion formula: 1 pound = 16 ounces
    pounds = ounces/16 
    
    # The result is composed using the .format() method. There are two
    # placeholders in the string: the first is for the "ounces" 
    # variable and the second is for the "pounds" variable. The second
    # placeholder formats the float result of the conversion 
    # calculation to be limited to 2 decimal places.
    result = "{} ounces equals {:.2f} pounds".format(ounces,pounds)
    return result


print(convert_weight(12)) # Should be: 12 ounces equals 0.75 pounds
print(convert_weight(50.5)) # Should be: 50.5 ounces equals 3.16 pounds
print(convert_weight(16)) # Should be: 16 ounces equals 1.00 pounds


 Skill Group 3  

. Within the format() parameters, select characters at specific index [ ] positions from a variable string.  

. Use the format() method, with {} placeholders for variable data, to create a new string.

# This function generates a username using the first 3 letters of a
# user’s last name plus their birth year. 
def username(last_name, birth_year):
    
    # The .format() method will use the first 3 letters at index 
    # positions [0,1,2] of the "last_name" variable for the first
    # {} placeholder. The second {} placeholder concatenates the user’s
    #  "birth_year" to that string to form a new string username.
    return("{}{}".format(last_name[0:3],birth_year))


print(username("Ivanov", "1985")) 
# Should display "Iva1985" 
print(username("Rodríguez", "2000")) 
# Should display "Rod2000" 
print(username("Deng", "1991")) 
# Should display "Den1991"



Skill Group 4:

. Use the .replace() method to replace part of a string.  

. Use the len() function to get the number of index positions in a string.

. Slice a string at a specific index position.



# This function checks a given schedule entry for an old date and, if 
# found, the function replaces it with a new date. 
def replace_date(schedule, old_date, new_date):

    # Check if the given "old_date" appears at the end of the given 
    # string variable "schedule". 
    if schedule.endswith(old_date):

        # If True, the body of the if-block will run. The variable "n" is
        # used to hold the slicing index position. The len() function
        # is used to measure the length of the string "new_date".
        p = len(old_date)

        # The "new_schedule" string holds the updated string with the 
        # old date replaced by the new date. The schedule[:-p] part of 
        # the code trims the "old_date" substring from "schedule" 
        # starting at the final index position (or right-side) counting
        # towards the left the same number of index positions as 
        # calculated from len(old_date). Then, the code schedule[-p:]
        # starts the indexing position at the slot where the first
        # character of the "old_date" used to be positioned. The 
        # .replace(old_date, new_date) code inserts the "new_date" into
        # the position where the "old_date" used to exist.  
        new_schedule = schedule[:-p] + schedule[-p:].replace(old_date, new_date)

        # Returns the schedule with the new date.
        return new_schedule
        
    # If the schedule does not end with the old date, then return the
    # original sentence without any modifications.
    return schedule
 
 
print(replace_date("Last year’s annual report will be released in March 2023", "2023", "2024")) 
# Should display "Last year’s annual report will be released in March 2024"
print(replace_date("In April, the CEO will hold a conference", "April", "May")) 
# Should display "In April, the CEO will hold a conference"
print(replace_date("The convention is scheduled for October", "October", "June")) 
# Should display "The convention is scheduled for June"


Practice Quiz: 

Question 1
Fill in the blanks to complete the is_palindrome function. This function checks if a given string is a palindrome. A palindrome is a string that contains the same letters in the same order, whether the word is read from left to right or right to left. Examples of palindromes are words like kayak and radar, and phrases like "Never Odd or Even". The function should ignore blank spaces and capitalization when checking if the given string is a palindrome. Complete this function to return True if the passed string is a palindrome, False if not. 

def is_palindrome(input_string):
    # Two variables are initialized as string date types using empty 
    # quotes: "reverse_string" to hold the "input_string" in reverse
    # order and "new_string" to hold the "input_string" minus the 
    # spaces between words, if any are found.
    new_string = ""
    reverse_string = ""

    # Complete the for loop to iterate through each letter of the
    # "input_string"
    for ___:

        # The if-statement checks if the "letter" is not a space.
        if letter != " ":

            # If True, add the "letter" to the end of "new_string" and
            # to the front of "reverse_string". If False (if a space
            # is detected), no action is needed. Exit the if-block.
            new_string = ___
            reverse_string = ___

    # Complete the if-statement to compare the "new_string" to the
    # "reverse_string". Remember that Python is case-sensitive when
    # creating the string comparison code. 
    if ___:

        # If True, the "input_string" contains a palindrome.
        return True
		
    # Otherwise, return False.
    return False


print(is_palindrome("Never Odd or Even")) # Should be True
print(is_palindrome("abc")) # Should be False
print(is_palindrome("kayak")) # Should be True


q:

Using the format method, fill in the gaps in the convert_distance function so that it returns the phrase "X miles equals Y km", with Y having only 1 decimal place. For example, convert_distance(12) should return "12 miles equals 19.2 km".

def convert_distance(miles):
    km = miles * 1.6 
    result = "{} miles equals {___} km".___
    return result


print(convert_distance(12)) # Should be: 12 miles equals 19.2 km
print(convert_distance(5.5)) # Should be: 5.5 miles equals 8.8 km
print(convert_distance(11)) # Should be: 11 miles equals 17.6 km


q:

If we have a string variable named Weather = "Rainfall", which of the following will print the substring "Rain" or all characters before the "f"?


print(Weather[:4])


print(Weather[4:])


print(Weather[1:4])


print(Weather[:"f"])


q:

Question 4
Fill in the gaps in the nametag function so that it uses the format method to return first_name and the first initial of last_name followed by a period. For example, nametag("Jane", "Smith") should return "Jane S."

def nametag(first_name, last_name):
    return("___.".format(___))


print(nametag("Jane", "Smith")) 
# Should display "Jane S." 
print(nametag("Francesco", "Rinaldi")) 
# Should display "Francesco R." 
print(nametag("Jean-Luc", "Grand-Pierre")) 
# Should display "Jean-Luc G." 


q:

The replace_ending function replaces a specified substring at the end of a given sentence with a new substring. If the specified substring does not appear at the end of the given sentence, no action is performed and the original sentence is returned. If there is more than one occurrence of the specified substring in the sentence, only the substring at the end of the sentence is replaced. For example, replace_ending("abcabc", "abc", "xyz") should return abcxyz, not xyzxyz or xyzabc. The string comparison is case-sensitive, so replace_ending("abcabc", "ABC", "xyz") should return abcabc (no changes made).  


def replace_ending(sentence, old, new):
    # Check if the old substring is at the end of the sentence 
    if ___:
        # Using i as the slicing index, combine the part
        # of the sentence up to the matched string at the 
        # end with the new string
        i = ___
        new_sentence = ___
        return new_sentence


    # Return the original sentence if there is no match 
    return sentence
    
print(replace_ending("It's raining cats and cats", "cats", "dogs")) 
# Should display "It's raining cats and dogs"
print(replace_ending("She sells seashells by the seashore", "seashells", "donuts")) 
# Should display "She sells seashells by the seashore"
print(replace_ending("The weather is nice in May", "may", "april")) 
# Should display "The weather is nice in May"
print(replace_ending("The weather is nice in May", "May", "April")) 
# Should display "The weather is nice in April"
