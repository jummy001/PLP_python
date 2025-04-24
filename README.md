# PLP_python
assignment
def get_number(prompt):
    while True:
        try:
            return float(input(prompt))
        except ValueError:
            print("That's not a valid number. Please try again.")

def get_operation(prompt):
    valid_ops = {"+", "-", "*", "/"}
    while True:
        op = input(prompt).strip()
        if op in valid_ops:
            return op
        print(f"Invalid operation. Choose one of {', '.join(valid_ops)}.")

def calculate(a, b, op):
    if op == "+":
        return a + b
    elif op == "-":
        return a - b
    elif op == "*":
        return a * b
    elif op == "/":
        if b == 0:
            return None
        return a / b

def main():
    print("### Basic Python Calculator ###")
    num1 = get_number("Enter the first number: ")
    num2 = get_number("Enter the second number: ")
    op   = get_operation("Enter an operation (+, -, *, /): ")

    result = calculate(num1, num2, op)
    if result is None:
        print("Error: Division by zero is undefined.")
    else:
        # Format to drop .0 for integer results
        formatted = int(result) if result.is_integer() else result
        print(f"{num1} {op} {num2} = {formatted}")

if __name__ == "__main__":
    main()
PS C:\Users\TOSHIBA\Desktop\Python_Module> & C:/Users/TOSHIBA/AppData/Local/Programs/Python/Python313/python.exe c:/Users/TOSHIBA/Desktop/Python_Module/greetings.py
### Basic Python Calculator ###
Enter the first number: 10
Enter the second number: 5
Enter an operation (+, -, *, /): +
10.0 + 5.0 = 15
PS C:\Users\TOSHIBA\Desktop\Python_Module> 

