# Python_Assignments

Question 1:

With a given integral number n, write a program to generate a dictionary that contains (i, i x i) such that is an integral number between 1 and n (both included). and then the program should print the dictionary.
Suppose the following input is supplied to the program: 8
Then, the output should be:       {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64}

Code<>:

n = int(input("please enter a number between 1~10"))   
print({x: x*x for x in range(1, n+1)})


Question 2:

Write a program which accepts a sequence of comma-separated numbers from console and generate a list and a tuple which contains every number.Suppose the following input is supplied to the program:34,67,55,33,12,98
Then, the output should be:
                            ['34', '67', '55', '33', '12', '98']
                            ('34', '67', '55', '33', '12', '98')
Code<>:

lst1 = [(item) for item in input("Enter the list items : ").split(',')]
print(lst1)
print(tuple(lst1))
  

Question 3:

Create a list with 5 tuples. 
Each tuple should have the following elements ('Book Name', 'Published Year', 'Price'). 
Sort the list based on Price and Book Name

Code<>:    

my_list = [('python', '2010', 100),('Django', '2011', 120), ('Flask', '2012', 140),('Panda', '2013', 160), ('Web Development', '2008', 100)]
 
sorted_by_price = sorted(my_list, key=lambda list: list[2])
sorted_by_Name = sorted(my_list, key=lambda list: list[0])
print(sorted_by_price)
print(sorted_by_Name)

Question 4:

Define a class which has at least two methods:

getString: to get a string from console input
printString: to print the string in upper case.
Also please include simple test function to test the class methods.

Code<>:

class io():
    def __init__(self):
        self.s = ""
    def get_string(self):
        self.s = input('Enter a string:  ')
    def print_string(self):
        print(self.s.upper())
a = io()
a.get_string()
a.print_string()


Question 5:

Write a program that accepts a comma separated sequence of words as input and prints the words in a comma-separated sequence after sorting them alphabetically.

Input:  without,hello,bag,world
Output: bag,hello,without,world

Code<>:

item = sorted([x for x in input().split(',')])
print(','.join(item))

Question 6:

Write a program that accepts sequence of lines as input and prints the lines after making all characters in the sentence capitalized.

Suppose the following input is supplied to the program:
Hello world
Practice makes perfect

Then, the output should be:
HELLO WORLD
PRACTICE MAKES PERFECT

Code<>:

lines = []
while True:
    s = input()
    if s:
        lines.append(s.upper())
    else:
        break

for sentence in lines:
    print(sentence)
    
Question 2:

Write a program which accepts a sequence of comma separated 4 digit binary numbers as its input and then check whether they are divisible by 5 or not. The numbers that are divisible by 5 are to be printed in a comma separated sequence.

Example:

0100,0011,1010,1001
Then the output should be:
1010

Code<>:   
item = [int(x,2) for x in input().split(',')]
value = [i for i in item if i % 5 ==0]
for b in value:
    print(format(b,"b"))
