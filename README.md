import random
#Generates 28 dominoe variations
class CDominoes:
    def __init__(self):
        self.dominoes = []
        self.createDominoes()

    def createDominoes(self):
        for i in range(7):
            for j in range(i, 7):
                self.dominoes.append((i,j))
    
    
    def get_dominoes(self):
        return self.dominoes

#Randomizes the domino list
class CRandom:
    def mix(dominoes):    
        random.shuffle(dominoes)
        return dominoes
    
#Displays domino pieces in current order
class CTable:
    def display_dominoes(self, dominoes):
        print("Dominoes on the table:")
        for piece in dominoes:
            print(f"{piece[0]}|{piece[1]}", end=' ')
        print("\n")

#Initializes a player with a random set of dominoes
class CPlayer:
    def _init_(self, name):
        self.name = name
        self.hand = []

    def pick_dominoes(self, dominoes, count):
        self.hand = random.sample(dominoes, count)
        print(f"{self.name} picked {count} pieces.")

    def show_hand(self):
        print(f"{self.name}'s hand:")
        for piece in self.hand:
            print(f"{piece[0]}|{piece[1]}", end=' ')
        print("\n")
