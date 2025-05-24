logica_super_trunfo.py

import random

class Carta: def init(self, nome, forca, inteligencia, velocidade): self.nome = nome self.forca = forca self.inteligencia = inteligencia self.velocidade = velocidade

def _str_(self):
    return f"{self.nome} | Força: {self.forca} | Inteligência: {self.inteligencia} | Velocidade: {self.velocidade}"

class JogoSuperTrunfo: def init(self): self.cartas = self.criar_cartas() random.shuffle(self.cartas)

def criar_cartas(self):
    return [
        Carta("Leão", 90, 40, 60),
        Carta("Águia", 50, 70, 80),
        Carta("Tubarão", 85, 45, 70),
        Carta("Gato", 40, 60, 90),
        Carta("Elefante", 80, 60, 30)
    ]

def jogar(self):
    carta_jogador = random.choice(self.cartas)
    carta_computador = random.choice(self.cartas)

    print("Sua carta:")
    print(carta_jogador)
    print("\nCarta do computador:")
    print(carta_computador)

    atributo = input("Escolha o atributo para comparar (forca/inteligencia/velocidade): ").lower()

    valor_jogador = getattr(carta_jogador, atributo, None)
    valor_computador = getattr(carta_computador, atributo, None)

    if valor_jogador is None:
        print("Atributo inválido!")
        return

    print(f"\nVocê: {valor_jogador} vs Computador: {valor_computador}")
    if valor_jogador > valor_computador:
        print("Você venceu!")
    elif valor_jogador < valor_computador:
        print("Você perdeu.")
    else:
        print("Empate!")

if name == "main": jogo = JogoSuperTrunfo() jogo.jogar()
