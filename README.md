# PYTHON.STR
Lista de Strings


-
'''Atividade 1'''

entrada1 = input("Digite a primeira String: ")

entrada2 = input("Digite a segunda String: ")

print(f"String 1: {entrada1}\nString 2: {entrada2}")
print(f"Tamanho da String '{entrada1}': {len(entrada1)} caracteres.")
print(f"Tamanho da String '{entrada2}': {len(entrada2)} caracteres.")

if (len(entrada1) != len(entrada2)):
    print("As duas Strings são de tamanhos diferentes")
else:
    print("As duas Strings são de tamanhos iguais")
if(entrada1 == entrada2):
    print("As duas Strings possuem o mesmo conteúdo.")
else:
    print("As duas Strings não possuem o mesmo conteúdo.")
'''Atividade 1'''
---

'''Atividade 2'''
entrada = input("Digite seu nome: ")
saida = []

for ctr in entrada:
    saida.append(ctr)
saida.reverse()

print(f"Seu nome ao contrário é {saida} ")
'''
'''
entrada = input("Digite seu nome: ")
entrada.split()
for item in entrada:
    print(item)
'''Atividade 1'''
'''Atividade 2'''
'''
entrada = input("Digite seu nome: ")
entrada.split()
saida = ""

for item in range(len(entrada)):
    saida += entrada[item]
    print(saida)
'''Atividade 2'''
------


'''Atividade 3'''
entrada = list(input("Digite seu nome: "))

for item in range(len(entrada),0,-1):
    print(entrada)
    entrada.pop()
'''Atividade 3'''
---

'''Atividade 4'''
meses = ['Janeiro','Fevereiro','Março','Abril','Maio','Junho','Julho','Agosto','Setembro','Outubro','Novembro','Dezembro']

entrada = input("Digite sua data de nascimento: ")
data = entrada.split('/')
dia = int(data[0])
mes = int(data[1])
ano = int(data[2])

print(f'Você nasceu em {dia} de {meses[mes-1]} de {ano}')
'''Atividade 4'''
----

'''Atividade 5'''
entrada = input("Digite uma frase: ")

saida_a = entrada.count('a')
saida_e = entrada.count('e')
saida_i = entrada.count('i')
saida_o = entrada.count('o')
saida_u = entrada.count('u')
saida_spc = entrada.count(' ')
soma_vg = saida_a + saida_e + saida_i + saida_o + saida_u

print(f"Existem {soma_vg} vogais.\n"
      f"{saida_a} letras 'a'.\n"
      f"{saida_e} letras 'e'.\n"
      f"{saida_i} letras 'i'.\n"
      f"{saida_o} letras 'o'.\n"
      f"{saida_u} letras 'u'.\n"
      f"{saida_spc} espaços. ")
'''Atividade 5'''
---


'''Atividade 6'''
entrada = input("Digite uma palavra: ")

for letra in entrada:
    if 2 > entrada.count(letra):
        print("Contem mais de 2 letras idênditcas")
    else:
        print("Não é palindromo")
'''Atividade 6'''
---

'''Atividade 7'''
entrada = input("Digite seu cpf: ")
cont = 3
cpf_sb1 = entrada.replace('.', '/')
cpf_sb2 = cpf_sb1.replace('-', '/')

for sequenc in cpf_sb2.split('/'):
    if(len(sequenc) > 2) and (len(sequenc) < 4):
        cont -= 1
    elif cont == 0 and len(sequenc) <= 2:
       print("CPF VÁLIDO")

    else:
        print("CPF INVÁLIDO! ")
'''Atividade 7'''
----

'''Atividade 8'''
import random
listaDePalavras = 'Bailarina','Futebol','Estátua','Pintor','Frio','Bebê','Mímico','Escova','Lápis','Livro','Astronauta','Amor','Ódio','Cego','Cadeira','Sacola','Professor','Médico','Calculadora','Artista','Vitória','Pescador','Internet','Basquete','Semente','Policial','Amargo','Bilhete','Xadrez','Banana','Micróbio','Romance','Carteira','Máquina','Prancha de surfe','Debate','Lixo','Sombra','Cadeado','Massagem'

cond = False
numPara = random.randint(0,39)
underlin = ''
palavraSoltas = []

print("!!!Bem vido ao jogo da forca!!!")

palavra = listaDePalavras[numPara] #Escolhe a palavra

for item in palavra:
    if item == ' ':
        underlin += ' '
    else:
        underlin += ' _ '

print(f'A palavra tem {type(len(palavra)-1)} letras')
print(f"A palavra é {underlin[len(underlin)-1]}")
print(palavra)
print(palavra[len(palavra)-1])

while(cond == False):

    entrada = input('Digite uma letra: ')
    print(len(resp))
'''Atividade 8'''
----

'''Atividade 9'''
print("Valida e corrige número de telefone!")
numeros = input("Telefone: ")
telefone_form = ""
cont = 0

for item in numeros:
    if cont == 0:
        telefone_form += "("
    if cont == 2:
        telefone_form += ")"
    if cont == 2 and item != "9":
        telefone_form += "9"
    if cont == 3:
        telefone_form += "-"
    if cont == 7:
        telefone_form += "-"

    cont += 1
    telefone_form += item

if len(numeros) < 12:
    print(f"O número possui {len(numeros)} dígitos. \nVou acrescentar o digito 3 na frente.")
    numeros += str(3)
    telefone_form += str(3)
    print(f"Telefone corrigido sem formatação: {numeros}")
    print(f"Telefone corrigido com formatação: {telefone_form}")
else:
    print(f"Telefone corrigido sem formatação: {numeros}")
    print(f"Telefone corrigido com formatação: {telefone_form}")

'''Atividade 10'''
