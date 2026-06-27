🔷 Polymorphism in Python (Simple Explanation)

Polymorphism means “one name, many forms”.
In Python, it allows the same function or method to behave differently depending on the object or input.

Python mainly supports polymorphism in 3 ways 👇

🔹 1. Method Overriding (Run-time Polymorphism)

👉 When a child class provides a new implementation of a method that already exists in the parent class.

Example:
class Animal:
    def sound(self):
        print("Some sound")

class Dog(Animal):
    def sound(self):
        print("Bark")

class Cat(Animal):
    def sound(self):
        print("Meow")
Usage:
a = Dog()
a.sound()

a = Cat()
a.sound()
✔ Key Points:
Same method name in parent and child class
Behavior changes based on object type
Decided at runtime
🔹 2. Method Overloading (Conceptual in Python)

👉 Method overloading means using the same method name with different parameters.

⚠️ Python does NOT support true method overloading like Java or C++.
If multiple methods have the same name, the last one overrides the previous ones.

Concept Example:
class Math:
    def add(self, a, b):
        return a + b

    def add(self, a, b, c):
        return a + b + c
✔ Key Points:
Same method name
Different number/type of parameters (conceptually)
Not natively supported in Python
🔹 3. Duck Typing (Python Special Feature 🐍)

👉 “If it looks like a duck and quacks like a duck, it is a duck.”

In Python, the type of object doesn’t matter. What matters is whether the object has the required method or behavior.

Example:
class Dog:
    def sound(self):
        print("Bark")

class Robot:
    def sound(self):
        print("Beep beep")
Function using duck typing:
def make_sound(obj):
    obj.sound()

make_sound(Dog())
make_sound(Robot())
✔ Key Points:
No need for inheritance
Focus is on behavior, not type
Very flexible and Pythonic approach
🔷 Summary
Type	Description	Python Support
Method Overriding	Child class changes parent method	Yes
Method Overloading	Same method, different parameters	No (concept only)
Duck Typing	Behavior-based polymorphism	Yes (special feature)
🔥 Final Simple Definition

Polymorphism in Python allows the same function or method to behave differently depending on the object, either through method overriding, conceptual overloading, or duck typing.
