+++
author = "Burhanuddin Raja"
title = "Fundamentals of Programming"
date = "2022-09-10"
description = "Intorduction to fundamentals of Programming. Here, I have discussed about types of programming languages, How programs run in your machine, basic syntax, data types and many more."
tags = [
    "fundamentals of programming",
    "types of programming language",
    "run programs on machine",
    "syntax of programming",
    "data-types in a language",
    "intro to basic data structures",
]
+++

### Introduction

In today's world we are surrounded by computers. Not just mobiles and desktops but we have smart bulbs, smart refrigerator, smart dish washer etc. Computer Programming is a set of instructions given that tell the computer how to process the given data and produce results.

### How does your Computer Program works?

All computers contains a microprocessor i.e. CPU (Central Processing Unit) which understands a special kind of code called Machine code. This Machine code is made of binary numbers. These binary numbers contains 0s and 1s. On atomic level the CPU contains billions of transistors which acts as switchs that goes on and off when the electrical signal passes through. These signals are made up of 0s and 1s.

For Example 'Hello World' in binary: `01001000 01100101 01101100 01101100 01101111 00100000 01010111 01101111 01110010 01101100 01100100`


These binary numbers are used to express data and operations in a Macine code. The binary representation of any form is not human readable, that is the reason the Machine code is called a Low-level Language.

There are several languages which are called High-level languages which is human readable. These languages such as Java, Javascript, Python, C++ etc. are converted to Machine code for the machine to understand and give you the desired output. The programs that we write in these languages are called Source Code.

You might be wondering, how Machine Code is converted to Source Code? Lets see.

There are two ways with which these programming Source Code can be converted to Machine Code. They are:-

1. Compilation
2. Interpretation

##### Compilation

Here, a developer working with a programming language incorporates a compiler. For instance, C++, Rust etc. are compiled languages. A compiler is a software that converts source code to machine code and this process if called **Compilation**. 

&nbsp;

{{< image src="/img/compilationProcess.jpg" alt="Compilation Process" position="center" style="border-radius: 8px;" >}}

&nbsp;

So, a developer writes some code compiles it according to the Operating system as every system requires different configuration of machine code and the result that we get after conversion is an executable file cotaining machine code. This file will be given to end user to run on their computer. This executable file can be run on any computer with the same Operating system. This process of compilation is also called Ahead-Of-Time Compilation.

&nbsp;

#### Interpretation

Here, a developer working with a programming language does not require anything. For instance, Javascript, Python etc. are interpreted languages. An interpreter is a software that converts source code to byte code and byte code to machine code when the code is executed on the end user computer and this process is called **Interpretation**.

&nbsp;

{{< image src="/img/interpretation.jpg" alt="Interpretation" position="center" style="border-radius: 8px;" >}}

&nbsp;

Here, the interpreter does not give end user the executable file rather it gives the source code to the end user and the user's computer contains a language interpreter in order to execute the the source code.

The interpreter uses Just-In-Time compiler. This compiler converts the source code to byte code and this byte code is converted to machine code using a Bytecode Compiler or Virtual Machine. After these steps the code is executed on the user's computer. The Bytecode Compiler or Virtual Machine used by the interpreter is language specific. For instance, Javascript uses bytecode compiler and Python uses virtual machine.

&nbsp;

{{< image src="/img/detailed_interpreter.jpg" alt="Interpretation Process" position="center" style="border-radius: 8px;" >}}

&nbsp;

We can also say there is a third way to convert the Source Code to Machine Code. It basically happens in programming language called Java. It is kind of a mixture of the above two ways. Lets see.

&nbsp;

{{< image src="/img/java_jvm.jpg" alt="Interpretation Process" position="center" style="border-radius: 8px;" >}}

&nbsp;

In Java, source code is converted to a intermediate code called Byte Code. And this Byte Code further is converted to Machine code doing the similar process as interpreter. To run the Java program, it requires a Java Virtual Machine(JVM).



