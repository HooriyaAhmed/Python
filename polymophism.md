Polymorphism in Python (Simple Explanation)

Polymorphism means “one interface, many forms.”
In simple words, it allows the same function or method to behave differently depending on the object.

🔹 1. Method Overriding (Run-time Polymorphism)

👉 When a child class changes the behavior of a method that already exists in the parent class.

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
a1 = Dog()
a1.sound()

a2 = Cat()
a2.sound()
Output:
Dog barks
Cat meows

✔ Same method name (sound)
✔ Different behavior in different classes

🔹 2. Method Overloading (Concept in Python)

👉 Same method name but different number of arguments.
⚠️ Python does NOT support true overloading, but we can simulate it.

Example:
class Calculator:
    def add(self, a, b, c=0):
        return a + b + c
Usage:
calc = Calculator()

print(calc.add(2, 3))      # 5
print(calc.add(2, 3, 4))    # 9

✔ Same method name
✔ Works with different inputs using default arguments

🔹 3. Duck Typing (Python Special Feature 🐍)

👉 “If it behaves like the required object, we use it.”

Example:
class Dog:
    def speak(self):
        print("Bark")

class Robot:
    def speak(self):
        print("Beep Beep")
Function:
def call_speak(obj):
    obj.speak()

call_speak(Dog())
call_speak(Robot())
Output:
Bark
Beep Beep

✔ No need for inheritance
✔ Only method name matters, not object type

🔷 Final Summary
Method Overriding → same method, different class behavior
Method Overloading → same method, different inputs (simulated in Python)
Duck Typing → behavior matters, not object type
🧠 Simple Definition

👉 Polymorphism means the same method or function can work in different ways depending on the object.
