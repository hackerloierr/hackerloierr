
Topics
Functions,recursion
lambda → Map/filter
OOP & POP
Class & objects
user-built Module


Functions
A function is a block of code that performs a specific task.
Suppose, you need to create a program to create a blue circle. 
You can create two functions to solve this problem:
A function that create a circle function
A function that create a color function
Dividing a complex problem into smaller chunks makes our program easy to understand and reuse.


Types of function
There are two types of function in Python programming:

Standard library functions - These are built-in functions in Python that are available to use.
Almost all keywords are functions
print(),len(),input()....
User-defined functions - We can create our own functions based on our requirements.


Creating Functions
Syntax:							It have body like if else statements also have body.


Example: 
Functions have to be called to word. Thing functions like some skilled person, plumbers can do water pipe problems, their specific task is fixing broken pipes. So, if i need to fix my plumber what do i do?    I just call them right! |  =>  SO python functions also have to be called.

Cont…
We have 2 functions
gtst
Nathan
Both do different tasks.
We have called their name so they are on the output.

Function Arguments
They are used to take value while calling and insert it inside the function.


Cont…
The function takes fname & name as a variable for the function.

Return statement
A Python function may or may not return a value. 
If we want our function to return some value to a function call, we use the ‘return’ statement. 


Cont…
 As i told you every things are functions on python
So print() is function also input() is len(), everything
When we do                                                 we are calling the function and giving it an argument.
You can give default values too

Quiz coding.
Write a code that can replace this pow() keyword. It accepts 2 arguments a number and its power. It u do pow(4,2)  => it gives 16 , means the power.



Create A function
Accept to arguments
Do a calculation to power
Return the value
Call the function and print it.

Recursion
Recursion is process of defining something in terms of itself.
In Python, we know that a function can call other functions. It is even possible for the function to call itself. These types of construct are termed as recursive functions.

Cont…
So, This helps to call the factorial in

Advantages of Recursion
Recursive functions make the code look clean and elegant.
A complex task can be broken down into simpler sub-problems using recursion.
Sequence generation is easier with recursion than using some nested iteration.


Disadvantages of Recursion
Sometimes the logic behind recursion is hard to follow through.
Recursive calls are expensive (inefficient) as they take up a lot of memory and time.
Recursive functions are hard to debug.


Exercise 1
Create A function That accepts username and age, then display the name and the age.
BONUS: try to also display, the year which the user born
HINT: use 2023 as the year now.
Create 4 Functions add,sub,multi,div and those functions return the result of two arguments num1, num2. And accept  2 numbers user and do the calculation and display:

Anonymous / lambda Function
If function doesn’t have name it is called lambda function / Anonymous 
If you have 1 line code to return you don’t need to def a function,   
a lambda function is a special type of function without the function name.
Syntax: 
We use lambda keyword instead of def 

Function takers function
Filter, map & reduce takes a function as an argument.


Filter Function
Filters are used to filter or search some function from sequences.

Map function
Used to do some operations on Sequences

Cont…
If you want to do a doubling equations on a list of numbers.

The Append Keyword
This Keyword used to add new element to an existing list.
Syntax
mylist.append(“New Element”)

Exercise 2
Create a program that accepts 10 numbers, then filter the evens , then add 15 to them. 
DISPLAY: “Your Data: [ ….. ]”
HINT: Don’t forget to accept int() only, use loops,filter,map

Object-Oriented Programming / OOP
Python is an object oriented programming. This means mores things in python are objects.
Objects are anything which can have action and name.
Objects have attributes(properties) and methods(action or functions)
Example :  My Computer is an object because, it have..
Attribute: name,size,cpu,ram…
Behaviour: Running games, playing music, displaying texts…



Python class 
Class is simply a place where we create our Object’s attribute and behaviour 
It is like a template
a class is a blueprint for that object.
Syntax: 


After you create the Blueprint, now you can create the objects based on your class
On the above example we created Class computer and gave it an attributes of name,cpu
Conventionally Class Names Start with capital letter

Class
Creating a Class called Flower, with an attributes of the flower like petals, stem,leaf…

Creating Objects
You can Create many Objects based on 1 class.       
 Here we created 2 Objects called 
Nathan_Computer
Alemayew_Computer
Syntax:
Var = classname()
Var.attribute = “value”

CLASS
Object

Based on our flower class we can create different types of flowers in this case that is called different objects.

Lets check the type() of our object
When we check Our type it is similar with type of int, both are classes, 
‘a’  and ‘Nathan_Computer’ are objects 
computer and int are classes

Giving Behaviours == Creating Methods	
Functions are called methods on OOP
Syntax on calling
classname .method(object)
Creating a Behaviour run, which is 1 behaviour of my computer. And have parameter of ‘self’
Self is the object name on OOP you have to declare it.

Exercise 3 
Create a class of  human.
With properties of name,age,grade
With behaviour of running, dancing, eating.   Display “I can run!” “i can dance” “i can eat!”  for the behaviours
Create an Object with human1 and give the attributes of yours.
Display This:


Python Constructors 
Earlier we assigned a default value to a class attribute,
However, we can also initialize values using the constructors.
Here, __init__() is the constructor method that is called whenever a new object of that class is instantiated.
The constructor above initializes the value of the name attribute. We have used the self.name to refer to the name attribute of the bike1 object. -> it is like 2 variables 1 is from outside(name) the class and the another is from inside(self.name) the class
If we use a constructor to initialize values inside a class, we need to pass the corresponding value during the object creation of the class.

COnt…

Exercise 4
Rewrite your code with __init__ 

Python Inheritance
Is a way of creating new class with some properties of existing class.
Syntax: 
class newclass(oldclass):
…

Python Encapsulation
Encapsulation is Feature of OOP, That refers to bundling of attributes and methods inside a single class.
Encapsulation allows for better control and protection of the data, ensuring that it is accessed and modified only through specified methods.

Package installing
As we have seen package installing on our linux tutorial
We use pip to install tools so, on terminal
	pip install packagename

Package using
On python, there are a lot of packages to use them, we simply

Each packages have their own classes and methods so we have to do more studies about those packages.


From now on when you want to learn website dev with python it is just learning the package. - Django,flask,panda,numpy….
Here, we imported sys package and from that package we added the method argv, and creating an object ‘a’ 
We will see details on this when we try to create hacking tools in our future classes. DONT FORGET TO PRACTICE!!!
