# Rock-Paper-Scissor
Rock-Paper-Scissor game for one Player vs Computer in Python.

## Enjoy Coding 😊

```python

import random

def Menu():
    print("\n\n\t\t\t\t\tEnter 1 for Rock.")
    print("\t\t\t\t\tEnter 2 for Paper.")
    print("\t\t\t\t\tEnter 3 for Scissor.")
    num = int(input("\n\t\t\t\t\tEnter Your Choice : "))
    return num

def test(num):
    if num == 1:
        return "Rock"
    elif num == 2:
        return "Paper"
    else:
        return "Scissor"

def check(num, comp):
    if num == comp:
        print("\n\n\t\t\t\t\tGame Tie...")
    elif (num == 1 and comp == 2) or (num == 2 and comp == 3) or (num == 3 and comp == 1):
        print("\n\n\t\t\t\t\tComputer Win...")
    else:
        print("\n\n\t\t\t\t\tYou Win...")

def start():
    cond = 1
    while cond == 1:
        print("\033[H\033[J")
        print("\n\n\t\t\t\t\t************************************")
        print("\t\t\t\t\t| Rock-Paper-Scissor By PK Singhal |")
        print("\t\t\t\t\t************************************")
        choice = Menu()
        if choice < 1 or choice > 3:
            print("\n\t\t\t\t\tInvalid Choice...")
        else:
            comp = random.randint(1, 3)
            com = test(comp)
            player = test(choice)
            print("\n\t\t\t\t\tYou      : ",player)
            print("\t\t\t\t\tComputer : ",com)
            check(choice, comp)
        cond = int(input("\n\n\n\t\t\t\t\tEnter 1 to continue & 0 to exit... "))
        
start():
print("\033[H\033[J")

```
