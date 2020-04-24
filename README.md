# Jogo-de-Tabuleiro---Alce-x-Caçador

Este script foi criado para simulação de um Jogo de Tabuleiro, composto por 12 espaços. 

O Jogador Alce iniciava na posição 7 e o Caçador na Posição 1.  

Condições para Vitória:  

O Alce seria vecendor se chegasse na posição 12 antes do adversário. O Caçador seria o vencedor se chegasse na mesma posição que o Alce ou chegasseno espaço 12 antes do adversário.


import random

#Declarando as Variaveis 
alce=7
cacador=1
x,cont=1,1

#Enquanto x for menor ou igual a 12, continua lançando o Dado
while x<=12:
    #Lança o Dado
    dado = random.randint(1,6)
    if(dado<=4):
        alce+=dado
        x+=alce
        cont+=1
    else:
        cacador+=dado
        x+=cacador
        cont+=1

if(cacador>=12 or cacador>=alce):
    print('Caçador Venceu!\nJogadas: '+str(cont))
elif(alce>=12):
    print('Alce Venceu!\nJogadas: '+str(cont))

