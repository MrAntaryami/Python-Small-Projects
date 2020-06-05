# Python-Small-Projects (STONE-PAPER-SCISSOR GAME IN PYTHON)
import random
import time
import os
words = ["Stone","Paper","Scissor"]
ch='Y'
while ch == 'Y' or ch == 'y' :
 draw=0
 your_score = 0
 comp_score = 0
 interval = 10
 while interval > 0 :
  print("1-Stone")
  print("2-Paper")
  print("3-Scissor")
  i = random.uniform(0,0.56)
  time.sleep(i)
  index = random.randint(0,len(words)-1)
  guess = words[int(input("Make a Guess:(1/2/3)... "))-1]
  print(f"You Choose :{guess}")
  print(f"Computer Choose :{words[index]}")
  if guess == "Stone" :
    if index == 0   :
      print("Draw")
      draw+=1
    elif index == 1 :
      print("Computer Got that!")
      comp_score += 1
    else :
      print("You Got that!")
      your_score += 1
  if guess == "Paper" :
    if index == 1   :
      print("Draw")
      draw+=1
    elif index == 2 :
      print("Computer Got that!")
      comp_score += 1
    else :
      print("You Got that!")
      your_score += 1
  if guess == "Scissor" :
    if index == 2   :
      print("Draw")
      draw+=1
    elif index == 1 :
      print("Computer Got that!")
      comp_score += 1
    else :
      print("You Got that!")
      your_score += 1
  print(f"\n\n\tYour Score :{your_score}",end="  ")
  print(f"computer Score :{comp_score}",end="  ")
  print(f"Draws :{draw}")
  interval -= 1
 if your_score > comp_score :
   print("\n\n\tYou Won!!")
 elif your_score < comp_score :
   print("\n\n\tComputer Won!!")
 else :
   print("\n\n\tGame Draw")
 ch = input("Wanna Play Again :(Y/y) or (N/n)..")
 if ch == 'N' or ch == 'n' :
   break;
