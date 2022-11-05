# Python_Program-
'''
This program is to validity the password. A password is valid only if it has:
Atleast 8 Characters
UpperCase Characters: A-Z
LowerCase Characters: a-z
Any of the Speacial Characters: @#$%^&+=
'''
# Python program to check validation of password 
 
import re 
password = input("Enter the password: ")
flag = True
while flag:   
    if (len(password)<8):
        print("Invalid Password: Length of the password must be of atleat 8 characters") 
        break
    elif not re.search("[A-Z]", password): 
        print("Invalid Password: Upper Case character is missing")
        break
    elif not re.search("[a-z]", password): 
        print("Invalid Password: Lower Case character is missing")      
        break
    elif not re.search("[0-9]", password):
        print("Invalid Password: Numerical character is missing") 
        break
    elif not re.search("[@#$%^&+=]", password):
        print("Invalid Password: Special character is missing") 
        break
    else: 
        print("Valid Password") 
        break
  
if flag == False: 
    print("Not a Valid Password") 
