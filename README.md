# Spacescan-internship1
# Snake,Water,Gun

import random

list = ["s", "w", "g"]

chance = 10
no_of_chance = 0
human_point = 0
computer_point = 0

print("\t \t \t \t Snake,Water,Gun game ")
print("s for snake\nw for water\ng for gun")

# making the gama in while

while no_of_chance < chance:
    user_input = input("Snake ,Water,Gun : ")
    computer_input = random.choice(list)

    if user_input == computer_input:
        print("Tie Both 0 Point to Each \n ")

    # if user input is "s"
    elif user_input == "s" and computer_input == "g":
        computer_point = computer_point + 1
        print((f"your guess is {user_input} and computer_guess is {computer_input} \n"))
        print("computer wins 1 point \n ")
        print(f"your_point is {human_point} and computer_point is {computer_point} \n ")

    elif user_input == "s" and computer_input == "w":
        human_point = human_point + 1
        print((f"your guess is {user_input} and computer_guess is {computer_input} \n"))
        print("human wins 1 point \n ")
        print(f"your_point is {human_point} and computer_point is {computer_point} \n ")

    #if user input is "w"
    elif user_input == "w" and computer_input == "s":
        computer_point = computer_point + 1
        print((f"your guess is {user_input} and computer_guess is {computer_input} \n"))
        print("computer wins 1 point \n ")
        print(f"your_point is {human_point} and computer_point is {computer_point} \n ")

    #if user input is "g"
    elif user_input == "g" and computer_input == "s":
        human_point = human_point + 1
        print((f"your guess is {user_input} and computer_guess is {computer_input} \n"))
        print("human wins 1 point \n ")
        print(f"your_point is {human_point} and computer_point is {computer_point} \n ")

    else:
        print("you have input wrong \n ")

        no_of_chance = no_of_chance + 1
        print(f"{chance - no_of_chance} is left out of {chance} \n ")

    print("GAME OVER\n")
    if computer_point == human_point:
        print("Tie")

    elif computer_point > human_point:
        print("computer wins and you loose")

    else:
        print("you win and computer loose")

    print(f"your_point is {human_point} and computer_point is {computer_point}")

    no_of_chance = no_of_chance + 1
    print(f"{chance - no_of_chance} is left out of {chance} \n ")
    
