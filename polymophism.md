🔷 Polymorphism in Python (Easy Explanation)

Polymorphism means “same name, different behavior”.
It allows us to use the same method/function in different ways.

🔹 1. Method Overriding (Run-time Polymorphism)

👉 Same method name in parent and child class, but different behavior.

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
Output:
Bark
Meow

✔ Same method (sound)
✔ Different output based on object

🔹 2. Method Overloading (Concept only in Python)

👉 Same function name, different inputs (not truly supported in Python)

Example:
class Math:
    def add(self, a, b):
        return a + b

    def add(self, a, b, c):
        return a + b + c
Concept idea:
m = Math()
print(m.add(2, 3))     # 5
print(m.add(2, 3, 4))  # 9

⚠️ In real Python, the last method replaces the first one.

✔ Same function name
✔ Different arguments (theory concept)

🔹 3. Duck Typing (Python Special 🐍)

👉 “If it behaves like it, treat it like it”

Example:
class Dog:
    def sound(self):
        print("Bark")

class Robot:
    def sound(self):
        print("Beep Beep")
Function:
def make_sound(obj):
    obj.sound()

make_sound(Dog())
make_sound(Robot())
Output:
Bark
Beep Beep

✔ No inheritance needed
✔ Only method matters, not object type

🔥 Simple Summary
Overriding → same method, different class behavior
Overloading → same method, different inputs (concept only)
Duck Typing → behavior matters, not type
🧠 One-line definition

👉 Polymorphism = same function name, different behavior in different situations
