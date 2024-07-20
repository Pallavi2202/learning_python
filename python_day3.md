# oops concepts
   
 1. classes and objects
 2. inheritance
 3. data abstraction
 4. polymorphism
 5. encapsulation

## classes and objects
## coding
    # Define a class named 'Car'
    class Car:
    # Constructor method to initialize attributes
    def __init__(self, brand, model):
        self.brand = brand  # Instance variable
        self.model = model  # Instance variable
    
    # Method to display information about the car
    def display_info(self):
        print(f"Car: {self.brand} {self.model}")

    car1 = Car("Toyota", "Corolla")
    car2 = Car("Tesla", "Model S")

    car1.display_info()
    car2.display_info()
## result
    Car: Toyota Corolla
    Car: Tesla Model S
## inheritance
    # Parent class
    class Animal:
    def __init__(self, species):
        self.species = species
    
    def sound(self):
        return "Some sound"  # Default sound, to be overridden

    # Child class inheriting Animal
    class Dog(Animal):
    def __init__(self, breed):
        super().__init__("Dog")  # Call parent's constructor
        self.breed = breed
    
    def sound(self):
        return "Woof!"  # Dog's sound

    # Child class inheriting Animal
    class Cat(Animal):
    def __init__(self, breed):
        super().__init__("Cat")  # Call parent's constructor
        self.breed = breed
    
    def sound(self):
        return "Meow!"  # Cat's sound

    # Creating instances of the child classes
    dog = Dog("Labrador")
    cat = Cat("Persian")

    # Outputting their properties and methods
    print(f"{dog.species} ({dog.breed}): {dog.sound()}")
    print(f"{cat.species} ({cat.breed}): {cat.sound()}")
## result
    Dog (Labrador): Woof!
    Cat (Persian): Meow!
# data abstraction
    from abc import ABC, abstractmethod

    # Abstract class defining an interface
    class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

    # Concrete implementation of Shape
    class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius * self.radius
    
    def perimeter(self):
        return 2 * 3.14 * self.radius

    # Usage of Circle class
    circle = Circle(5)
    print("Area:", circle.area())
    print("Perimeter:", circle.perimeter())
## result
    Area: 78.5
    Perimeter: 31.400000000000002
# polymorphism and encapsulation
    # Parent class (encapsulation)
    class Shape:
    def __init__(self, name):
        self.name = name
    
    def area(self):
        pass  # To be overridden in subclasses

    # Child classes (polymorphism)
    class Circle(Shape):
    def __init__(self, name, radius):
        super().__init__(name)
        self.radius = radius
    
    def area(self):
        return 3.14 * self.radius * self.radius

    class Square(Shape):
    def __init__(self, name, side_length):
        super().__init__(name)
        self.side_length = side_length
    
    def area(self):
        return self.side_length * self.side_length

    # Function demonstrating polymorphism
    def print_area(shape):
    print(f"The area of {shape.name} is: {shape.area()}")

    # Usage of the function with different objects
    circle = Circle("Circle", 5)
    square = Square("Square", 4)

    # Outputting the areas using polymorphism
    print_area(circle)
    print_area(square)
## result
      The area of Circle is: 78.5
      The area of Square is: 16


        
