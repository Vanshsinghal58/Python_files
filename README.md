import random
import string

def generate_password(length):
    
    characters = string.ascii_letters + string.digits + string.punctuation
    
    
    password = ''.join(random.choice(characters) for _ in range(length))
    
    return password


try:
    length = int(input("Enter desired password length: "))
    if length <= 0:
        print("Please enter a positive number.")
    else:
        password = generate_password(length)
        print("\nGenerated Password:", password)
except ValueError:
    print("Invalid input! Please enter a number.")
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))


print("\nSelect Operation:")
print("1. Addition (+)")
print("2. Subtraction (-)")
print("3. Multiplication (*)")
print("4. Division (/)")


choice = input("\nEnter your choice (1/2/3/4): 

if choice == '1':
    result = num1 + num2
    print(f"\nResult: {num1} + {num2} = {result}")
elif choice == '2':
    result = num1 - num2
    print(f"\nResult: {num1} - {num2} = {result}")
elif choice == '3':
    result = num1 * num2
    print(f"\nResult: {num1} × {num2} = {result}")
elif choice == '4':
    if num2 != 0:
        result = num1 / num2
        print(f"\nResult: {num1} ÷ {num2} = {result}")
    else:
        print("\nError: Division by zero is not allowed!")
else:
    print("\nInvalid choice! Please select from 1 to 4.")
