# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

**->B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.**

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.


______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'

**-->C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'**

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

**-->C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".**

D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".


______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200


B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.


**-->C)**
**Compra 1 aprovada. Saldo restante: 800**

**Compra 2 aprovada com limite de crédito. Saldo restante: 700**

**Compra 3 aprovada. Saldo restante: 400**

**Compra 4 negada. Saldo insuficiente e limite de crédito excedido.**

D)

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

**-->B) Preload -> Create -> Update**

C) Load -> Initialize -> Render

D) Begin -> Play -> End
______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

**-->B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.**

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

```

# Algoritmo para verificar se uma pessoa pode votar

# Entrada: Idade da pessoa (inteiro)

# Saída: Mensagem informando se a pessoa pode votar

# Declaração de variáveis
idade = int(input("Insira sua idade: "))

# Verificação da idade
if idade < 16:
  # Pessoa não pode votar
  print("Você não pode votar!")
else:
  # Pessoa pode votar
  if idade < 18:
    # Voto facultativo
    print("Você tem voto facultativo!")
  else:
    # Voto obrigatório
    print("Você tem voto obrigatório!")

```
______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

Classe Retangulo herda de FormaGeometrica:
    Atributos:
        - base
        - altura

    Método Construtor(cor, base, altura):
        Chama o construtor da classe pai passando 'cor' como parâmetro.
        Define os valores dos atributos base e altura com os valores passados como parâmetros.

    Método CalcularArea():
        Retorna base * altura.

Classe Circulo herda de FormaGeometrica:
    Atributos:
        - raio

    Método Construtor(cor, raio):
        Chama o construtor da classe pai passando 'cor' como parâmetro.
        Define o valor do atributo raio com o valor passado como parâmetro.

    Método CalcularArea():
        Retorna π * raio^2.

```

______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

Considere a fórumla de atualização velocidade:
```
    velocidade = velocidadeInicial + aceleracao*tempo
```
```
Função simularCorrida(distancia, velocidadeInicial, aceleracao, velocidadeMaxima, tempoMaximo):
    // Inicialize o tempo decorrido como 0
    tempoDecorrido = 0
    
    // Inicialize a velocidade atual como a velocidade inicial
    velocidadeAtual = velocidadeInicial
    
    // Enquanto a distância não for percorrida e o tempo não ultrapassar o máximo
    Enquanto distancia > 0 e tempoDecorrido <= tempoMaximo:
        // Atualize a velocidade atual
        velocidadeAtual = min(velocidadeAtual + aceleracao, velocidadeMaxima)
        
        // Calcule o tempo necessário para percorrer a distância restante com a velocidade atual
        tempoPercorrerDistancia = distancia / velocidadeAtual
        
        // Verifique se o tempo necessário é menor que o tempo máximo disponível
        Se tempoPercorrerDistancia <= tempoMaximo - tempoDecorrido:
            // Se sim, atualize o tempo decorrido
            tempoDecorrido = tempoDecorrido + tempoPercorrerDistancia
            
            // O carro percorreu a distância toda, então saia do loop
            Quebrar o loop
        
        Senão:
            // Calcule a distância percorrida durante o tempo máximo disponível
            distanciaPercorrida = velocidadeAtual * (tempoMaximo - tempoDecorrido)
            
            // Atualize a distância restante
            distancia = distancia - distanciaPercorrida
            
            // Atualize o tempo decorrido
            tempoDecorrido = tempoMaximo
            
    // Retorne o tempo decorrido
    Retorne tempoDecorrido

```

______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função MultiplicacaoDeMatrizes(matrizA, matrizB):
    # Verifica se o número de colunas da matrizA é igual ao número de linhas da matrizB
    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser multiplicadas. Dimensões incompatíveis."
    Senão:
        linhasA <- tamanho(matrizA)
        colunasA <- tamanho(matrizA[0]) # Número de colunas da matrizA
        colunasB <- tamanho(matrizB[0]) # Número de colunas da matrizB
        
        matrizResultado <- novaMatriz(linhasA, colunasB)

        # Loop para percorrer cada elemento da matrizResultado
        Para i de 0 até linhasA-1 faça:
            Para j de 0 até colunasB-1 faça:
                elemento <- 0
                Para k de 0 até colunasA-1 faça: # Ou k de 0 até tamanho(matrizB)-1
                    elemento <- elemento + matrizA[i][k] * matrizB[k][j]
                matrizResultado[i][j] <- elemento

        Retornar matrizResultado

```