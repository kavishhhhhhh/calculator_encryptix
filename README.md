# calculator_encryptix
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Error: Division by zero is not allowed."

def calculator():
    while True:
        try:
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))

            print("Choose an operation:")
            print("1. Addition (+)")
            print("2. Subtraction (-)")
            print("3. Multiplication (*)")
            print("4. Division (/)")
            operation = input("Enter the operation (+, -, *, /): ")

            if operation == '+':
                result = add(num1, num2)
            elif operation == '-':
                result = subtract(num1, num2)
            elif operation == '*':
                result = multiply(num1, num2)
            elif operation == '/':
                result = divide(num1, num2)
            else:
                print("Invalid operation. Please try again.")
                continue

            print(f"The result is: {result}")

            another = input("Do you want to perform another calculation? (yes or no): ").lower()
            if another != 'yes':
                break
        except ValueError:
            print("Invalid input. Please enter numerical values.")

    print("Thanks for using the Calculator!")

calculator()
