---
toc: true
comments: false
layout: post
title: Python Quiz
type: hacks
courses: { compsci: {week: 2} }
---

``` python
import getpass, sys

def question_with_response(prompt):
    print("Question: " + prompt)
    msg = input()
    return msg

questions = 3
correct = 0

print('Hello, ' + getpass.getuser() + " running " + sys.executable)
print("You will be asked " + str(questions) + " questions.")
question_with_response("Are you ready to take a test?")

rsp = question_with_response("What variable is the dynamic result of the input command?")
if rsp == "msg":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")

rsp = question_with_response("What is a keyword in python that defines a function?")
if rsp == "def":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")

rsp = question_with_response("What kind of text is this in python: Hello World")
if rsp == "static":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")
    
percentage = (correct / questions) * 100
print(f"You got: {percentage:.2f}%")