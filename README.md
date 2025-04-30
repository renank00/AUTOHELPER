# AUTOHELPER
Projeto: Calculadora de Consumo e Manutenção Automotiva

# Boas vindas
print("=== AUTOHELPER - Gerenciador de Consumo e Manutenção ===")

# Loop principal 
while True:
    print("\nEscolha uma opção:")
    print("1. Calcular consumo de combustível")
    print("2. Estimar custo da viagem")
    print("3. Verificar revisões necessárias")
    print("4. Sair")

    # Receber a escolha do usuáro
    opcao = input("Digite o número da opção desejada: ")

    # Verificar a escolha do usuário

    if opcao == "1":

        # Cálculo do consumo de combustível

        print("Você escolheu calcular o consumo de combustível.")

        quilometros_rodados = float(input("Quantos quilômetros você percorreu?"))
        litros_usados = float(input("Quantos litros de combustível você usou?"))

        if litros_usados == 0:
            print("ERRO: você não pode dividir por zero! Informe um valor válido.")
        else: 
             consumo = quilometros_rodados / litros_usados

        print(f"Seu consumo médio foi de {consumo:.2f} km\l")
       
        pass

    elif opcao == "2":
        # Custo de viagem
        pass

    elif opcao == "3":
        # Verificação de revisões
        pass

    elif opcao == "4":
        print("Obrigado por usar o AutoHelper! Até a próxima!")
        break

    else:
        print("Opção inválida! Tente novamente.")
