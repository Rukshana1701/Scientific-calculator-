import math

class Scientific CalculatorAl:

def basic_operations(self, operation, num1, num2=None):

Perform basic arithmetic operations. 

if operation == "add":

return num1 + num2

elif operation == "subtract":

return num1 - num2

elif operation == "multiply":

return num1 * num2

elif operation == "divide":

return num1 / num2 if num2 != 0 else "Error: Division by zero"

else:

return "Invalid operation"

def trigonometry(self, func, angle):

Perform trigonometric calculations.

angle_radians = math.radians(angle)

if func == "sin":

return math.sin(angle_radians)

elif func == "cos":

return math.cos(angle_radians)

elif func == "tan":

return math.tan(angle_radians)

else:

return "Invalid trigonometric function"

def logarithmic(self, base, value):

Perform logarithmic calculations.

if value > 0:

return math.log(value, base)

else:

return "Error: Logarithm undefined for non-positive values"

def exponential(self, value, power):

Perform exponential calculations (value^power).

return value ** power

# Main function to interact with the Al

def main():

calc = Scientific CalculatorAl()

while True:

print("\nScientific Calculator Al")

print("1. Basic Operations (Add, Subtract, Multiply, Divide)")

print("2. Trigonometry (sin, cos, tan)")

print("3. Logarithm")

print("4. Exponential (value^power)")

print("5. Exit")

choice = input("Select an option (1-5): ")

if choice == "1":

operation = input("Enter operation (add, subtract, multiply, divide): ").lower()

num1 = float(input("Enter the first number: "))

num2 = float(input("Enter the second number: "))

result = calc.basic_operations(operation, num1, num2)


print(f"Result: {result}")

elif choice == "2":

func = input("Enter the trigonometric function (sin, cos, tan): ").lower()

angle = float(input("Enter the angle in degrees: ")) result = calc.trigonometry(func, angle) print(f"Result: {result}")

elif choice == "3":

base = float(input("Enter the base of the logarithm: ")) value = float(input("Enter the value: ")) result = calc.logarithmic(base, value) print(f"Result: {result}")

elif choice == "4":

value = float(input("Enter the base value: "))

power = float(input("Enter the exponent: "))

result = calc.exponential (value, power)

print(f"Result: {result}")

elif choice == "5":

print("Exiting Scientific Calculator Al.")

break

else: print("Invalid choice. Try again.")

if_name__ == "__main__": main()
