# Object-Oriented Programming (OOP)

**Object-Oriented Programming (OOP)** is a programming paradigm that uses objects and classes for organizing and structuring code. It's designed to help manage complex software systems by modeling real-world entities and their interactions. OOP is based on several key concepts that help make programs more modular, reusable, and easier to maintain.

## Key Concepts

### Classes and Objects
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
