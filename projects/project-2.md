---
layout: project
type: project
image: images/calc.jpg
title: Postfix Prefix Calculator
permalink: projects/calculator
# All dates must be YYYY-MM-DD format!
date: 2020-10-15
labels:
  - Javascript
  - Post-fix
  - Pre-fix
  - Stack
summary: I created a Post-fix and Pre-fix Calculator for my ICS211 class using Stack ADT.
---

<img class="ui medium right floated rounded image" src="../images/calc.jpg">

In my ICS211 course, I was tasked to implement the Postfix and Prefix Calculator to calculate the given expression. The assignment was an individual project. Professor Moore provided a format of the code, and our classmates had to implement the code to calculate the answer and returns the solution. The main theme of this assignment was using a Stack to keep track of the operands. Our code must return an Integer when it received int math and a Double when it received floating point math.



By doing this assignment, I learned the concepts of post-fix and pre-fix calculation. Furthermore, I was able to learn how to use Stack ADT. For instance, we can only access the top of the stack, and stack is usually known as LIFO (last in first out). I gained more experience with Javascript using a stack to store information.


Here is my code example for reversing the string for the pre-fix calculate:
```js
  private String reverse(String s) {

    // Specifying the pattern to be searched
    Pattern pattern = Pattern.compile("\\s");

    // splitting String str with a pattern
    // (i.e )splitting the string whenever their
    // is whitespace and store in temp array.
    String[] temp = pattern.split(s);
    String result = "";

    // Iterate over the temp array and store
    // the string in reverse order.
    for (int i = 0; i < temp.length; i++) {
      if (i == temp.length - 1) {
        result = temp[i] + result;
      } else {
        result = " " + temp[i] + result;
      }
    }
    return result;
  }

}
```

View code: <a href="https://github.com/cathy-kim95/calculator"> Calculator

