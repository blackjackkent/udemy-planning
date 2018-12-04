# Object-Oriented Programming - In Plain Language

## Introduction

Hi! I'm Rosalind Wills, and welcome to my course -- Object-Oriented Programming in Plain Language. I've been working as a software developer for over ten years, specializing in Javascript, C#, and Java; I have a master's degree in software engineering and a bachelor's in English. Not only do I love programming, but I love talking about it, helping other people to understand how to get started and give life to their ideas in apps and programs.

Learning programming can sometimes seem like a daunting task. There's so many languages to choose from, so many ways to architect and structure your code, and so many tutorials out there, all assuming different levels of knowledge. In this course series, I will describe major programming concepts from the ground up, giving you a framework to build on as you dive deeper into the world of software development.

The topic for this course is object-oriented programming. So before we dive in, let's define some terms. What *is* object-oriented programming?

Object-oriented programming, or OOP, is what's known as a programming paradigm or programming model; in other words, it is a way of thinking about how to put your code together in a way that is cohesive, organized, and easily understandable. Specifically, OOP encourages structuring your code around representations of physical ideas or concepts.

Consider these two pieces of Java code. 

```java
class Main {
	public static void main(String[] args) {
		String player1Name = "John Smith";
		int player1Score = 32;
		String player2Name = "Jane Doe";
		int player2Score = 56;

		System.out.println(player1Name + " has a score of " + player1Score);
		System.out.println(player2Name + " has a score of " + player2Score);
	}
}

class Main {
	public static void main(String[] args) {
		Player player1 = new Player("John Smith", 32);
		Player player2 = new Player("Jane Doe", 56);

		System.out.println(player1.name + " has a score of " + player1.score);
		System.out.println(player2.name + " has a score of " + player2.score);
	}
}
```

You don't have to fully understand what's happening here yet, but if you look at both pieces of code, you can see that in the first one, we have a bunch of discrete text strings and numbers that exist without being connected to anything in particular. We, as the developers, know that they represent the name and score of two different players in a game, but from the compiler's perspective, they could be anything, and there's nothing in particular that associates, for instance, the player1Name and player1Score variables with each other.

In the second, however, we are representing that concept of a Player in our actual code structure. The compiler actually knows of the existence of this Player concept, and the name and score values for a particular player are connected as elements of that concept. We'll go into this in more detail later, but this is the general idea behind object-oriented programming -- we represent actual real-world objects and concepts in the way we structure our code, so that we can model how those objects and concepts interact with each other more effectively.

This is extremely useful for a lot of reasons that you will find important as you begin to work professionally in software development.

* By focusing on the objects and concepts that are important to your business or application and codifying them into your program architecture, you make it easier to keep your program's behavior in line with your business requirements and the real-world usage of your application.
* By representing an object like a Player as an instance of a reusable class, you reduce the amount of code you need to repeat and rewrite in order to represent, say, five players in a game.
* By splitting your application structure into code designed to represent different objects and concepts, you make it easier to maintain and change the behavior of part of the application without modifying the whole thing. We'll go into this in much more detail later.

So that, in a nutshell, is what object-oriented programming is all about. So how do we go about implementing it?

In the next section, I will do a quick demo of a very simple application coded in an object-oriented way. After that, we will go through and explain some of the major concepts of OOP that you might see mentioned in other discussions of the subject.

## OOP Demonstration

For a demonstration of how object-oriented programming works, we will start with the concept of...a dog.

A dog is a real-world object. It's something you can see and touch and -- most importantly for our purposes -- describe. How would you go about describing a dog?

You could describe its breed, for a start -- what type of dog it is. You could say what color it is, how old it is, what its name is, whether it is housebroken. You could even connect it to other objects in the world, such as saying which dog is its mother, or which human is its owner.

These ways of describing an object or its condition are known, in the object-oriented programming world, as properties. You've actually already encountered the idea of properties if you've worked with Java's built-in types. Ever had a string variable and checked its length?

```java
String myString = "This is a string.";
int length = myString.length;
```

In this code, length is a *property* of the string, a characteristic of the particular string, "This is a string." An object like a dog has properties as well; they're just specific to its particular type of object.

So we've thought about the ways we could describe this dog, and come up with some useful properties.

We have the breed, which will be a string like "Golden Retriever" or "Beagle". We have the name, which will be a string like "Rover". We have the color, which is also a string like "Black" or "Brown". We have the age, which is a number like 7 or 13. And we have whether or not it is housebroken -- this is a boolean value, true or false.

With this information we can represent a dog as what's called a "class" in object-oriented programming. A class is like a blueprint for how to create new objects. Here is how we might describe a Dog class based on the properties we considered:

```java
class Dog {
	String name;
	String breed;
	String color;
	int age;
	boolean isHousebroken;
}
```

This class declaration tells us exactly how any individual dog will be described. It will have a name, breed, color, age, and isHousebroken value. The first three are strings, the fourth is an integer, and the fifth is a boolean, i.e. `true` or `false`.

So now we have our blueprin
