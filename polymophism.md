Python mein polymorphism ko **simple exam style mein “all types”** ke form mein aise samjho 👇

---

# 🔷 Polymorphism ke Types (Python OOP)

Python mein polymorphism ko 3 main types mein samjhaya jata hai:

---

# 🔹 1. Method Overriding (Run-time Polymorphism)

👉 Jab parent class ka method child class mein same name se change ho jaye

```python id="t1"
class Animal:
    def sound(self):
        print("Some sound")

class Dog(Animal):
    def sound(self):
        print("Bark")
```

### Use:

```python id="t2"
a = Dog()
a.sound()
```

✔ Same method name
✔ Different behavior
✔ Run-time pe decide hota hai

---

# 🔹 2. Method Overloading (Conceptual in Python)

👉 Same function name, different parameters

⚠️ Python direct support nahi karta (latest function override ho jata hai), lekin concept samjha jata hai

```python id="t3"
class Math:
    def add(self, a, b):
        return a + b

    def add(self, a, b, c):
        return a + b + c
```

✔ Same name
✔ Different arguments
✔ Compile-time concept (theory)

---

# 🔹 3. Duck Typing (Python Special)

👉 “Agar object ka behavior same hai to usay same treat karo”

```python id="t4"
class Dog:
    def sound(self):
        print("Bark")

class Robot:
    def sound(self):
        print("Beep")
```

```python id="t5"
def make_sound(obj):
    obj.sound()

make_sound(Dog())
make_sound(Robot())
```

✔ Object type important nahi
✔ Method important hota hai
✔ Very Pythonic concept 🐍

---

# 🧠 Final Summary (exam line):

👉 Python mein polymorphism 3 types ka hota hai:

1. Method Overriding (Run-time)
2. Method Overloading (conceptual)
3. Duck Typing (Python-specific)

---

# 💡 One-line yaad rakh:

👉 “Override = inheritance change, Overload = same name different args, Duck = behavior matters not type”

---

Agar chaho to main tumhein **OOP complete revision (Abstraction + Encapsulation + Inheritance + Polymorphism) ek hi page mein** bana deta hoon 👍
