"""

Break and Make (A Minecraft Parody)
@Author: Khanh Tran, Arun Chacko
@Credits: 'zigg' on stackoverflow
@Param: name
"""
#imports for color and slow type
from colorama import Fore, Style
import sys, time
from os import system

#function for text speed
def slow_type(t):
  for l in t:
    sys.stdout.write(l)
    sys.stdout.flush()
    time.sleep(1/50) 

#function to clear the screen after
def clear():
 _ = system('clear') 
  
#input for character's name 
def intro():
  try: 
    print()
    initial = str(input("What's your first " + Fore.LIGHTMAGENTA_EX + "INITIAL" + Style.RESET_ALL + "? "))
    print()
  except:
    print("Please insert a letter")
    intro()
  return initial

#first option
def start(): 
  clear()
  slow_type("Your name is " + names.capitalize() + "eve and you're dropped into an unfamiliar world. For now, just " + Fore.LIGHTMAGENTA_EX + "STAY ALIVE" + Style.RESET_ALL + ". Do you \n\n" +  "A. Explore\nB. Chop down a tree \n")
  firstChoice = input()
  if (firstChoice == 'A'):
    print()
    clear()
    explore()
  elif (firstChoice == 'B'):
    print()
    clear()
    getWood()
  else:
    print("I don't understand, please insert a valid choice\n")
    start()

#style.reset resets previous text's style before continuing 
def explore(): 
  slow_type("You chose to" + Fore.LIGHTMAGENTA_EX + " EXPLORE" + Style.RESET_ALL + ". You stumble upon a pathway leading in three directions. The pathway to the left leads to the" + Fore.CYAN + " Taiga" + Style.RESET_ALL + ", the one in the middle leads to the" + Fore.GREEN + " Jungle" + Style.RESET_ALL + ", and the one on the right leads to the" + Fore.YELLOW + " Desert" + Style.RESET_ALL + ".\n\nWhere should you go?\n")
  print(Fore.CYAN + "A.Taiga")
  print(Fore.GREEN + "B.Jungle")
  print(Fore.YELLOW + "C.Desert" + Style.RESET_ALL)
  
  biomeChoice = input()
  if (biomeChoice == "A"):
    print()
    print(Fore.CYAN + "You went to the Taiga, but froze to death.")
    print(Fore.RED + Style.BRIGHT + '***  YOU DIED  ***')
    print(Style.RESET_ALL)
    playAgain()
  elif (biomeChoice == "B"):
    clear()
    slow_type("You successfully traveled through the"+ Fore.GREEN + " Jungle. " + Style.RESET_ALL)
    sleep()
  elif (biomeChoice == "C"):
    print()
    print(Fore.LIGHTYELLOW_EX + "You traveled through the hot desert, but failed to find any water" + Fore.RED + Style.BRIGHT + "\n***  YOU DIED  ***")
    print(Style.RESET_ALL)
    playAgain()
  else:
    print("I don't understand, please insert a valid choice")
    explore()

#option for termination
def Zombie(): 
  slow_type("You chose not to " + Fore.LIGHTMAGENTA_EX + "SLEEP " + Style.RESET_ALL + "and continue exploring. It's nighttime and you encounter a Zombie. Will you\nA.Fight\nB.Run\n")
  runChoice = input()
  if (runChoice == 'A'):
    print("You chose to " + Fore.LIGHTMAGENTA_EX + "FIGHT " + Style.RESET_ALL + ", but you don't have anything to defend yourself with.")
    print(Fore.RED + Style.BRIGHT + "***  YOU DIED  ***" + Style.RESET_ALL)
    playAgain()
  elif (runChoice == 'B'):
    print()
    clear()
    cave()
  else:
    print("I don't understand, please insert a valid answer")
    Zombie()

#slowtype print statement --> separate input
def getWood():
  slow_type("You decided to " + Fore.LIGHTMAGENTA_EX + "GET WOOD " + Style.RESET_ALL + "but will you\nA. Craft\nB. Explore\n")  
  craftChoice = input()
  if (craftChoice == 'A'):
    print()
    clear()
    craft()
  elif (craftChoice == 'B'):
    print()
    clear()
    explore()
  else:
    print("I don't understand, please insert a valid answer")
    getWood()

#one of the first options
def craft():
  slow_type(Fore.GREEN + Style.BRIGHT + "       ACHIEVEMENT GET: PICKAXE        " + Style.RESET_ALL)
  slow_type("\nYou made a pickaxe! But it's getting dark... Should you\n\nA. Mine\nB. Settle Down\n")
  pickaxe=input()
  if (pickaxe == 'A'):
    print()
    clear()
    print("You went mining. ")
    cave()
  elif (pickaxe == 'B'):
    print()
    clear()
    sleep()

#only 'good' ending
def sleep():
  slow_type("As night falls, you begin to tire. Will you sleep?\nA. Yes\nB. No\n")
  sleepOption = input()
  if sleepOption == 'A':
    print("You slept and dreamed of what will happen tomorrow. It was sweet.\n")
    print(Fore.GREEN + "***  YOU WON  ***") #Insert win statement
    print(Style.RESET_ALL)
    playAgain()
  elif sleepOption == 'B':
    print()
    clear()
    Zombie()
  else:
    print("I don't understand")
    sleep()

#starts back at firstChoice
def playAgain():
  win=input("Play Again? ")
  if (win.lower() in yes): #.lower auto makes their statement into lowercase 
    print()
    start()
  elif (win.lower() in no):
    print()
    print("Alright, hope you had a fun time")
  else:
    print("I don't understand")
    playAgain()

#ends for user
def cave():
  slow_type("Fortunately, you found a cave, but as you wander blind, you hear a loud " + Fore.LIGHTGREEN_EX + "HISSING " + Style.RESET_ALL +  "behind you.\nA. Run\nB. Investigate\n")
  caveOption = input()
  if caveOption == "A":
    print("Fortunately, you managed to get away from the creeper, but while doing so you fell into a ravine and died.")
    print(Fore.RED + Style.BRIGHT + "***  YOU DIED  ***" + Style.RESET_ALL)
    playAgain()
  elif caveOption == "B":
    print("Turns out, it was a creeper and it blows up in your face.")
    print(Fore.RED + Style.BRIGHT + "***  a w w w w   m a n   ***" + Style.RESET_ALL) #best ending
    playAgain()

#if the user doesn't exactly put 'yes'
yes = ['yes','ye','ya','yah','si']
no = ['no','nope','nah','no thanks'] 
      
names = intro() #defines variable to function

start() #calls the function --> runs entire code 

