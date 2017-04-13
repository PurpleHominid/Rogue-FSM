# Rogue-FSM
A simple state machine as a rouge game

```
room=1
health=10


def room1():
    global room
    print ("\nYou are in room 1")
    print ("You can go through door A or door B")
    while True:
        door=input("Enter A to go through door A, or B to leave via door B: ")
        if door == "a" or door =="A":
            room=2
            
            break
        elif door == "b" or door == "B":
            room=3
            break


def room2():
    global room
    print ("\nYou are in room 2")
    print ("You can go through door A, B or door C")
    while True:
        door=input("Enter A to go through door A, B, or C to leave via door C: ")
        if door == "a" or door =="A":
            room=1
            break
        elif door == "b" or door == "B":
            room=5
            break
        elif door == "c" or door == "C":
            room=3
            break


def room3():
    global room
    print ("\nYou are in room 3")
    print ("You can go through door A, B,C, D or E")
    while True:
        door=input("Enter A to go through door A, B, C, D or E: ")
        if door == "a" or door =="A":
            room=1
            break
        elif door == "b" or door == "B":
            room=9
            break
        elif door == "c" or door == "C":
            room=7
            break
        elif door == "d" or door == "D":
            room=4
            break
        elif door == "e" or door == "E":
            room=2
            break
            

while health > 0:
    health=health-1

    if room==1:
        room1()
    elif room==2:
        room2()
    elif room==3:
        room3()


    print("\n\nYou have lost 1 health point, you have ", health, "left")


print("\nThe game has finished")

    
```
