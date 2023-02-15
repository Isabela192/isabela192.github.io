---
title: "Programming Paradigms"
date: 2023-02-14
categories:
  - tech
tags:
  - Programming
---

❤️ *HAPPY VALENTINE'S DAY* ❤️

I first started to write code in college. And no, I didn't like it one bit.
My first programming language was **C++** and passing that class felt like a miracle.
Did that class make me like programming? No.

Was I obligated to learn how to program to proceed with my degree? Yes.
And here is where Python and R showed up. First, I only used R to analyze some weather data. Then I started to learn Python to make some nice plots for my articles.
Fast forward to the future to me working with Python full-time.
The thing is, I never really learned how to code as a developer. I learned how to code as someone trying to apply a tool to a problem.
now that I work with Python feels important to know what Python **is**.

So I went and learned that Python is an *object-oriented* programming language. Which means?... And if Python is an OOP, what is C? Are there more types of classification?

So, since I'm alone this Valentines' I decided to research a little on *Programming Paradigms* 💔.

> :warning: **I'm not a specialist** If you find something wrong, please let me know :)

Ok, first things first: what is a programming paradigm? 
Well, a *paradigm* is a set of ideas or patterns that define a particular subject. When we apply this concept to computers, we have broad ways of writing code.
There are a **LOT** of different paradigms. Essentially, we have five major ones:

### The procedural paradigm

Can be called imperative paradigm. Consists of writing code as a sequence of tasks executed from top to bottom. Each task is followed by another one and may contain loops, conditional statements, and subroutines that control the flow of execution. 
Examples of this are [C](https://en.wikipedia.org/wiki/C_(programming_language)), [Python](https://en.wikipedia.org/wiki/Python_(programming_language)), and [Fortran](https://en.wikipedia.org/wiki/Fortran). (Even if you may write the functions for a Fortran routine at the end of the main code, the compile process will pre-compile those and call these functions when needed, like decorators in Python).

- As you may have noticed, this is one of the earliest types of programming that exists, and it sticks around since:
- They are portable;
- Simple to code and implement;
- You can apply DRY since you can define a function and reuse it throughout the code
Since it is a top-down approach, you can easily follow the flow and track bugs.

A simple Fortran program would be like:

````fortran
program hello
  print *, 'Hello, World!'
end program hello
````

### Logical Programming

As the name suggests, it is based on logic. It deals with symbols and relationships between them. [Prolog](https://en.wikipedia.org/wiki/Prolog) and [SQl](https://en.wikipedia.org/wiki/SQL) are good examples of this paradigm.

- The main takeaways from this type of paradigm are;
- The code gets more flexible since it depends on the logic, not the order; 
- This makes the program easier to understand since it follows logical thinking.

In SQL a query would express all the logic to fetch data from a DB.

`````SQl
SELECT * 
FROM TABLE
WHERE CONDITION IN (VALUES);
`````

### Functional Programming

It is the use of functions to build a program. What does this mean? 
The program consists of *pure functions*. You input the arguments list, and the function returns a value. Simple? Well...
The thing is, in functional programming, the data is immutable. So, unlike Python, where you may have a global variable being used in a function, this does not occur here. This is like the anti-OOP since states can't be shared.

That means that the return of the function is dependent on the input. BTW, this is one of the main takeaways from Functional Programming.
The other ones are:
- Recursion: the function can call itself during its execution. This allows the  repetition of the process several times, ending with the output;
- Variables are immutable, so you can't modify them after the code started;
- [Lisp](https://en.wikipedia.org/wiki/Lisp_(programming_language)) is an example of this paradigm and is very popular in the artificial intelligence field.

A very elegant way to say `Hello World`in Lisp:

````Lisp
(format t "Hello, World!")
````

[C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)), [JavaScript](https://en.wikipedia.org/wiki/JavaScript), and Python can be considered Functional Programming languages, just not *pure*.

### Object-oriented Paradigm

*Objects!* They are instances of classes that represent real-world entities.
Alone, classes don't do much but can help create a template for the objects. Now objects can encapsulate states and behaviors. They also interact with each other and hold data.
Some essential features of OOP are encapsulation which gives you a clean code without declaring every representation of each object. Inheritance, which allows you to generate classes from other classes sharing the same attributes (do not abuse this power).
Other cool things that come with OOP are:
- You can simplify how you represent your data by representing a whole from a part;
- Basically, you are getting the best things from procedural and functional paradigms. That means: writing faster code with less repetition.

Examples of this languages are: Python, [Ruby](https://en.wikipedia.org/wiki/Ruby_(programming_language)), and JavaScript.
A simple class in Python would look like:
````Python
class School:
  def __init__(self, student, subject):
    self.student = student
    self.subject = subject
````

### Also...
As an honorable mention to Declarative Paradigm, this one is based on writing out what you want and letting the computer do the heavy lifting. A good example of that is SQL.

### In conclusion

There are many more paradigms in programming. Here I just wanted to cover the most used ones. And after all, by the end of the day is the programmer's decision to choose the right tool for the right problem.

References:

1. [hackr.io](https://hackr.io/blog/programming-paradigms#:~:text=Let%20us%20go%20on%20a,-Oriented%2C%20Functional%20and%20Logical.)
2. [codingdojo](https://www.codingdojo.com/blog/what-is-functional-programming#:~:text=Functional%20programming%20(FP)%20is%20an,by%20applying%20and%20composing%20functions.)
3. [w3schools](https://www.w3schools.com/cpp/cpp_oop.asp)
