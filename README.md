# Python OOP Inheritance Example

This project demonstrates the concept of **Object-Oriented Programming (OOP)** in Python using **inheritance**.  
A base class `Car` is created, and a child class `ElectricCar` inherits all its properties and methods.

---

## 🚗 Project Overview

- `Car` class contains:
  - Basic attributes (make, model, year)
  - Odometer functionality
  - Methods to read, update, and increment mileage

- `ElectricCar` class:
  - Inherits all features from `Car`
  - Demonstrates how child classes reuse parent class functionality

---

## 📌 Features
- Class inheritance  
- Method overriding support (if needed)  
- Odometer update and validation  
- Clean and beginner-friendly implementation  

---

## 🧩 Code Structure

 **car.py**
python
class Car:    
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0

    def get_descriptive_name(self):
        long_name = str(self.year) + ' ' + self.make + ' ' + self.model
        return long_name.title()

    def read_odometer(self):
        print("This car has " + str(self.odometer_reading) + " miles on it.")

    def update_odometer(self, mileage):
        if mileage >= self.odometer_reading:
            self.odometer_reading = mileage
        else:
            print("You can't roll back an odometer!")

    def increment_odometer(self, miles):
        self.odometer_reading += miles


class ElectricCar(Car):
    pass


# Create object OUTSIDE the class
ec1 = ElectricCar('Tesla', 'Electric', 2005)

# Increase mileage
ec1.increment_odometer(20)

# Print updated odometer reading
ec1.read_odometer()
