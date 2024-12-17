# Variable-name
Checking the validity of a variable name in Python
import string
import keyword

user_input = input("Введіть ім'я змінної: ")

if user_input in keyword.kwlist or user_input[0].isdigit():
    print(False)
else:
    if (all(char.islower() or char.isdigit() or char == '_' for char in user_input) and
        user_input.count('_') <= 1):
        print(True)
    else:
        print(False)
