# MatchMaker_rb
# Riley Baert
# Matchmaker 1.00

#Constants 
INTRODUCTION = '''
--------------------------------
         Matchmaker 1.0
         Riley A. Baert
         CPSC-20000-003
--------------------------------
This program has been written to
determine if we are a good fit.
Please enter a value 1-5 indicating
how much you agree with the statement;
1 indicates that you do not agree at all,
5 indicates that you agree completely, etc.
Have fun! :)


'''
QUESTION = [
    'Dogs are better than cats',
    'I enjoy travelling and seeing new places',
    '18 percent is an acceptable tip to leave waitstaff for good service at a restaurant',
    'I could never go vegetarian--meat is too yummy!',
    'I am a very fast walker',
]

DESIRED_RESPONSE = [
    1, #strongly disagree
    5, #strongly agree
    3, #neutral
    2, #slightly disagree
    4, #slightly agree
]

MAX_SCORE = 5 * len(QUESTION)

print(INTRODUCTION)

response = []
compatability = []

userResponse1 = int(input(QUESTION[0]))
if userResponse1 in range (1,6):
    pass
else:
    print("Sorry! Please pick a numerical value between 1 and 5")
    userResponse1 = int(input(QUESTION[0]))
compatability1 = 5 - abs(userResponse1 - DESIRED_RESPONSE[0])
print("Question 1 compatability: " + str(compatability1))
print("")

userResponse2 = int(input(QUESTION[1]))
if userResponse2 in range (1,6):
    pass
else:
    print("Sorry! Please pick a numerical value between 1 and 5")
    userResponse2 = int(input(QUESTION[1]))
compatability2 = 5 - abs(userResponse2 - DESIRED_RESPONSE[1])
print("Question 2 compatability: " + str(compatability2))
print("")

userResponse3 = int(input(QUESTION[2]))
if userResponse3 in range (1,6):
    pass
else:
    print("Sorry! Please pick a numerical value between 1 and 5")
    userResponse2 = int(input(QUESTION[2]))
compatability3 = 5 - abs(userResponse3 - DESIRED_RESPONSE[2])
print("Question 3 compatability: " + str(compatability3))
print("")

userResponse4 = int(input(QUESTION[3]))
if userResponse4 in range (1,6):
    pass
else:
    print("Sorry! Please pick a numerical value between 1 and 5")
    userResponse2 = int(input(QUESTION[3]))
compatability4 = 5 - abs(userResponse4 - DESIRED_RESPONSE[3])
print("Question 4 compatability: " + str(compatability4))
print("")

userResponse5 = int(input(QUESTION[4]))
if userResponse5 in range (1,6):
    pass
else:
    print("Sorry! Please pick a numerical value between 1 and 5")
    userResponse2 = int(input(QUESTION[4]))
compatability5 = 5 - abs(userResponse5 - DESIRED_RESPONSE[4])
print("Question 5 compatability: " + str(compatability5))
print("")


totalCompatability = (compatability1 + compatability2 + compatability3 + compatability4 + compatability5) * 4
print("Total Compatability: " + str(totalCompatability))
print("")

if totalCompatability in range(90,101):
    print("Wow! I hope you're open to the idea of a destination wedding!")
if totalCompatability in range (80, 90):
    print("Let's go on a date... only if you promise to tip the waitstaff 20% :)")
if totalCompatability in range (70,80):
    print("Meh. Not too impressed, but i'll give you a second chance.")
if totalCompatability <70:
    print("It's not me, its you. Try someone else.")
