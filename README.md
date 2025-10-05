
''' Snake, Water and Gun Game (Pyhton)
     Chaitanya Mangla '''

''' Rules of the game:
    1. Sanke drinks water (snake > water)
    2. Gun kills snake  (gun > snake)
    3. Gun drowns in water (water > gun) 
    '''
'''1 for snake
   -1 for water
    0 for gun 
    '''
import random # Import random library to allow computer operating system for making choices

computer =  random.choice([-1,0,1])
youstr = input ("Enter your choice ")
youDict = {"s": 1, "w" : -1, "g" : 0}
reverseDict = {1: "Snake", -1: "Water" , 0: "Gun"}
you = youDict[youstr]

# Here, we have 2 number variables, you and computer 

print(f"You chose {reverseDict[you]}\nComputer chose {reverseDict[computer]}")

if (computer == you):
    print("Its a draw")

else:  # This is a perfect example of nested if else statement 
    if(computer == -1 and you == 1):
        print("You Win\nCongratulations!!")
    
    elif(computer == -1 and you == 0):
        print("You Lose\nBetter Luck next time!!")
    
    elif(computer == 1 and you == 0):
        print("You Win\nCongratulations!!")
    
    elif(computer == 1 and you == -1):
        print("You Lose\nBetter Luck next time!!")
    
    elif(computer == 0 and you == -1):
        print("You Win\nCongratulations!!")
    
    elif(computer == 0 and you == 1):
        print("You Lose\nBetter Luck next time!!")

    else:
        print("Something went wrong")

