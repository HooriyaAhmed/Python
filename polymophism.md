Polymorphism in Python
Overview

Polymorphism is one of the core concepts of Object-Oriented Programming (OOP).
The word Polymorphism means “many forms”.

In Python, it allows the same function or method name to behave differently depending on the object or input.

Types of Polymorphism in Python

Python supports polymorphism mainly in three ways:

1. Method Overriding (Run-time Polymorphism)

Method overriding occurs when a child class provides a specific implementation of a method that is already defined in its parent class.

Example:
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):
    def sound(self):
        print("Dog barks")

class Cat(Animal):
    def sound(self):
        print("Cat meows")
Usage:
animals = [Dog(), Cat()]

for animal in animals:
    animal.sound()
Output:
Dog barks
Cat meows
Key Points:
Same method name in parent and child classes
Behavior depends on object type
Happens at run-time
2. Method Overloading (Simulated in Python)

Python does not support true method overloading.
However, it can be simulated using default arguments or variable-length arguments.

Example:
class Calculator:
    def add(self, a, b, c=0):
        return a + b + c
Usage:
calc = Calculator()

print(calc.add(2, 3))
print(calc.add(2, 3, 4))
Output:
5
9
Key Points:
Same method name
Different number of inputs handled using default parameters
Not natively supported like Java/C++
3. Duck Typing (Pythonic Polymorphism)

In Python, the type of object is not important. What matters is whether the object has the required method or behavior.

Example:
class Dog:
    def speak(self):
        print("Bark")

class Robot:
    def speak(self):
        print("Beep Beep")
Usage:
def call_speak(obj):
    obj.speak()

call_speak(Dog())
call_speak(Robot())
Output:
Bark
Beep Beep
Key Points:
No inheritance required
Focus is on behavior, not object type
Very flexible and widely used in Python
Summary
Type	Description	Support in Python
Method Overriding	Child class modifies parent method	Yes
Method Overloading	Same method, different parameters	Simulated
Duck Typing	Behavior-based polymorphism	Yes
Conclusion

Polymorphism in Python enables flexible and reusable code by allowing the same interface to represent different underlying forms.
