# Rock-paper-scissor-game
import random
l1=["rock","scissors","paper"]
'''
rock vs paper->paper wins
paper vs scissors->scissors wins
rock vs scissors->rock wins
'''

while True :
    ccount=0
    ucount=0
    uc=int(input('''
1.Game Start
2.No | Exit
    
    '''))
    if uc==1:
        for a in range(1,6):
            userInput=int(input('''
1.Rock
2.Scissors
3.Paper
            
            '''))
            if userInput==1:
                  uchoice="rock"
            elif userInput==2:
                  uchoice="scissors"
            elif userInput==3:
                  uchoice = "paper"
            Cchoice=random.choice(l1)
            if Cchoice==uchoice:
                print("Computer Value",Cchoice)
                print("User Value", uchoice)
                print("Game Draw")
                ucount=ucount+1
                ccount=ccount+1
            elif(uchoice=="rock" and Cchoice=="scissors") or (uchoice=="paper" and Cchoice=="rock") or (uchoice=="scissors" and Cchoice=="paper"):
                print("Computer Value", Cchoice)
                print("User Value", uchoice)
                print("you win")
                ucount=ucount+1
            else:
               print("Computer Value", Cchoice)
               print("User Value", uchoice)
               print("Computer Win")
               ccount=ccount+1

        if ucount == ccount:
            print("Final game draw....")
            print("User Score", ucount)
            print("Computer Score", ccount)
        elif ucount > ccount:
            print("Final You Win the game...")
            print("User Score", ucount)
            print("Computer Score", ccount)
        else:
            print("Final Computer win the game...")
            print("User Score", ucount)
            print("Computer Score", ccount)


    else:
       break




