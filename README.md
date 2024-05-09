# 3.Write a program that takes a string as input and counts the occurrences of
each word in the string.
Code :
def count_word_occurrences(input_string):
words = input_string.split()
word_counts = {}
for word in words:
word = word.strip(",.?!;:\"")
word = word.lower()
if word in word_counts:
word_counts[word] += 1
else:
word_counts[word] = 1
return word_counts
input_string = input("Enter a string: ")
word_occurrences = count_word_occurrences(input_string)
print("Occurrences of each word:")
for word, count in word_occurrences.items():
print(f"{word}: {count}")




#...........................................................

6. Write a Python program to calculate and print the number of key-value pairs in a
given dictionary.
Code :
def count_key_value_pairs(dictionary):
num_pairs = len(dictionary)
return num_pairs
my_dict = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
result = count_key_value_pairs(my_dict)
print("Number of key-value pairs in the dictionary:", result)


#...........................................................


7. Write a Python program that takes a password as input and checks if it meets
the following criteria: at least 8 characters long, contains both uppercase and
lowercase letters, and has at least one digit. If the password is valid, print
“Password accepted.” If not, use `continue` to prompt the user to enter a valid
password.
Code :
def is_valid_password(password):
if len(password) < 8:
return False
has_upper = any(char.isupper() for char in password)
has_lower = any(char.islower() for char in password)
if not (has_upper and has_lower):
return False
has_digit = any(char.isdigit() for char in password)
if not has_digit:
return False
return True
while True:
password = input("Enter a password: ")
if is_valid_password(password):
print("Password accepted.")
break
else:
print("Invalid password. Please make sure your password is at least 8 characters long,
contains both uppercase and lowercase letters, and has at least one digit.")
continue


#...........................................................


8. Write a Python function called `even_or_odd` that takes an integer as input and
returns “Even” if the number is even and “Odd” if the number is odd.
Code :
def even_or_odd(number):
if number % 2 == 0:
return "Even"
else:
return "Odd"
num = int(input("Enter a number: "))
result = even_or_odd(num)
print("The number is:", result)







