# stone-paper-scissor.game

'''
1 for Stone, 
-1 for paper,
0 for scissors,
'''

import random  #to make the computer make any random choices

computer = random.choice([-1, 0, 1])
youstr = input("Enter your choice: ") # s or p or c
youDict = {"s": 1, "p": -1, "c": 0} # for easy lookup
reverseDict = {1: "Stone", -1: "paper", 0: "scissor"} #naming  the choices for easy understanding
you = youDict[youstr] # converting string input  to integer


print(f"You chose {reverseDict[you]}\nComputer chose {reverseDict[computer]}")
# Logic for determining winner/loser based on the rules of the game:
if(computer == you):
    print("It's a tie!")

else:
    if(computer == -1 and you == 1):
        print("You Lose!")
    
    elif (computer == -1 and you == 0):
        print("You Win!")

    elif (computer == 1 and you == -1):
        print("You Win!")

    elif (computer == 1 and you == 0):
        print("You Lose!")

    elif (computer == 0 and you == 1):
        print("You Win!")

    elif (computer == 0 and you == -1):
        print("You Lose!")

    else:
        print("something went wrong!") #just in case the program runs into an unexpected situation
