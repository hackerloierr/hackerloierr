
Today's Topics
what is bash,
 use of bash for hackers
Output,
variables & data type
Input
comment and indentations
Arithmetic operation
if-else


What is Bash Script?
Bash = Bourne Again Shell
It is a shell, that used to interact with your kernel.
What is Script?
Script is a file that contains shell commands in a simple and clear algorithm. 
The original is sh - Bourne shell

Uses of bash
Script development
Automating tasks
Simplifying your linux ability
Developing hacking scripts.

Starting with Bash
Bash files can have “.sh” extension but you can have it without ‘.sh’ too
The file have to have executable Permissions.
You can use any text editors u need: VIM,nano,VScode,gedit,cherrytree…

Tmux can help
+

Displaying output
To start Every bash scripts use shebang.
#! /bin/bash
#! /bin/sh
To display outputs on bash you just do 
echo “YOUR TEXT HERE”
To run your project you can do:
/bin/bash hello.sh
./hello.sh   ->  need x
hello -> need x

Shebang’s used to tell the shell which interpreter is used to execute the script

Examples
If you need to add new lines on your code just add echo

Variables
Bash Variables are same with python variables, with some exceptions.
Syntax:
VARIABLE_NAME=value 
Exceptions:
NO Space between the equal sign ( = )
NAME  =  “Nathan”   => ERROR
NAME=”Nathan”  =>  Correct.
Never Start with Numbers
USE double quotes only.
To use the variable we will use dollar sign( $ )  before the Variable name
If you want to display the variable sticked with other text use ${VARIABLE_NAME}
Bash Variables are string by default. 


Cont…
The set command can be used to assign values to positional parameters.
Syntax: 
set value1 value2 value3 value4 value5

Exercise 1									10min
Display, “This is Day10,” and on new line “Introduction to Bash Scripting”
Create a Variable Called fname and lname with value of your first name and last name ,
DIsplay: “ (Your name) is firstname and your Father name is (your father name).: 
Create a Variable called Num and give it value of 10 and 
Display, “This is Day10 class”  the num 10 from the variable 

System Variables 
Are variables those are declared by the system.





There are so many: LANG, TERM,MAIL,EDITOR,USER,SHELL….
USER displays Computer owner(host)

Variables & Data Types
As we saw, the previous method they create strings only.
So to create other data types we use declare.
Arrays
Arrays are lists or tuples on python.
Syntax: 
var=(“list1” “list2” “list3” “list4)
TO display echo 
${var[0]}
To get all the elements 
${var[@]}

cont…
To get the indexes 
${!var[@]}
To get the length 
${#var[@]}
To add element to the array 
var[4]=”list5”
To remove from the array 
unset var[3]


Bash Input
On bash we have 2 methods to accept input
Read function
Arguments


Bash read 
Read used to accept inputs while the script is running.
Syntax: 
read -p “Text To Display” var
read -sp “Password: ” var  =>   used to accept hidden texts like password.
read -a var  =>   for accepting arrays(lists)

Cont…

2) Arguments
These helps to get input before the script starts
Syntax:
Just use $0-$9 while you want to work with the input

Comments
On bash the comments are
For multi line comment we start with
	<<COMMENTS
			Sfasf
			Sfa
COMMENTS     , we close with this

Bash sleep
Sleep used to make a good waiting on our script.
Syntax: 
sleep <number>s

Exercise 2                                           10 min
Create an Array of fruits with element of apple,banana,pineapple,mango
Display “I love apple banana pineapple mango”
Accept a normal username and hidden secret key input  then display The Computer Owner name.
The user after inserting username wait for 1 second.
HINT: to get computer owner name use SYSTEM variables
Accept 2 values from the user before the script start, your name and age
Display: “Your name is ____ you are ___ years old.”

Operation
To do mathematical operations you have to do $(( expression ))
  we will use let keyword for assigning variable
Arithmetic Operations
Addition $(( a + b ))
Subtraction $(( a - b ))
Multiplication $(( a * b ))
Division $(( a / b ))
Exponential $(( a ** b ))
Modulo $(( a % b ))
Assignment Operations  
Increment  “let a+= 3”
Decrement  “ let a-= 3”
Multiply “ let a*= 3  “
Divide  “ let  a/=3 “

Cont…
C)	Comparison operation
	Alphabetic comparison
Greater Than =>  -gt
Less Than => -lt
Greater than and equals to => -ge
Less than and equals too  =>  -le
Equal  =>  -eq
Not equal  => -ne
Sign comparison
>
<
>=
<=
=
!=


If else conditions
Syntax: 

If you used [ condition ]  => you will use alphabetic comparison
But for strings you can use sign too
If you used (( condition ))  => you will use numeric comparison
On bash we don't have indentation but if u finished writing the body you type “fi” 

