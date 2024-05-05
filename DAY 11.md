
Regular expressions
Else if
loops
functions
bash and linux shell
Today’s Topics

Regular Expressions! /regex/
How do this site know that our input is not email?

Cont…
Most filter Validation on any platform done by Regular expression/regex/.
They are patterns that helps to filter so texts,space,tabs & symbols.
Like telegram or other platforms filtering links inside group, filtering some bad words.. All are regex.
Regex is PATTERN!
Regex are used on linux tools called grep,awk and sed


regex…
To demonstrate this we can simply use vscode search tool.
And don’t forget to turn the regex button on


regex…
The pattern is same but the implementation may differ on programming languages.
On Python,

Quick Test!
What do u think the output of this
SO, \n is a pattern, it is called metacharacter

Metacharacters 
Those are regex pattern symbols for filter.
They are :
 .
^
$
*
+
?
{ } 
[ ] 
( )
|
\

Dot ( . )
Used to get All the line except new lines
Syntax:   .
This means give me all lines except the new lines

Caret ( ^ )   -  Assertion 
Used to get line that start with pattern
Syntax:   ^hello
This means lines that start with hello

Dollar sign( $ )  -  Assertion  
Used to get line that ends with some pattern.
Syntax: hello$
That ends with hello

Plus ( + )  -  Quantity  
Used to get line that have pattern that occurs 1 and more times.
Syntax: hellos+
A text hello that have s at least 1 times and more.

Asteriks ( * )  -  Quantity  
Used to get line that have pattern that occurs 0 and more times.
Syntax: hellos*
A text hello that have s at least 0 times and more.

Question mark ( ? )  -  Quantity  
Used to get line that have pattern that occurs 0 and 1 times.
Syntax: hellos?
A text hello that have s at least 0 time or 1 time.

What if…
We need to get texts that starts with n and ends with com including all the texts between those 2 expressions…  
STart with n = ^n
End with com = com$
All Test between them = .* , .+

We can do it in 1 line
^n.*com$ 

Curly Bracket ( { min , max} ) - Quantity

Used to get line that have pattern that occurs min and max times.it is custom
Syntax: hellos{1,3}
A text hello that have s at least 0 times and more.
{1,} = plus sign
{0,} = asterisk
{0,1} = what..

What if…
We need to get texts that starts with n and ends with com including the texts that have 7-13 character between those 2 expressions…  
STart with n = ^n
End with com = com$
7-10 character = .{7,13}

We can do it in 1 line
^n.{7,13}com$ 

 \w   
Used to get Alphanumeric 
Syntax: \w
All texts except newlines and symbols

 \W   
Used to get All except Alphanumeric 
Syntax: \W
All texts except newlines and symbols

 \s   
Used to get whitespace.
Syntax: \s
All spaces and tabs

 \S   
Used to get all except whitespace.
Syntax: \S
All spaces and tabs

 \d   
Used to get Digits/numbers/
Syntax: \d
All spaces and tabs

 \D   
Used to get all except Digits/numbers/
Syntax: \D
All spaces and tabs

Pipe ( | )  -   OR
Used to search 2 different things.
Syntax:  a|b

Cont…

Escape ( \ ) 
Used to search symbols that are metacharacters.
Syntax:  \sign

Square Brackets ( [ ] )  - Custom pattern
Used to Create your own patterns
Syntax: [pattern]

You cant get small letters with the \w or built in patterns.

Cont…
You can add other patterns in same [ ] with no space between them.



Exercise 1								10min
Demlachewu is A software engineer and wanted to make a telegram bot that can delete links like https and ends with .com from the group, can u help him by writing the regex?
Write a Regex That Filters the emails only from the following list
john@gmail.com
natanhailu@yahoo.com
micky43@geeztecg.net
rexder@gmail.com
Hello there this is me
My phone number 0987654321


Bash regex
You can use it on awk, sed, but for today i will show you using grep.

On bash terminal these metacharacters have meaning so, we have to escape them by adding ‘\’ infront of the metacharacters

BASH FOR REGEX
We use =~ operator for regex check with if condition statements
Here we use double Brackets for our conditional Statemens.
SYNTAX:


Task																										10min 
Write A bash code that can accept emails from user name and check if it is Valid email or not, using regex

Bash else if
To do more than 1 comparing.
It is same with python is is “elif”
Syntax: 


Loops
On Bash, there are 3 types of loops
For loop
While loop
Until loop

For loops
The iteration may be different here. We can use arrays like list on python but we dont have range in bash but we can do {a..b}  this iterates from a to b
Syntax:

Cont…
Works with words in strings too.

For loop without sequence data
On bash
i++ = i +=1
i- - = i -= 1           

For Loop with increment/decrement
Same syntax with index slicing but here it is for looping.  -  {start..stop..step}

While loop
You do ((count++))

Infinite loop

Break Statement 

…Output

Continue Statement
Is A function that helps to break the loop there and start if from the up again. - its python equivalent is called ‘pass’

Exercise 2
Create a loop that prints your name 10 times
Accept 2 input from user 1 his name and 2 amount of repeat he needs and display it for the size he wanted to repeat. 
Create a infinite loop that displays, “You are BASH MASTER!!!”

Until loop
It is same but this one exits the loop when the expression is true.
The name until means እስከ

Function

Cont…
When you have function and the arguments will be $1, $2 ….
If we use $? it will call the return value.

Exercise 3
Write a code that can replace this pow() keyword. It accepts 2 arguments a number and its power. It u do pow(4,2)  => it gives 16 , means the power.



Create A function
Accept to arguments
Do a calculation to power
Return the value
Call the function and print it.


BASH and Linux
We can run linux commands inside our bash

Cont…
You can run bash codes in 1 line.

Cont…
You can access files in current directory using * sign

Interaction with linux
You can interact with linux terminal using bash.
For this our codes are bash so, your terminal have to be on bash
Command: /bin/bash

For loop on terminal
Syntax: 

