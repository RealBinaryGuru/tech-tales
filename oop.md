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
### Encapsulation in Naruto

**Definition**: Encapsulation is the bundling of data and methods that operate on that data into a single unit, typically a class, while restricting access to some of the object's components.

## Naruto Analogy:

1. **Data Protection**:
   - **Ninja Secrets**: Just like a ninja (e.g., Naruto) doesn't reveal all their techniques, encapsulation keeps certain data private.
   - **Example**: Naruto has powerful techniques like **Rasengan**, which he uses strategically without disclosing their details.

2. **Public and Private Access**:
   - **Public Methods**: Basic techniques (like **Transformation Jutsu**) are known to everyone.
   - **Private Methods**: Advanced skills (like **Sage Mode**) are kept secret and shared only when necessary.

3. **Controlled Interaction**:
   - **Using Techniques**: A ninja must perform hand signs to execute jutsu, just like methods allow controlled access to an object's data.
   - **Example**: To learn Naruto's chakra level, one would need to interact with him, not access his internal state directly.

## Conclusion:
Encapsulation in programming is like a ninja managing their abilities—keeping some information private and allowing interaction only through specific methods to protect their strengths and weaknesses.

