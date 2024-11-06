#__practical__1_

#Finding_roots



import math

# Function to find roots of the quadratic equation
def find_roots(a, b, c):
    # Calculate the discriminant
    discriminant = b**2 - 4 * a * c
    
    # Check if roots are real and different
    if discriminant > 0:
        root1 = (-b + math.sqrt(discriminant)) / (2 * a)
        root2 = (-b - math.sqrt(discriminant)) / (2 * a)
        return f"Roots are real and different: Root1 = {root1}, Root2 = {root2}"
    
    # Check if roots are real and the same
    elif discriminant == 0:
        root1 = -b / (2 * a)
        return f"Roots are real and same: Root = {root1}"
    
    # If roots are complex
    else:
        real_part = -b / (2 * a)
        imaginary_part = math.sqrt(-discriminant) / (2 * a)
        return f"Roots are complex: Root1 = {real_part} + {imaginary_part}i, Root2 = {real_part} - {imaginary_part}i"

# Taking input from the user
a = float(input("Enter coefficient a: "))
b = float(input("Enter coefficient b: "))
c = float(input("Enter coefficient c: "))

# Checking if a is zero
if a == 0:
    print("The coefficient 'a' cannot be zero in a quadratic equation.")
else:
    # Finding and printing the roots
    print(find_roots(a, b, c))