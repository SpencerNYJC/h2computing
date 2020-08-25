## Classes and Objects

- Object
  * An instance of a class.
- Class
  * A class defines its own class attribute and methods, that will characterize any object that is instantiated from this class



### Class

```python
class Human:
    
    # age is a class attribute, and will be shared by all instances of the class
    age = 17

    # __init__ is a dunder method and is called when the class is instantiated
    def __init__(self, height, weight):
        # self.height and self.weight are instance attributes
        self.height = height
        self.weight = weight
    
    # this is a class method, and can only be called by referencing the class
    def calculate_bmi(self):
        return self.weight / self.height ** 2 * 10000

# timmy is a object, which is an instance of the class Human
timmy = Human(182, 60)

print(timmy.calculate_bmi())
print(timmy.height, timmy.weight, timmy.age)

>>> 18.11375437749064
>>> 182 60 17
```



### Inheritance

Inheritance defines a class that inherits all the methods and attributes from another class.

```python
class Adult(Human):
    
    # this overwrites the inheritance of __init__ function of Human
    def __init__(self, height, weight):
        pass     
```

To keep the inheritance of Human's `__init__()` function, add a call to Human's `__init__()` function:

```python
class Adult(Human):
   
	# alternatively don't overwrite
    def __init__(self, height, weight):
        Human.__init__(self, height, weight)
        # alternatively
        super().__init__(height, weight)
```

### Polymorphism

Polymorphism (ability to take different forms) allows us to define methods in the child class with the same name as defined in their parent class.

```python
class Adult(Human):
    
    def calculate_bmi(self):
        return "Overwritten method: " + str(eval(f"{self.weight} / {self.height} ** 2 * 10000"))
    
jane = Adult(165, 45)
```

```python
print(timmy.calculate_bmi())
print(jane.calculate_bmi())

>>> 18.11375437749064
>>> Overwritten method: 17.7001953125
```

### Encapsulation

Encapsulations puts restriction on accessing variable and methods directly that prevents the accidental modification of data. A object's data can only be modified by a object method. These variables are known as **private variables**.

```python
class Example():
    def __init__(self):
        # protected member
        self._a = 2
        # private member
        self.__b = 3
```



- Protected member
  * can be accessed by inherited classes but not outside the base class
- Private member
  * cannot be accessed by inherited classes and outside the base class





