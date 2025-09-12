usuarios = { "nicole": "0123",
            "henrique": "4567",
            "everton": "8910",
            "kauan": "6843",
            "mauricio": "9625",
            "mikael": "7219"
            }

def login():
    login = input("Digite seu login:  ")
    senha = input("Digite sua senha:  ")

    if login in usuarios and usuarios[login] == senha:
        print ("Acesso concedido")
        return True
    else:
        print ("Acesso negado")
        return False
    

while True:
    if login ():
        sair = input("Digite 'sair' para encerrar: ")
        if sair.lower() == "sair":
            print ("Até logo")
        break
    else:
        print("Usuário ou senha incorretos. Tente novamente !")
        
