def simple_calculator():
    """Performs basic arithmetic operations based on user input."""

    while True:
        try:
            Input1 = float(input("Enter the first number: "))
            Input2 = float(input("Enter the second number: "))
            operation = input("Enter the operation (#Addition'+', #Substraction'-', #Multiplaction'*', #Divide'/'): ")

            if operation == "+":
                result = Input1 + Input2
            elif operation == "-":
                result = Input1 - Input2
            elif operation == "*":
            
                result = Input1 * Input2
            elif operation == "/":
                if Input2 == 0:
                    raise ZeroDivisionError("Cannot divide by zero")
                result = Input1 / Input2
            else:
                print("Invalid operation. Please try again.")
                continue

            print(f"The result is: {result}")
            break

        except ValueError:
            print("Invalid input. Please enter numbers only.")

if __name__ == "__main__":
    simple_calculator()
