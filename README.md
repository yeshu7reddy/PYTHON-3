# python 

##TIC-TAC-TOE

print("                                                 Welcome    machas     ")

print("             ")
print(" t1   t2  t3 ")
print("              ")
print(" m1   m2   m3 ")
print("              ")
print(" l1   l2   l3  ")



#make a dic to allocate the defined palce

game={'t1' : ' ','t2' : ' ', 't3': ' ',

      'm1' : ' ','m2' : ' ','m3' : ' ',

       'l1' : ' ','l2' : ' ','l3' : ' '

    }


player=1
tmoves=0
f_check = 0

def check():
    if game['t1']=='X' and game['t2']=='X' and game['t3']=='X':
        print("player 1 won the game")
        return 1
    if game['m1']=='X' and game['m2']=='X' and game['m3']=='X':
        print("player 1 won the game")
        return 1
    if game['l1']=='X' and game['l2']=='X' and game['l3']=='X':
        print("player 1 won the game")
        return 1
    if game['t1']=='X' and game['m2']=='X' and game['l3']=='X':
        print("player 1 won the game")
        return 1
    if game['t3']=='X' and game['m2']=='X' and game['l1']=='X':
        print("player 1 won the game")
        return 1
    if game['t1']=='X' and game['m1']=='X' and game['l1']=='X':
        print("player 1 won the game")
        return 1
    if game['t2']=='X' and game['m2']=='X' and game['l2']=='X':
        print("player 1 won the game")
        return 1
    if game['t3']=='X' and game['m3']=='X' and game['l3']=='X':
        print("player 1 won the game")
        return 1

    #for player 2
    if game['t1']=='O' and game['t2']=='O' and game['t3']=='O':
        print("player 2 won the game")
        return 1
    if game['m1']=='O' and game['m2']=='O' and game['m3']=='O':
        print("player 2 won the game")
        return 1
    if game['l1']=='O' and game['l2']=='O' and game['l3']=='O':
        print("player 2 won the game")
        return 1
    if game['t1']=='O' and game['m2']=='O' and game['l3']=='O':
        print("player 2 won the game")
        return 1
    if game['t3']=='O' and game['m2']=='o' and game['l1']=='O':
        print("player 2 won the game")
        return 1
    if game['t1']=='O' and game['m1']=='O' and game['l1']=='O':
        print("player 2 won the game")
        return 1
    if game['t2']=='O' and game['m2']=='o' and game['l2']=='O':
        print("player 2 won the game")
        return 1
    if game['t3']=='O' and game['m3']=='o' and game['l3']=='O':
        print("player 2 won the game")
        return 1
    #   if no one wins
    
        
    return 0
    

    
        
    


while True:
    #print(" --------------------------------------------------------")
    print("    " + game['t1'] + "     " + game['t2'] + "   " + game['t3'])
    print(" ")
    print("    " + game['m1'] + "     " + game['m2'] + "   " + game['m3'])
    print(" ")
    print("    " + game['l1'] + "     " + game['l2'] + "   " + game['l3'])
    #print#print(" --------------------------------------------------------")
    f_check=check()  # checking whether the game is completed or not
    if tmoves==9 :
        print("all places filled  - OR - game tied so restart the game")
        break
    if f_check==1:

        print("------The game is completedddd-------")
        break
    

    while True:
        
        if player==1:
            player1=input("player 1 : ")
            if player1 in game and game[player1] ==' ':
                game[player1]='X'
                player=2
                break
            else:
                print("macha this place is filled   or u entered wrong input")
                continue

        else:
            if player==2:
                player2=input("player 2 : ")
                if player2  in game and game[player2] ==' ':
                    game[player2]='O'
                    player=1
                    break
                else:
                    print("macha this place is filled or u entered wrong input")
                    continue
    
    tmoves+=1

