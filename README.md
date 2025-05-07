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

        quilometros_rodados = float(input("Quantos quilômetros você percorreu? "))
        litros_usados = float(input("Quantos litros de combustível você usou? "))

        if litros_usados == 0:
            print("ERRO: você não pode dividir por zero! Informe um valor válido.")
        else: 
             consumo = quilometros_rodados / litros_usados

        print(f"Seu consumo médio foi de {consumo:.2f} km\l")
       
        pass

    elif opcao == "2":
        # Custo de viagem

        print("Você escolheu calcular o custo de viagem.")

        quilometros_rodados = float(input("Quantos quilômetros você percorreu? "))
        litros_usados = float(input("Quantos litros de combustível você usou? "))
        preco_combustivel = float(input("Qual o valor do litro do combustível? "))

        if quilometros_rodados <= 0 or litros_usados <= 0 or preco_combustivel <= 0:
            print("Todos os valores devem ser maiores que zero. ")
        else:
            consumo_medio = quilometros_rodados / litros_usados
            custo_total = litros_usados * preco_combustivel

            print(f"Consumo médio: {consumo_medio:.2f}km/l")
            print(f"Custo total da viagem: R$ {custo_total:.2f}")
        pass

    elif opcao == "3":
        # Verificação de revisões
        print("Você ecolheu calcular a data da próxima troca de óleo.")
        km_atual = int(input("Insira a quilometragem atual do seu veíiculo: "))
        km_ultima_troca = int(input("Insira a quilometragem da última troca de óleo do seu veículo: "))

        if km_atual <= 0 or km_ultima_troca <= 0:
            print("Todos os valores devem ser maiores que zero.")
        else:
            proxima_troca = km_atual - km_ultima_troca

            if proxima_troca >= 10000:
                print("É hora de trocar o óleo!!!")
            else:
                faltam = 10000 - proxima_troca
                print(f"Ainda não é necessário, faltam {faltam} km para a próxima troca.")
        pass

    elif opcao == "4":
        print("Obrigado por usar o AutoHelper! Até a próxima!")
        break

    else:
        print("Opção inválida! Tente novamente.")
