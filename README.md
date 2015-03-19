# projeto-1# -*- coding: utf-8 -*-
from random import choice
opc = ["pedra", "papel", "tesoura", "lagarto", "spock"]
pedra = "pedra"   
papel = "papel"
tesoura = "tesoura"
lagarto = "lagarto"
spock = "spock"
denovo = "sim"
while denovo == "sim":
    comp = 0
    jog = 0
    while comp<3 and jog<3:
        opc = ["pedra", "papel", "tesoura", "lagarto", "spock"]
        print ("O placar está: comutador %d x jogador %d" %(comp, jog))
        computer = choice (opc)
        jogador = str(input("pedra, papel, tesoura, lagarto ou spock?"))
        while jogador not in opc:
            print ("Você digitou errado! Tente mais uma vez")
            jogador = str(input("pedra, papel, tesoura, lagarto ou spock?"))
        if computer == tesoura:
            if jogador == papel or jogador == lagarto:
                print("Computador ganhou")
                print("O computador escolheu:", computer)
                comp = comp + 1 
            elif jogador != computer:
                print ("Jogador ganhou")
                print("O computador escolheu:", computer)
                jog = jog + 1
        if computer == papel:
            if jogador == pedra or jogador == spock:
                print ("Computador ganhou")
                print("O computador escolheu:", computer)
                comp = comp + 1 
            elif jogador != computer:
                print ("Jogador ganhou")
                print("O computador escolheu:", computer)
                jog = jog + 1
        if computer == pedra:
            if jogador == lagarto or jogador == tesoura:
                print ("Computador ganhou")
                print("O computador escolheu:", computer)
                comp = comp + 1 
            elif jogador != computer:
                print ("Jogador ganhou")
                print("O computador escolheu:", computer)
                jog = jog + 1
        if computer == lagarto:
            if jogador == spock or jogador == papel:
                print ("Computador ganhou")
                print("O computador escolheu:", computer)
                comp = comp + 1 
            elif jogador != computer:
                print ("Jogador ganhou")
                print("O computador escolheu:", computer)
                jog = jog + 1
        if computer == spock:
            if jogador == tesoura or jogador == pedra:
                print ("Computador ganhou")
                print("O computador escolheu:", computer)
                comp = comp + 1 
            elif jogador != computer:
                print ("Jogador ganhou")
                print("O computador escolheu:", computer)
                jog = jog + 1
        if computer == jogador:
            print ("Deu empate")
    if comp > jog:
        print ("O jogo acabou.\n O computador ganhou!")
    else:
        print ("O jogo acabou. \n O jogador ganhou!")
    denovo = input("Quer jogar mais uma vez?")
print ("Obrigada por jogar")
