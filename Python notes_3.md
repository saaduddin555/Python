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


# FORMATTING STRINGS


