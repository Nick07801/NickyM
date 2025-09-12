# NÍVEL 1 - Iniciante
'''EXERCÍCIO 1: Verificação de número positivo ou negativo'''
numero = int(input("digite um número"))

if numero > 0:
    print ("O número é positivo")

elif numero < 0:
    print ("O número é negativo")

else:
    print ("O número é igual a zero")


'''EXERCÍCIO 2: Verificação de número positivo ou negativo'''
idade = int(input("Digite sua idade"))

if idade > 18:
    print ("Você é maior de idade")

else:
    print ("Você é menor de idade")


'''EXERCÍCIO 3: Par ou ímpar'''
numero = int(input("Digite um número"))

if numero / 2:
    print ("O número digitado é um número par")

else:
    print ("O número digitado é um número ímpar")


# NÍVEL 2 - Intermediário
'''EXERCÍCIO 4: Classificação de nota'''
nota = float(input("Digite sua nota"))

if nota >= 7:
    print ("Voce foi Aprovado")

elif 5 <= nota < 7:
    print ("Você está de Recuperação")

else:
   print ("Você está Reprovado")


'''EXERCÍCIO 5: Login simples '''
usuario = "admin"
senha = 1234

if usuario == "admin" and senha == 1234:
    print ("Acesso concebido")

else:
    print ("Acesso negado")


'''EXERCÍCIO 6: Calculadora de IMC'''
kg = float(input ("Digite seu peso"))
m = float(input("Digite sua altura"))

imc = kg / (m**2)

print (f"seu imc é:{imc:.2f}")

if imc < 18.5:
    print ("Abaixo do peso")

elif 18.5 <= imc <= 24.9:
    print("Peso normal")

elif 25 <= imc <= 29.9:
    print ("Sobrepeso")

else:
    print ("Obesidade")


# NÍVEL 3 - Desafio
'''EXERCÍCIO 7: Calculadora de IMC'''
ano = int(input("digite um ano"))

if ano / 4 == 0:
    print("o ano é bissexto")

else:
    print("o ano não é bissexto")


'''EXERCÍCIO 8: Simulador de caixa eletrônico '''
valor = int(input("Digite o valor a ser sacado: "))

if valor < 2:
    print("Valor muito baixo para saque.")
else:
    notas_100 = valor // 100
    resto = valor % 100

    notas_50 = resto // 50
    resto = resto % 50

    notas_20 = resto // 20
    resto = resto % 20

    notas_10 = resto // 10
    resto = resto % 10

    notas_5 = resto // 5
    resto = resto % 5

    notas_2 = resto // 2
    resto = resto % 2

    print("Notas entregues:")
    print("100:", notas_100)
    print("50:", notas_50)
    print("20:", notas_20)
    print("10:", notas_10)
    print("5:", notas_5)
    print("2:", notas_2)

    if resto != 0:
        print("Não é possível sacar o valor exato com as notas disponíveis.")


'''EXERCÍCIO 9: Conversor de temperatura'''
Celsius = "c"
Fahrenheit = "f"

temperatura = int(input("Digita uma temperatura em Celsius"))

