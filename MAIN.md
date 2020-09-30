# Rock-Paper-Scissors-Game-in-Python

	from random import randint

	game_list = ['Rock', 'Paper', 'Scissors']

	def player_input():
    selection = ' '
    while selection not in game_list:
    selection = input('Please Enter Choice. -Paper-Rock-Scissors ').capitalize()
    return selection
    

  	def comp_selection():
    rand = randint(0,2)
    comp_selection = game_list[rand]
    return comp_selection
    
    
    def decide_winner(InputFromPlayer,SelectionFromCompurt):
    #Player
    if(InputFromPlayer == 'Rock' and SelectionFromCompurt == 'Scissors'):
        print('Player won')
    elif(InputFromPlayer == 'Paper' and SelectionFromCompurt == 'Rock'):
        print('Player won')
    elif(InputFromPlayer == 'Scissors' and SelectionFromCompurt == 'paper'):
        print('Player won')
    #Comp
    elif(InputFromPlayer == 'Scissors' and SelectionFromCompurt == 'Rock'):
        print('Computer won')
    elif(InputFromPlayer == 'Rock' and SelectionFromCompurt == 'Paper'):
        print('Computer won')
    elif(InputFromPlayer == 'Paper' and SelectionFromCompurt == 'Scissors'):
        print('Computer won')
    else:
        print('TIE')
        
    
    print("Let's start the game :)")
    
    Player = player_input()
    
    print(f'Player selected {Player}')
    
    Comp = comp_selection()
    
    print(f'Computer selected {Comp}')
    
    decide_winner(Player,Comp)
