# Object-Oriented Programming (OOP)

**Object-Oriented Programming (OOP)** is a programming paradigm that uses objects and classes for organizing and structuring code. It's designed to help manage complex software systems by modeling real-world entities and their interactions. OOP is based on several key concepts that help make programs more modular, reusable, and easier to maintain.

## Key Concepts


## Classes and Objects:

- **Class**: A blueprint for creating objects. It defines a set of attributes and behaviors (methods) that the objects created from the class will have.
- **Object**: An instance of a class. Objects are specific realizations of the class template.

#### Example
```python
class Ninja:
    def __init__(self, name, village, rank):
        self.name = name
        self.village = village
        self.rank = rank

# Create an object
naruto = Ninja(name="Naruto Uzumaki", village="Konoha", rank="Hokage")
print(naruto.name)  # Output: Naruto Uzumaki
```
## Encapsulation:

**Definition**: Encapsulation is the bundling of data and methods that operate on that data into a single unit, typically a class, while restricting access to some of the object's components.

### Naruto Analogy:

1. **Data Protection**:
   - **Ninja Secrets**: Just like a ninja (e.g., Naruto) doesn't reveal all their techniques, encapsulation keeps certain data private.
   - **Example**: Naruto has powerful techniques like **Rasengan**, which he uses strategically without disclosing their details.

2. **Public and Private Access**:
   - **Public Methods**: Basic techniques (like **Transformation Jutsu**) are known to everyone.
   - **Private Methods**: Advanced skills (like **Sage Mode**) are kept secret and shared only when necessary.

3. **Controlled Interaction**:
   - **Using Techniques**: A ninja must perform hand signs to execute jutsu, just like methods allow controlled access to an object's data.
   - **Example**: To learn Naruto's chakra level, one would need to interact with him, not access his internal state directly.

### Conclusion:
Encapsulation in programming is like a ninja managing their abilities—keeping some information private and allowing interaction only through specific methods to protect their strengths and weaknesses.

## Inheritance:

**Inheritance** is a mechanism that allows one class (known as a **subclass** or **derived class**) to inherit properties and behaviors (methods) from another class (known as a **superclass** or **base class**). This promotes code reusability and establishes a natural hierarchy between classes.

### Key Points of Inheritance:
- **Code Reusability**: You can use existing code from a base class without having to rewrite it, reducing redundancy.
- **Hierarchy**: It establishes a parent-child relationship between classes, which can reflect real-world relationships.
- **Overriding**: A subclass can provide a specific implementation of a method that is already defined in its superclass.

## Example of Inheritance

Imagine we have a base class called `Ninja`, and we want to create specific types of ninjas like `Shinobi` and `Jonin`. 

```python
class Ninja:
    def __init__(self, name, village):
        self.name = name
        self.village = village

    def attack(self):
        return f"{self.name} attacks!"

# Subclass: Shinobi
class Shinobi(Ninja):
    def __init__(self, name, village, stealth_level):
        super().__init__(name, village)  # Call to the base class constructor
        self.stealth_level = stealth_level

    def sneak(self):
        return f"{self.name} sneaks with stealth level {self.stealth_level}."

# Subclass: Jonin
class Jonin(Ninja):
    def __init__(self, name, village, experience_level):
        super().__init__(name, village)  # Call to the base class constructor
        self.experience_level = experience_level

    def lead(self):
        return f"{self.name} leads the team with experience level {self.experience_level}."

# Creating objects of subclasses
shino = Shinobi(name="Shino Aburame", village="Konoha", stealth_level=10)
kakashi = Jonin(name="Kakashi Hatake", village="Konoha", experience_level=5)

print(shino.attack())  # Output: Shino Aburame attacks!
print(shino.sneak())   # Output: Shino Aburame sneaks with stealth level 10.
print(kakashi.attack())  # Output: Kakashi Hatake attacks!
print(kakashi.lead())   # Output: Kakashi Hatake leads the team with experience level 5.
```

## Polymorphism: 

is a concept that allows objects to perform the same action but in different ways. Let’s explore this concept using **Naruto** characters and scenarios.



### What is Polymorphism?

