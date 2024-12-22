# calculator
# Its just a calculator in python

def display_menu():
    print("Select operation")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiplay")
    print("4. Divide")
    print("5. Exit")

    choice = input("Enter choice (1/2/3/4/5): ")

    return choice


def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiplay(x, y):
    return x * y

def divide(x, y):
    return x / y

def calculator():
    while True:
        choice = display_menu()

        if choice == "5":
            print("Exiting..")
            break

        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))

        if choice == "1":
            print(num1, "+", num2, "=", add(num1, num2))

        elif choice == "2":
            print(num1, "-", num2, "=", subtract(num1, num2))

        elif choice == "3":
            print(num1, "*", num2, "=", multiplay(num1, num2))

        elif choice == "4":
            if num2 == 0:
                print("Error: cannot be divide by zero")
            else:
                print(num1, "/", num2, "=", divide(num1, num2))
        
        else:
            print("Invalid input.")

        



if __name__ == "__main__":
    calculator()

