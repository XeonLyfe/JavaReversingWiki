# Chapter 1 - JVM structure

> A brief introduction, this part of knowledge does not need to be studied for the time being

Let me talk about a strange thing first. In fact, the JVM itself does not know the JAVA language at all. It only knows its own instruction code, that is, Java bytecode (Java bytecode).

So the flow of the Java program is:

After the Java source code is compiled by javac, it becomes a Java bytecode, and then put into the JVM to be recognized and run by the JVM! [Java running process] (Chapter 1 img/Java running process.png)

<br/>
##Threads:

Java's framework is parallel, which means that different calculations can be run at the same time using multiple threads.

When a new JVM process starts, the first new thread created is the main thread.

After the main thread is created, the code in static main(String[] args) starts running in the main thread.

<br/>
## Frame stack (Stack/Stackframe) and frame (Frames):

Each Java thread has a frame stack for method calls and returns. The frame stack is equivalent to the frame container and is used to control method calls and returns. The JVM will create a frame for the method, and when the method `return`, the corresponding method frame will be destroyed.

![JVM structure](Chapter 1 img/JVM structure.png)

<br/>
## The structure of Frames (later explained in detail):

Frames, also known as method frames, are used to process the content in each method. The frame consists of two main parts: local variable table, operation stack

<br/>
Quote & Reference: https://www.overops.com/blog/jvm-architecture-101-get-to-know-your-virtual-machine/