In Naruto, many characters are ninjas with unique techniques. Despite their differences, they share common actions, like attacking. Polymorphism in OOP is similar: different objects (ninjas) can use the same method but perform it differently based on their specialization.


### Types of Polymorphism

### **1. Compile-Time Polymorphism (Method Overloading)**

This is like a ninja using multiple variations of a technique. For example:

- Kakashi’s **Sharingan** can:
  - Copy techniques.
  - Trap enemies in Genjutsu.
  - Predict movements.

In programming, this is achieved by defining multiple methods with the same name but different parameters.

**Example in Code**:
```python
class Ninja:
    def attack(self, target):
        return f"Attacking {target} with basic attack."

    def attack(self, target, technique):
        return f"Attacking {target} using {technique}."

# Usage
kakashi = Ninja()
print(kakashi.attack("enemy", "Sharingan Genjutsu"))
# Output: Attacking enemy using Sharingan Genjutsu.
```

### **2. Run-Time Polymorphism (Method Overriding)**

This is like different ninja clans having unique signature jutsu:

- Naruto uses Rasengan.
  - Sasuke uses Chidori.
  - Rock Lee relies on Taijutsu.
In programming, this is achieved by overriding a method in a subclass.

**Example in Code**:
```python
class Ninja:
    def attack(self):
        return "Basic attack!"

class Naruto(Ninja):
    def attack(self):
        return "Naruto attacks with Rasengan!"

class Sasuke(Ninja):
    def attack(self):
        return "Sasuke attacks with Chidori!"

# Usage
ninjas = [Naruto(), Sasuke()]
for ninja in ninjas:
    print(ninja.attack())

# Output:
# Naruto attacks with Rasengan!
# Sasuke attacks with Chidori!

```

## Abstraction:
is the process of hiding complex details and showing only the essential features of an object or concept. In OOP, abstraction allows developers to define methods that declare the functionality but not the specifics of how it is implemented.

In Naruto, abstraction can be understood by looking at how techniques (jutsu) are used:


### 1. Using Jutsu Without Knowing How They Work:
- Ninjas perform powerful techniques (e.g., **Shadow Clone Jutsu**) without everyone needing to know how the technique is actually implemented. For example:
  - **Naruto's Shadow Clone Jutsu**: The village ninja only need to see the result (multiple clones appear). They don’t need to understand the inner workings of chakra splitting.
- In programming, this is like having an abstract class or method where the "how" is hidden, and only the "what" is defined.

---

### 2. Abstracting Jutsu Types:
- All jutsu can be grouped into broad categories (e.g., **Ninjutsu, Taijutsu, Genjutsu**). The details of how each jutsu works are abstracted, and only their category and purpose are defined.
- For example:
  - **Ninjutsu**: Uses chakra to manipulate elements or create effects.
  - **Taijutsu**: Focuses on physical combat and requires no chakra.
  - **Genjutsu**: Alters perception using illusions.
- Each category defines an abstract "framework" that individual techniques (e.g., **Rasengan, Chidori, Leaf Hurricane**) implement differently.

```python 
from abc import ABC, abstractmethod

# Abstract class
class Jutsu(ABC):
    @abstractmethod
    def execute(self):
        pass  # Abstract method, no implementation

# Ninjutsu implementation
class Ninjutsu(Jutsu):
    def execute(self):
        return "Performing Ninjutsu with chakra manipulation!"

# Taijutsu implementation
class Taijutsu(Jutsu):
    def execute(self):
        return "Performing Taijutsu with physical combat!"

# Genjutsu implementation
class Genjutsu(Jutsu):
    def execute(self):
        return "Performing Genjutsu to alter perception!"

# Using the abstracted Jutsu types
def perform_jutsu(jutsu: Jutsu):
    print(jutsu.execute())

# Creating objects
ninjutsu = Ninjutsu()
taijutsu = Taijutsu()
genjutsu = Genjutsu()

# Perform abstracted actions
perform_jutsu(ninjutsu)  # Output: Performing Ninjutsu with chakra manipulation!
perform_jutsu(taijutsu)  # Output: Performing Taijutsu with physical combat!
perform_jutsu(genjutsu)  # Output: Performing Genjutsu to alter perception!
```
