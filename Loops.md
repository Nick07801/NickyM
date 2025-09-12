# Nível iniciante 
'''1: Imprimir uma mensagem 5 vezes'''
frase = ("Olá Mundo!")

for _ in range (5):
    print(frase)


'''2: Contar de 1 a 10'''
contador = 1

while contador <= 10:
    print (contador)
    contador += 1


'''3:  Percorrer uma lista de frutas'''
frutas = ["banana", "uva", "laranja", "manga"]

for fruta in frutas:
    print (fruta)


'''4: Verificar se um número está em uma lista'''
numeros = [0, 1, 2, 3, 4, 5, 9]
numero_procurado = int(input("Digite um número:"))

encontrado = False
for numero in numeros:
    if numero == numero_procurado:
        encontrado = True
        break

if encontrado:
    print(f"{numero_procurado} está na lista!")
else:
    print(f"{numero_procurado} não está na lista.")


'''5: Somar os elementos de uma lista'''
numeros = [3, 7, 8, 9]
soma = 0

for numero in numeros:
    soma += numero
    print (f"o resultado é: {soma}")


#Nível Intermediário


'''6: Filtrar números pares de uma lista '''
lista = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

for numero in lista:
    if numero % 2 == 0:
        print (numero)


'''7: Modificar elementos de uma lista'''
valor = [100, 250, 80, 150, 60]

for numero in range(len(valor)):
    valor[numero] = valor[numero] * 0.9  

print(f"Preços com 10% de desconto:{valor}")


'''8: Iterar sobre um dicionário e imprimir chave e valor'''
pessoa = {"nome": "Marcela", "idade":30, "cidade": "itapecerica"}

for chave, valor in pessoa.items():
    print (f"{chave} -> {valor}" )


'''9: Iterar sobre um dicionário e imprimir chave e valor'''
numeros = [10, 20, 70, 66, 54, 15, 22, 34]

for numero in numeros:
    if numero > 50:
        print (f"números maiores que cinquenta: {numero}")


# Nível Desafio


'''10: Simular um caixa eletrônico'''
saldo = 3000

while True:
    entrada = (input("Digite o valor do saque ou 'sair' para encerrar"))

    if entrada.lower() == "sair":
        print ("Encerrar caixa eletrônico")
        break

    valor_saque = float(entrada)
    if valor_saque <= saldo:
        saldo -= valor_saque
        print(f"Saque de {valor_saque:.2f} realizado com sucesso.")
        print(f"Saldo restante: {saldo:.2f}")
    else:
        print("Saldo insuficiente!")


'''11: Contar frequência de letras em uma frase'''
frase = input("Digite uma frase: ")
frequencia = {}

for letra in frase:
    if letra in frequencia:
        frequencia[letra] += 1
    else:
        frequencia[letra] = 1
for letra, contagem in frequencia.items():
    print(f"{letra}: {contagem}")

print("Frequência de cada caractere:")


'''12: Criar um menu interativo'''
itens = []

while True:
    print("1 - Adicionar item")
    print("2 - Remover item")
    print("3 - Listar itens")
    print("4 - Sair")

    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        item = input("Digite o item que deseja adicionar: ")
        itens.append(item)
        print("Item adicionado!")

    elif opcao == "2":
        item = input("Digite o item que deseja remover: ")
        if item in itens:
            itens.remove(item)
            print("Item removido!")
        else:
            print("Item não encontrado.")

    elif opcao == "3":
        print("Itens na lista:")
        for item in itens:
            print("- " + item)

    elif opcao == "4":
        print("Saindo do programa.")
        break

    else:
        print("Opção inválida. Tente novamente.")


'''13: Gerar uma tabela formatada de alunos e notas'''
alunos = []

quantidade = int(input("Quantos alunos deseja cadastrar? "))

for i in range(quantidade):
    nome = input(f"Nome do aluno {i+1}: ")
    nota1 = float(input("Nota 1: "))
    nota2 = float(input("Nota 2: "))
    media = (nota1 + nota2) / 2

    aluno = {
        "nome": nome,
        "nota1": nota1,
        "nota2": nota2,
        "media": media
    }

    alunos.append(aluno)

print("\nAlunos e Notas:")
for aluno in alunos:
    print("Nome:", aluno["nome"])
    print("Nota 1:", aluno["nota1"])
    print("Nota 2:", aluno["nota2"])
    print("Média:", aluno["media"])
    print("-" * 20)