### What is Programming Syntax?

Syntax are the set of instructions corresponding to a particular programming langauge. It contains certain keywords. Keywords are some reserved or specific words in a language. They act like tokens of instructions when you put them in a program. Let's take an example of a programming language called Javascript.

{{< code language="javascript" title="Example of Keywords" id="1" expand="Show" collapse="Hide" >}}

if (count < 10) {
    console.log("Hello");
}
else {
    console.log("World!");
}

{{< /code >}}

As you can see in the above example the keywords `if` and `else` are reserved for the programming language. You cannot use these keywords for any other purpose that defined in a programming language.

List of some common Keywords for all the programming languages :-

- if
- else
- for
- while
- do
- switch
- true
- false
- return
- continue
- break

and many more

##### Case sensitivity

Syntax of the programming languages should be written based on some rules defined according to a particular programming languages. Like in the above code sample of keywords, I gave example of `if` and `else`. It caannot be written like this :- 

{{< code language="javascript" title="Example of Keywords" id="2" expand="Show" collapse="Hide" isCollapsed="false" >}}

If (count < 10) {
    console.log("Hello");
}
Else {
    console.log("World!");
}

{{< /code >}}

Capital first letter of If and Else is not correct accordding to the javascript rules. This is also called case sensitivity. It should be `if` and `else` for the above example.


##### Statements

It is important for the Syntax to contain statements because it defines that from where the program begins and where it ends. Lets understand this by example.

{{< code language="javascript" title="Example of Keywords" id="3" expand="Show" collapse="Hide" isCollapsed="false" >}}

function checkAge(count) {
    if (count < 30) {
        console.log("Young");
    }
    else {
        console.log("Old");
    }
}

{{< /code >}}

The statements start and end is determined by the `{}` brackets. As you can see in the above code the function named `checkAge()` where it has started and ended. And you can also see the statements for `if` ans `else` too.

In some languages like Python, there are no `{}` brackets to determine the start and end of a statement rather it uses indentations. Indentations are the space left for the compiler to understand the statements. For example the same function as above can be written in Python as :-

{{< code language="python" title="Example of Keywords" id="4" expand="Show" collapse="Hide" isCollapsed="false" >}}

def checkAge(count):
    if count < 30:
        print("Young")
    else:
        print("Old")

{{< /code >}}

In Python, how an interpreter can understand the start and end of any statement. This is possible using **Lexer**.

Lexer is converts this code into tokens using a method called Lexical Analysis. In this analysis, it ignores the white spaces in the code and categorize them into several token headers. We can also say it sets the token as per the grammar of the language. This the reason Lexer is also called tokenizers.

Now, these tokens further goes to a component called parser. This parser tries to make sense out of this tokenized code. The parser converts these tokens and constructs a tree of tokens representing the logical form of program. This process is called Parser Syntax Analysis. The parser helps the compiler to understand the program and the program is further passed to the compiler.


### Data Types

The data types are classification of the given data from which the compiler and interpreter can interpret that which type of input is given. For example, it could be integer, decimal, true or false etc.

- **Integer** is a numeric value like 923, 2432 etc.
- **Float** is a decimal value like 32.90, 45.1387 etc.
- **Boolean** is true or false.
- **Char** is where you can have character or single letter, like 'a', 'k' etc.
- **String** is where you can write words in, like "Hello World!".

The above data types are in every programming languages. There more types of data types used in many diffeent programming languages.

&nbsp;

#### Follow me on Github :- [BurhanRaja](https://github.com/BurhanRaja)
#### Follow me on Twitter :- [Burhan_Raja52](https://twitter.com/Burhan_Raja52)
#### Follow me on Linkedin :- [Burhanuddin Raja](https://twitter.com/Burhan_Raja52)
###### This was all from my side about Introduction to Programming.
###### Hope It was helpful.
###### Stay Tuned for more
###### Thank you.