# Jogo-Da-Vida-0.1v
Jogo Da Vida Em Python

# Jogo da Vida de Conway
importrandom, time, copy
WIDTH = 10
HEIGHT = 10

# Cria uma lista de listas de celulas:
nextCells = []
for x in range(WIDTH):
column = [] # Cria uma coluna em uma lista.
    for y in range(HEIGHT):
ifrandom.randint(0, 1) == 0:
column.append('#') # Adiciona uma célula viva.
else:
column.append('.') # Adiciona uma célula morta.
nextCells.append(column) # nextCells é uma lista de colunas.

whileTrue:
    print('\n\n\n\n\n')
currentCells = copy.deepcopy(nextCells) # Cria uma cópia da lista principal

	# Imprime na tela:
    for y in range(HEIGHT):
        for x in range(WIDTH):
            print(currentCells[x][y], end='') # Imprime cada célula.
print() # Imprime uma nova linha ao término de cada linha.

    # Calcula o próximo ciclo com base nas células do ciclo atual:
    for x in range(WIDTH):
        for y in range(HEIGHT):
            # Verifica as células vizinhas:
leftCoord = (x - 1)
rightCoord = (x + 1)
aboveCoord = (y - 1)
belowCoord = (y + 1)

            # Conta o número de vizinhos vivos:
numNeighbors = 0
ifaboveCoord>= 0:
ifleftCoord>= 0:
ifcurrentCells[leftCoord][aboveCoord] == '#':
numNeighbors += 1 # Celula Superior Esquerda está viva.
ifcurrentCells[x][aboveCoord] == '#':
numNeighbors += 1 # Celula Superior está viva.
ifrightCoord< 10:
ifcurrentCells[rightCoord][aboveCoord] == '#':
numNeighbors += 1 # Celula Superior Direita está viva.

ifleftCoord>= 0:
ifcurrentCells[leftCoord][y] == '#':
numNeighbors += 1 # Celula Esquerda está viva.
ifrightCoord< 10:
ifcurrentCells[rightCoord][y] == '#':
numNeighbors += 1 # Celula Direita está viva.

ifbelowCoord< 10:
ifleftCoord>= 0:       
ifcurrentCells[leftCoord][belowCoord] == '#':
numNeighbors += 1 # Celula Inferior Esquerda está viva.
ifcurrentCells[x][belowCoord] == '#':
numNeighbors += 1 # Celula Inferior está viva.
ifrightCoord< 10:
ifcurrentCells[rightCoord][belowCoord] == '#':
numNeighbors += 1 # Celula Inferior Direita está viva.

            # Anota como ficará cada célula de acordo com a regra do Jogo da Vida de Conway:
ifcurrentCells[x][y] == '#' and (numNeighbors == 2 ornumNeighbors == 3):
                # Células Vivas com 2 ou 3 vizinhos vivos permanecem vivas:
nextCells[x][y] = '#'
elifcurrentCells[x][y] == '.' andnumNeighbors == 3:
                # Células Mortas com exatamente 3 vizinhos voltam a vida:
nextCells[x][y] = '#'
else:
                # Qualquer outra condição, a célula morre ou permanece morta:
nextCells[x][y] = '.'
time.sleep(1)

,

