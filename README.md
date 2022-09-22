
nome_idade = ''
idade_nome = []
idade1 = 0
matutino = []
vespertino = []
acumulador = 0
contador = 0
contador2 = 0

for i in range (0,6):
    print("---------------------")
    nome = input("Insira o nome do aluno:")
    print("---------------------")
    idade = int(input("Insira a idade do aluno:"))
    if (idade > idade1):
        nome_idade = nome
        idade_nome.append(idade)
        idade1 = idade
    print("---------------------")
    acumulador = acumulador + idade
    turno = input("Insira o turno do aluno (M ou V):").upper()
    if (turno == "M") and (idade <= 14):
        contador = contador + 1
        matutino.append(turno)
    elif (turno == "V"):
        contador2 = contador2 + 1
        vespertino.append(turno)

m_idade = (acumulador/6)
print("---------------------")
print("O nome da pessoa mais velha é:",nome_idade)
print("---------------------")
print("A média de idades é {}".format(m_idade))
print("---------------------")
print("Ao todo temos {} aluno(s) no turno matutino com menos de 15 anos".format(contador))
print("---------------------")
print("Ao todo temos {} aluno(s) no turno vespertino".format(contador2))
