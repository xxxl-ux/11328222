import random

def alien_attack():
    # 初始距離
    distance = 30

    # 回合數
    rounds = 0

    # 模擬每一回合
    while True:
        rounds += 1
        
        # 地球射退外星人的距離 (隨機1到6)
        earth_shoot = random.randint(1, 6)
        
        # 外星人前進的距離 (隨機1到6)
        alien_move = random.randint(1, 6)
        
        # 更新距離
        distance -= earth_shoot
        distance += alien_move
        
        # 顯示每回合的距離狀況
        print(f"Round {rounds}: Earth shoots {earth_shoot}, Alien moves {alien_move}, Distance = {distance}")
        
        # 判斷遊戲結束條件
        if distance >= 60:
            print("Earth wins! Distance exceeds 60.")
            break
        elif distance <= 0:
            print("Earth loses! Distance reaches 0.")
            break

# 開始遊戲
alien_attack()

