# Создайте класс Касса, который хранит текущее количество денег в кассе, у него есть методы:      top_up(X) - пополнить на X     count_1000() - выводит сколько целых тысяч осталось в кассе     take_away(X) - забрать X из кассы, либо выкинуть ошибку, что не достаточно денег
# Решение:
class Cashbox:
    def __init__(self, money):
        self.money = money
 
    def top_up(self, x):
        self.money += x
 
    def count_1000(self):
        return self.money // 1000
 
    def take_away(self, x):
        if x <= self.money:
            self.money -= x
        else:
            raise ValueError('Not enough money')
