# Python_calc_multipleoperations
import re


def add(number):
    s = int(number[0])+int(number[1])
    number.append(number.pop(0))
    return s


def subtract(number):
    s = int(number[0])-int(number[1])
    number.append(number.pop(0))
    return s


def multiply(number):
    s = int(number[0])*int(number[1])
    number.append(number.pop(0))
    return s


def divide(number):
    s = int(number[0])/int(number[1])
    number.append(number.pop(0))
    return s


calculation = input("Type your calculation")
numbers = re.findall(r'\d+', calculation)
print(numbers)
ans = 0

for x in calculation:
    if x == "+":
        ans = ans + add(numbers)

    elif x == "-":
        ans = ans + subtract(numbers)

    elif x == "*":
        ans = ans + multiply(numbers)

    elif x == "/":
        ans = ans + divide(numbers)

    else:
         print("scanning...")

print(ans)
