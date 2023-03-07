# Estágio_Target_Sistemas

Questionário Vaga de estágio Target Sistemas.

##Utilizando Google Colab e o Github para melhor experiência de visualização.
## Caso ocorra algum problema segue abaixo o código descrito;

<h2>Clique na imagem para entrar no diretório para melhor visualização do código<h2>
<a href="https://colab.research.google.com/drive/1JSKdP2Xo9tnrazEfjoCfjhbWgg6i_ZLL" target="_blank"><img src="https://user-images.githubusercontent.com/104304589/223461550-d7d75a8a-ace3-4637-a19f-c7f351e2edca.png" /></a>

## Caso ocorra algum problema segue abaixo o código descrito;

-----------------------------
2) R:

# Python

numero = int(input("Digite um número: ")) # Entrada de dados

fibo_1 = 0 # Variável inicial da sequência de Fibonacci
fibo_2 = 1 # Segunda variável inicial da sequência de Fibonacci

while fibo_1 <= numero: # Enquanto a primeira variável for menor ou igual ao número informado
    if fibo_1 == numero: # Verifica se o número informado é igual ao número da sequência de Fibonacci
        print("O número informado pertence à sequência de Fibonacci")
    prox_num = fibo_1 + fibo_2 # Soma dos dois números da sequência
    fibo_1 = fibo_2 # Atribuição da variável fibo_2 à variável fibo_1
    fibo_2 = prox_num # Atribuição da variável prox_num à variável fibo_2

if fibo_1 != numero: # Verifica se o número informado é diferente do número da sequência de Fibonacci
    print("O número informado não pertence à sequência de Fibonacci")

--------------------------

3)R:

// Importar biblioteca para manipulação de arquivos JSON
const fs = require('fs');

// Ler arquivo JSON que contém os dados de faturamento
let jsonData = fs.readFileSync('faturamento.json');
let faturamento = JSON.parse(jsonData);

// Variáveis para fazer os cálculos
let menorFaturamento = 0;
let maiorFaturamento = 0;
let somaFaturamento = 0;
let diasComFaturamento = 0;

// Percorrer o vetor de faturamento
for (let i = 0; i < faturamento.length; i++) {
  // Verificar se o dia tem faturamento
  if (faturamento[i] > 0) {
    // Verificar se é o menor faturamento
    if (faturamento[i] < menorFaturamento || menorFaturamento == 0) {
      menorFaturamento = faturamento[i];
    }
    // Verificar se é o maior faturamento
    if (faturamento[i] > maiorFaturamento) {
      maiorFaturamento = faturamento[i];
    }
    // Somar para calcular a média
    somaFaturamento += faturamento[i];
    diasComFaturamento++;
  }
}

// Calcular a média
let mediaFaturamento = somaFaturamento / diasComFaturamento;

// Variável que conta o número de dias com faturamento superior à média
let diasAcimaMedia = 0;

// Percorrer o vetor de faturamento para contar os dias acima da média
for (let i = 0; i < faturamento.length; i++) {
  if (faturamento[i] > mediaFaturamento) {
    diasAcimaMedia++;
  }
}

// Imprimir os resultados
console.log(`Menor faturamento: R$ ${menorFaturamento}`);
console.log(`Maior faturamento: R$ ${maiorFaturamento}`);
console.log(`Dias com faturamento superior à média: ${diasAcimaMedia}`);

----------------------

4)R:
#Linguagem Python

faturamento_sp = 67836.43
faturamento_rj = 36678.66
faturamento_mg = 29229.88
faturamento_es = 27165.48
faturamento_outros = 19849.53

total_faturamento = faturamento_sp + faturamento_rj + faturamento_mg + faturamento_es + faturamento_outros

percentual_sp = (faturamento_sp / total_faturamento) * 100
percentual_rj = (faturamento_rj / total_faturamento) * 100
percentual_mg = (faturamento_mg / total_faturamento) * 100
percentual_es = (faturamento_es / total_faturamento) * 100
percentual_outros = (faturamento_outros / total_faturamento) * 100

print('O percentual de representação de SP foi de', percentual_sp, '%')
print('O percentual de representação de RJ foi de', percentual_rj, '%')
print('O percentual de representação de MG foi de', percentual_mg, '%')
print('O percentual de representação de ES foi de', percentual_es, '%')
print('O percentual de representação de Outros foi de', percentual_outros, '%')

-------------------------

5)R:
# Entrada de dados
string = input("Digite uma string para ser invertida: ")

# Criando variáveis
invertida = ""

# Loop para inverter a string
for i in range(len(string)-1, -1, -1):
   invertida += string[i]

# Imprimir resultado
print("A string invertida é:", invertida)
