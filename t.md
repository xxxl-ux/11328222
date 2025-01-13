import random

def alien_attack():
    
    distance = 30

    
    rounds = 0

    
    while True:
        rounds += 1
        
        
        earth_shoot = random.randint(1, 6)
        
        
        alien_move = random.randint(1, 6)
        
        
        distance -= earth_shoot
        distance += alien_move
        
        
        print(f"Round {rounds}: Earth shoots {earth_shoot}, Alien moves {alien_move}, Distance = {distance}")
        
        
        if distance >= 60:
            print("Earth wins! Distance exceeds 60.")
            break
        elif distance <= 0:
            print("Earth loses! Distance reaches 0.")
            break


alien_attack()

