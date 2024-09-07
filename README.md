
# my first project

# area of an irregular shape

import math

pi = math.pi
total_circle_area= 0
total_square_area = 0
total_triangle_area = 0
total_rectangle_area = 0
total_area = 0

def a_circle(r):
    return pi*r**2
def a_square(l):
    return l**2
def a_rectangle(length, w):
    return length * w
def a_triangle(b, h):
    return 0.5 * b * h

print("Please put the number of shapes (circle,square,triangle and rectangle) that are in your irregular shape:")
circles = int(input("Number of circles: "))
squares = int(input("Number of squares: "))
triangles = int(input("Number of triangles: "))
rectangles = int(input("Number of rectangles: "))

while circles> 0:
    r = float(input("Radius of circle: "))
    total_circle_area += a_circle(r)
    circles -= 1

while squares> 0:
    l = float(input("Length of square: "))
    total_square_area += a_square(l)
    squares -= 1

while triangles> 0:
    b = float(input("Base of triangle: "))
    h = float(input("Height of triangle: "))
    total_triangle_area += a_triangle(b, h)
    triangles -= 1

while rectangles> 0:
    length = float(input("Length of rectangle: "))
    w = float(input("Width of rectangle: "))
    total_rectangle_area += a_rectangle(length, w)
    rectangles -= 1

total_area = total_circle_area + total_triangle_area + total_rectangle_area + total_square_area

print(f"Area of the circles is: {total_circle_area: .2f}")
print(f"Area of the squares is: {total_square_area: .2f}")
print(f"Area of the triangles is: {total_triangle_area: .2f}")
print(f"Area of the rectangles is: {total_rectangle_area: .2f}")
print(f"The area of the irregular shape is equal to: {total_area: .2f}")
