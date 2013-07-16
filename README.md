Guess a number
====================
import random

print "Guess the number!"

anum = random.randrange(255)

def generate():
    global anum
    anum = random.randrange(255)
    

def test():
    # the number below is our input.
    guess = input("Please type a number: ")
    
    if guess==anum:
        print "You guessed correctly. The number is " + str(anum)
        tryagain = raw_input("Would you like to try again (y/n)? ").lower()
        if (tryagain=='y'):
            generate()
            print "New number generated!"
            test()
        else:
            print "Thank you for playing!"
    else:
        if guess<anum:
            print "A little higher maybe..."
            test()
        if guess>anum:
            print "A little lower maybe..."
            test()

test() 
