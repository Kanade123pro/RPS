TASK 4

import random
print("........Welcome to RPS........")
user_score=0
comp_score=0
ties=0
name=input("Enter your name here:")
print("""
Winning Rules:
1.paper vs rock-->pper
2.Rock vs Scissors-->Rock
3.Scissors vs paper-->Scissors""")
print()
while True:
    print("""Choices are:
    1.Rock
    2.paper
    3.Scissors""")
    choice=int(input("enter your choice from 1-3:"))
    print()
    while choice>3 or choice<1:
        choice=int(input("enter valid input"))
    if choice==1:
        user_choice="Rock"
    elif choice==2:
        user_choice="paper"
    else:
        user_choice="Scissors"
    print("The User's choice is",user_choice)
    print("Now it is computer turn")
    computer=random.randint(1,3)
    if computer==1:
        comp_choice="Rock"
    elif computer==2:
        comp_choice="paper"
    else:
        comp_choice="Scissors"
    print("The computer choice is",comp_choice)
    if((user_choice=="paper" and  comp_choice=="Rock") or (user_choice=="Rock" and  comp_choice=="paper")):
        print("paper wins")
        result="paper"
    elif((user_choice=="scissors" and comp_choice=="Rock") or (user_choice=="Rock" and comp_choice=="Scissors")):
        print("Rock wins")
        result="Rock"
    elif(user_choice==comp_choice):
        print("it is a tie")
        result="Tie"
    else:
        print("Scissors wins")
        result="Scissors"
    if result == "Tie":
        ties+=1
    elif result == user_choice:
        print("user wins")
        user_choice +=1
    else:
        print("computer wins")
        comp_choice+=1
    print("Score are")
    print(name,"'s score is",user_score)
    print("computer's score is",comp_score)
    print("ties are",ties)
    repeat = input("do you want to play again?")
    if repeat=="No" or repeat=="NO":
        break

    print("Game over!")
    print('Thanks for playing!!!')
