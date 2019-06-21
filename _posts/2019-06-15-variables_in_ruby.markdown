---
layout: post
title:      "Variables in Ruby "
date:       2019-06-15 15:16:56 -0400
permalink:  variables_in_ruby
---

Variables are one of the basic steps in many programming languages including Ruby and are used to store values in particular names. 
Creating a variable, which is also called ‘declaring a variable’, is simply assigning an appropriate name to a value. Essentially, we store value in a particular name so we can reference it later. 

It is very important to give appropriate names to variables so it is easier to understand what the code is about.  
For example, if there is a field where we need to use store a zip code, it only makes sense to call the variable ‘zip_code’ and not ‘x’. 
 
To declare a variable in Ruby, we need an appropriate variable name, equal sign and data that represents the value which is assigned to the variable. 

Variables can only be lowercase strings with or without underscore but cannot be integers. They may also include certain special characters in the beginning of the variables known as ‘sigils’. Sigils are $ and @ characters. These determine the scope of the variable. 

Variables without any symbols are called local variables. This type of variables can only be accessed within the method or loop in which they were created in. They must start with lowercase or underscore.

Variables with ‘$’ are global variables can be accessed throughout the program. However, they are highly not recommended to be used. Since global variables can be accessed from any scope in the program, if incorrectly used, they may create many errors within the program.

Variables with ‘@’ symbol are instance variables that are valid in specific instances of an object. 

Variables with ‘@@’ symbols are class variables that can be valid in the entire class. 
 

It is important to understand that in Ruby unlike some other programming languages, variables function by the pass-by-value process (as opposed to pass-by-reference process). If we were to assign a value to a variable and create a new variable that references the initial variable, when we change the value of the first variable, the second variable would keep the original value. 
For example,
a = 5,  
b = a  
b = 5              ‘b’ now has the value of 5. 
However, if we change ‘a’ again to 10, ‘b’ will not become ‘10’ but it remains ‘5’ as originally set. 
a = 10
b = 5
 
This is happening in Ruby because variables are referenced to locations in memory instead of the value that is assigned to them. 

There is a lot more to cover about variables in Ruby; however, this is a good start to understand the basic function of how variables work. The most important takeaway from this is that variables must have meaningful names, cannot be integers, and they point to the location in memory instead of the value that was assigned to them. 



