---
layout: post
title:      "JS and Rails Project: What I learned About Classes in Both Languages"
date:       2020-01-26 17:37:08 -0500
permalink:  studies_javascript_and_rails_project
---


I am on my fourth project at Flatiron, and I’m amazed how far I have come from my first project that I created seven months ago! The project we had to create this time was a JavaScript and Rails Single Page Application (SPA) that uses JavaScript, HTML, CSS for the frontend while Ruby on Rails for the backend.
The frontend had to communicate with the database from the backend API. Everything we learned up until this point had to come together as a giant puzzle. 
For many days before the project week, I was searching for ideas on what I should create. I watched several videos from Flatiron former students demonstrating their flashy, well-organized applications. I wanted to create something practical that I can use myself and has a purpose. While I was watching the 4-part video tutorial from Cernan Bernardo, I had an idea! Wouldn’t it be great if I actually had a place where I can log all the programming topics I’m learning for quick reference?  I can create a page that lists the programming language, topic, and a brief description about it. 
For several days I worked on creating the basis for the program. I had only one problem. It was missing the association (one to many relationship) that was part of the requirement to pass the project. After consulting with my cohort Michael, we threw some ideas together for what I could add to the program without having to redo too much and meet the deadline. Finally, the idea came to me that I could add study objectives to each study. Once I added the association, I was struggling to make my code work again. That’s where the digging and researching brought me to the understanding that I was missing the serializer. Once I added the Serializer Class that had many objectives with the rest of the attributes, my program finally worked. I’m happy I was able to make the program work. I put my best forward and will continue to press ahead learning more new things so my future projects can have additional functionalities. 

As I was working on this project, I couldn’t help but notice the major differences between JavaScript and Ruby syntaxes. Ruby language appears to be very easy on the eyes while JavaScript has many strange punctuations such as curly braces, parentheses and semicolons. 
When it comes to classes, Ruby and JavaScript share a common purpose by using classes as blueprints to create objects. They both have classes and inheritance. The syntax; however, is a little different. 


In JavaScript, we use the class keyword with the class name uppercased. Then follows the constructor() method which is automatically called when we create a new object. 
JavaScript example 

    class Dog {
      constructor (name) {
      this.name = name;
      }
    }

In Ruby, the same example would be much simpler. Notice, instead of ‘constructor’, Ruby uses ‘initialize’ as a method and uses an instance variable instead of the keyword ‘this’. 

    class Dog
	     def initialize(name)
	     @name = name
    end

To instantiate a new object in JavaScript, we use the following syntax:

     let dog = new Dog(“Trixie”);

while in Ruby it would be this way:

     trixie = Dog.new(“Trixie”)

Both JavaScript and Ruby have inheritance which is a very important part of the object-oriented programming. It is a relationship between two or more classes. Methods or functions can get copied from one class to another. In JavaScript, we use the keyword ‘extends’ to create a child class of a parent class. 

JavaScript example:

   class Cat extends Dog {
   }

In Ruby, classes can only inherit from a single other class, though. We would use the following syntax for inheritance in Ruby:

   class Cat < Dog 
   end

In JavaScript, we can also utilize the keyword super() when we call the parent class’ constructor. The child class will automatically inherit all the properties from the constructor of the parent class. 

JavaScript example:

     class Bird extends Dog {
        constructor(name)
        super(name)
     }

In Ruby, the ‘super’ keyword must be used inside of a method. When we call super, it will look for the inheritance hierarchy for a method with the same name and it will execute that method. For example:

     class Wolf
	      def howls
		       “Awoof!”
	      end
     end 

     class Dog < Wolf
	      def howls
	        super
	      end
     end

The keyword ‘super’ can also be used with the ‘initialize’ method just like with the ‘constructor’ in JavaScript. 
Although, JavaScript is mainly used as a front-end programming language whereas Ruby is used as a back-end programming language, there are many common concepts in JavaScript and Ruby. At first glance, they appear quite different, especially with the different syntax. However, they have in common many of the same object-oriented concepts. 
 

	 






