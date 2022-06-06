# Exercises-Object-Oriented
In this repository, you are going to find various questions and answers which are created in respect to object-oriented programming.
Questions Part I
Question 1
An anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once. For example: “New York Times” => “monkeys write”

Write a function named is_anagram that takes two strings as arguments and returns True if the strings are anagrams, and returns False otherwise:

def is_anagram(str1,str2):
	# You do this part
Question 2
Write a function which finds the first non-prime number in the given list. If all the numbers are prime, return None.

def first_non_prime():
	# You do this part

    
print(first_non_prime([2,3,52,19])) # prints 52
print(first_non_prime([2,101,71462394821,55467547393])) # prints 71462394821
print(first_non_prime([2,3,5,7,11])) #prints nothing 
Question 3
Write a function called substring_count that takes two strings and returns how many times the second string occurs in the first one as an integer. You need also count overlapping substrings in the given string.


def substring_count(first, second):
	# You do this part

substring_count("lifeforlifeforlifeforlife","life") # returns 4
substring_count("lifeforlifeforlifeforlife","lifeforlife") # returns 3
Question 4
Make a class that represents a circle.

The circle should have a radius, a diameter, and an area. The circle object should be created by giving the value of the radius to the constructor. It should also have a nice string representation.

For example:

>>> c = Circle(5)
>>> c
Circle(5.0)
>>> c.radius()
5.0
>>> c.diameter()
10.0
>>> c.area()
78.53981633974483
Additionally, the radius should default to 1 if no radius is specified when you create your circle:

>>> c = Circle()
>>> c.radius()
1.0
>>> c.diameter()
2.0
The Circle class’s radius, diameter and area methods should be used to both get and set their respective values. If no argument is given they will act as getters, if an argument is given, they will be setters. Radius, diameter and area need to be numeric (int or float). For example:

>>> c = Circle()
>>> c.radius()
1.0
>>> c.radius(4.5)
>>> c.radius()
4.5
>>> c.area()
63.61725123519331
>>> c.area(10)
>>> c.area()
10.0
Make sure that when one aspect (radius/diameter/area) of your class changes, that the others also reflect the changes:

>>> c = Circle(2)
>>> c.radius(1)
>>> c.diameter()
2
>>> c.area()
3.141592653589793
>>> c
Circle(1)
>>> c.radius(2)
>>> c.diameter()
4.0
>>> c.area()
12.566370614359172
>>> c
Circle(2.0)
>>> c.area(5)
>>> c.radius()
1.2615662610100802
>>> c.diameter()
2.5231325220201604
>>> c
Circle(1.26)
Implement this Circle class. The class name, and the method names should be exactly as given above. You may create other methods if you like, but the radius, diameter, and area methods must exist.

Question 5
Develop an inheritance hierarchy based upon the following Polygon class:

import math

class Polygon:
    def __init__(self, sides):
        """Initialized with the lengths of the sides"""
        for s in sides:
            if s <= 0:
                raise ValueError('Side lengths must be positive')
        self._sides = sides
        self._name = "Polygon"

    def name(self):
        return self._name

    def area(self):
        """The area of an arbitrary polygon is unknown"""
        return None #placeholder

    def perimeter(self):
        total = 0.0
        for s in self._sides:
            total += s
        return total
Implement classes Triangle and Parallelogram that extend this base class, with the obvious meanings for the area() and perimeter() methods. Also implement classes, IsoscelesTriangle, EquilateralTriangle, Rectangle, and Square, that have the appropriate inheritance relationships. the math module is already imported, you can use math.sqrt if needed.

The following should work:

shapelist = [Polygon([1.0,4.5,3.1,3.3]),
             Triangle(3.4,5.3,4.2),
             IsocelesTriangle(4.1,1),
             EquilateralTriangle(4.2),
             Rectangle(5,4),
             Square(3.25)]

for shape in shapelist:
    print('{0} Area: {1:.3f}  Perimeter: {2:.3f}'.format(shape.name(),
                                                           shape.area(),
                                                           shape.perimeter()))
and should print out:

Polygon Area:  Perimeter: 11.900
Triangle Area: 7.135  Perimeter: 12.900
IsoscelesTriangle Area: 2.035  Perimeter: 9.200
EquilateralTriangle Area: 7.638  Perimeter: 12.600
Rectangle Area: 20.000  Perimeter: 18.000
Square Area: 10.5625  Perimeter: 13.000
