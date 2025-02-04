# Python-Oops
A Python repository demonstrating Object-Oriented Programming (OOP) concepts.  Includes examples of classes, inheritance, polymorphism, and encapsulation, explained with clear and concise code.  Ideal for learning OOP in Python.
Python Object-Oriented Programming (OOPs) Guide

Python Object-Oriented Programming (OOPs) Guide

Introduction

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of objects. It allows for modular, reusable, and scalable code by encapsulating data and behavior together. This repository explores key OOP concepts in Python with examples.

Key Concepts

1. Class & Object

Class: A blueprint for creating objects.

Object: An instance of a class.

Example:

class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model
    
    def display(self):
        print(f"Car: {self.brand} {self.model}")

my_car = Car("Toyota", "Corolla")
my_car.display()

2. Encapsulation

Restricting direct access to certain attributes using private/protected members.

Example:

class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable
    
    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
print(account.get_balance())

3. Abstraction

Hiding implementation details and exposing only necessary parts.

Example:

from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        return "Bark"

dog = Dog()
print(dog.make_sound())

4. Dunder Methods (Magic Methods)

Special methods in Python (e.g., __init__, __str__, __len__).

Example:

class Book:
    def __init__(self, title):
        self.title = title
    
    def __str__(self):
        return f"Book: {self.title}"

book = Book("Python Basics")
print(book)

5. Inheritance

Deriving a class from another class.

Example:

class Vehicle:
    def move(self):
        print("Moving...")

class Car(Vehicle):
    pass

car = Car()
car.move()

6. Polymorphism

Using a unified interface for different types.

Example:

class Bird:
    def speak(self):
        return "Chirp"

class Dog:
    def speak(self):
        return "Bark"

def animal_sound(animal):
    print(animal.speak())

animal_sound(Bird())
animal_sound(Dog())

7. Constructor (__init__ Method)

Initializes object attributes.

Example:

class Person:
    def __init__(self, name):
        self.name = name

    def greet(self):
        print(f"Hello, {self.name}!")

p = Person("Alice")
p.greet()

8. Class Methods & Static Methods

Class Method (@classmethod): Works with class attributes.

Static Method (@staticmethod): Does not modify class or instance attributes.

Example:

class Math:
    value = 10
    
    @classmethod
    def modify_value(cls, new_value):
        cls.value = new_value
    
    @staticmethod
    def add(x, y):
        return x + y

Math.modify_value(20)
print(Math.value)
print(Math.add(5, 10))

9. Method Overloading & Overriding

Method Overloading: Same method name but different parameters (Python does not support overloading natively but can be mimicked).

Method Overriding: Redefining a parent class method in a child class.

Example:

class Parent:
    def show(self):
        print("Parent Class")

class Child(Parent):
    def show(self):
        print("Child Class")

obj = Child()
obj.show()  # Output: Child Class

10. Property Decorator (@property)

Used to define getter and setter methods in a cleaner way.

Example:

class Employee:
    def __init__(self, salary):
        self._salary = salary
    
    @property
    def salary(self):
        return self._salary
    
    @salary.setter
    def salary(self, value):
        if value > 0:
            self._salary = value
        else:
            raise ValueError("Salary must be positive!")

emp = Employee(5000)
print(emp.salary)
emp.salary = 6000
print(emp.salary)

11. Class Variable & Instance Variable

Class Variable: Shared among all instances.

Instance Variable: Specific to each object.

Example:

class Student:
    school = "ABC School"  # Class variable
    
    def __init__(self, name):
        self.name = name  # Instance variable

s1 = Student("John")
s2 = Student("Jane")
print(s1.school, s1.name)
print(s2.school, s2.name)

12. Multiple Inheritance

A class inheriting from multiple parent classes.

Example:

class A:
    def method_A(self):
        print("Method A")

class B:
    def method_B(self):
        print("Method B")

class C(A, B):
    pass

obj = C()
obj.method_A()
obj.method_B()

Conclusion

This repository serves as a comprehensive guide to Python OOPs concepts. Feel free to explore, modify, and experiment with the provided examples!



