(https://colab.research.google.com/drive/1AVE8F7Ic-rt4iHdyj3p2Q4pjxHX7s4jm?usp=sharing)
1. Calculate Average of numbers if a list is given
def calculate_average(numbers):
    if len(numbers) == 0:
        return 0
    return sum(numbers) / len(numbers)
numbers = [10, 20, 30, 40, 50]
average = calculate_average(numbers)
print(f"The average of the numbers is: {average}")
2. Search a number from a given list
def search_number(numbers, target):
    for number in numbers:
        if number == target:
            return True
    return False
numbers = [10, 20, 30, 40, 50]
target_number = 30

if search_number(numbers, target_number):
    print(f"{target_number} found in the list.")
else:
    print(f"{target_number} not found in the list.")
3.Search the largest from the list
def find_largest(numbers):
    if len(numbers) == 0:
        return None
    return max(numbers)
numbers = [10, 20, 30, 40, 50]
largest_number = find_largest(numbers)
print(f"The largest number in the list is: {largest_number}")
4. Search second smallest from the list
 def find_second_smallest(numbers):
  if len(numbers) < 2:
    return None
  unique_numbers = list(set(numbers))  # Remove duplicates
  unique_numbers.sort()
  if len(unique_numbers) < 2:
    return None
  return unique_numbers[1]

numbers = [10, 20, 30, 40, 50]
second_smallest = find_second_smallest(numbers)
print(f"The second smallest number in the list is: {second_smallest}")

numbers = [50,40,30,20,10]
second_smallest = find_second_smallest(numbers)
print(f"The second smallest number in the list is: {second_smallest}")

numbers = [10, 10, 10, 10]
second_smallest = find_second_smallest(numbers)
print(f"The second smallest number in the list is: {second_smallest}")

5.Ask user name and password from user and if same entry exist in file print valid username and if not print invalid username.
with open('credentials.txt', 'w') as file:
    file.write('javaria 12345\n')
    file.write('rida 0000\n')
    file.write('sawera 46535\n')
    file.write('isma 5674\n')

print("credentials.txt file created successfully!")
username = input("Enter username: ")
password = input("Enter password: ")
found = False
with open('credentials.txt', 'r') as file:
    for line in file:
        stored_username, stored_password = line.strip().split()
        if username == stored_username and password == stored_password:
            found = True
            break

if found:
    print("Valid username")
else:
    print("Invalid username")
#Slide #1

1. Calculate Average of numbers if a list is given

[ ]
def calculate_average(numbers):
    if len(numbers) == 0:
        return 0
    return sum(numbers) / len(numbers)

[ ]
numbers = [10, 20, 30, 40, 50]
average = calculate_average(numbers)
print(f"The average of the numbers is: {average}")

The average of the numbers is: 30.0
2. Search a number from a given list

[ ]
def search_number(numbers, target):
    for number in numbers:
        if number == target:
            return True
    return False

[ ]
numbers = [10, 20, 30, 40, 50]
target_number = 30

if search_number(numbers, target_number):
    print(f"{target_number} found in the list.")
else:
    print(f"{target_number} not found in the list.")
30 found in the list.
3.Search the largest from the list

[ ]
def find_largest(numbers):
    if len(numbers) == 0:
        return None
    return max(numbers)

[ ]
numbers = [10, 20, 30, 40, 50]
largest_number = find_largest(numbers)
print(f"The largest number in the list is: {largest_number}")

The largest number in the list is: 50
4. Search second smallest from the list

[ ]
 def find_second_smallest(numbers):
  if len(numbers) < 2:
    return None
  unique_numbers = list(set(numbers))  # Remove duplicates
  unique_numbers.sort()
  if len(unique_numbers) < 2:
    return None
  return unique_numbers[1]


[ ]

numbers = [10, 20, 30, 40, 50]
second_smallest = find_second_smallest(numbers)
print(f"The second smallest number in the list is: {second_smallest}")

numbers = [50,40,30,20,10]
second_smallest = find_second_smallest(numbers)
print(f"The second smallest number in the list is: {second_smallest}")

numbers = [10, 10, 10, 10]
second_smallest = find_second_smallest(numbers)
print(f"The second smallest number in the list is: {second_smallest}")

The second smallest number in the list is: 20
The second smallest number in the list is: 20
The second smallest number in the list is: None
Ask user name and password from user and if same entry exist in file print valid username and if not print invalid username.
Username and Password Verification

[ ]
with open('credentials.txt', 'w') as file:
    file.write('javaria 12345\n')
    file.write('rida 0000\n')
    file.write('sawera 46535\n')
    file.write('isma 5674\n')

print("credentials.txt file created successfully!")
credentials.txt file created successfully!

[ ]
username = input("Enter username: ")
password = input("Enter password: ")
found = False
with open('credentials.txt', 'r') as file:
    for line in file:
        stored_username, stored_password = line.strip().split()
        if username == stored_username and password == stored_password:
            found = True
            break

if found:
    print("Valid username")
else:
    print("Invalid username")
Enter username: javaria
Enter password: 12345
Valid username
Slide 2

Write a program to access the grade of a student by providing the name of the student.
students = {
    "Javaria": "A",
    "Isma": "B+",
    "Noor": "A+",
    "Fatima": "B",
    "Maliha": "A-"
}

name = input("Enter the name of the student: ")

if name in students:
    print(f"The grade for {name} is {students[name]}")
else:
    print(f"No record found for student named '{name}'.")
Q)Write a program in Python that combines the elements of two lists if they are not equal
A) 
list1 = [1, 2, 3, 4]
list2 = [3, 4, 5, 6]

combined_list = []

for item1 in list1:
    for item2 in list2:
        if item1 != item2:
            combined_list.append((item1, item2))

print("Combined elements (only if they are not equal):")
for pair in combined_list:
    print(pair)
Q)Write a Program that creates a list of squares upto to 10 numbers
squares = []
for number in range(1, 11):
    squares.append(number ** 2)
print("List of squares from 1 to 10:")
print(squares)


