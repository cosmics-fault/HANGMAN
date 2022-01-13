# HANGMAN
FINDING HEROINE'S NAME
from random import*
from IPython.display import clear_output
words=["nayanthara","trisha","shreyasaran","malavikamohan","asin","priyankamohan"]
word=choice(words)
guessed,lives,game_over=[],7,False
guesses=["_"]*len(word)
while not game_over:
    hidden_word="".join(guesses)
    print("WORD TO GUESS:{}".format(hidden_word))
    print("YOU HAVE {} LIVES".format(lives))
    ans=input("TYPE QUIT OR GUESS THE HEROINE NAME:")
    if ans=="QUIT":
        print("THANKS FOR PLAYING")
        game_over=True
    elif ans in word:
        print("YOU GUESSED IT RIGHT")
    else:
        lives-=1 
        print("INCORRECT YOU LOST A LIFE,TRY AGAIN")
        if lives<=0:
            print("YOU HAVE LOST ALL YOUR LIVES,YOU LOST")
            game_over=True
            
