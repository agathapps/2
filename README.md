python
import random

def jogar():
    numero_secreto = random.randint(1, 10)
    tentativas = 0

    print("Bem-vindo ao jogo de adivinhação!")
    print("Estou pensando em um número entre 1 e 10. Tente adivinhar!")

    while True:
        try:
            palpite = int(input("Digite seu palpite: "))
        except ValueError:
            print("Por favor, digite um número válido.")
            continue

        tentativas += 1

        if palpite == numero_secreto:
            print(f"Parabéns! Você acertou em {tentativas} tentativas.")
            break
        elif palpite < numero_secreto:
            print("Tente um número maior.")
        else:
            print("Tente um número menor.")

    print("Obrigado por jogar!")

jogar()
