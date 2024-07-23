# Inteligência Artificial

**O que é:**

## Conceitos:

* Heurística - fórmula matemárica para dizer o quão perto ou o quão longe o computador está do problema
  * Algo que vai guiar o computador, ajudando a chegar na solução do problema

## Algoritmo de otimização

Diferença entre algoritmo de busca e de otimização:

Algoritmo de busca: Sair de um estado inicial para um estado final

Algoritmo de otimização: Maximizar ou minimizar um valor

Heurística: específico de um problema

Metaheurística: Técnicas/algoritmos que se aplicam a vários problemas

Fitness function: função de custos - Retorna o valor que queremos otimizar

### **Algoritmo genético**

- indivíduo -> cada solução possível
- população -> Conjunto de soluções (indivíduos)
- gene -> Cada valor/variável que compõe uma solução. No exemplo do curso e do problema dos voor, é cada voo que forma a escala de voo
- Cromossomo -> Conjunto de genes (variáveis/valores) que compõem uma solução. No exemplo do curso e do problemas dos voos, é o conjunto dos voos que formam a escala de voos da solução
- Avaliar a população -> Aplicar a função de custo ou fitness function para saber qual é o "valor" daquela população
- Critério de parada -> número de gerações (iterações) do algoritmo

Funcionamento do algoritmo genético: geramos uma população aleatória inicial. Depois, avaliamos a população e selecionamos como pais os melhores indivíduos (aqueles que possuem o melhor custo) e usamos eles de base para gerar as novas gerações. Para isso, usamos as duas técnicas de reprodução: Crossover/reprodução (que mistura os genes dos pais) e mutação (que muda um gene aleatoriamente). Agora, teremos uma nova população, que será avaliada e a população antiga descartada. Assim, caso ainda não tenhamos atingido a condição de parada, o algoritmo usa essa nova população para continuar o processo, repetindo as técnicas de reprodução e gerando novas gerações de populações.

## Lógica Fuzzy (Lógica Difusa)

Trabalha com variáveis que variam de 0 a 1 (são booleanas mas temos uma faixa de intervalos entre elas). Ex: quente e frio. Não existe apenas está quente e está frio. Pode estar morno, um pouco quente etc. Varia da interpretação também.

Na lógica fuzzy, a afirmação está frio, se transforma em uma variável que terá um valor de 0 a 1 e tiramos a conclusão a partir desse valor. Quanto mais próximo do 1, mais "verdadeira" é a afirmação e quanto mais próximo do 0 mais "falsa" é a afirmação. Exemplo:

esta_frio = 0.2 -> está um pouco frio (pouco falso)

esta_frio = 0.5 -> está mais ou menos frio (meio falso)

esta_frio = 0.8 -> está bem frio (quase verdadeiro; mais verdadeiro do que falso)

Normalmente usar técnicas de inteligência artificial desse tipo requer conhecimento de um especialista no assunto que estamos tratando.

## Machine Learning

IA que aprende com os dados. Necessita de uma série de dados histórica e rotulada

### Classificação

#### Naive Bayes

Usa probabilidades (cria uma tabela de probabilidades) de acordo com a base de dados de treinamento

Cálculos que geram um modelo de dados

- Base de dados de treinamento: Que o algoritmo vai usar para aprender
- Base de dados de teste: Que iremos usar para testar como estão os resultados do nosso algoritmo (geralmente dividimos nossa base de dados que temos inicialmente em duas partes, uma maior para ser de treinamento e outra menor para os testes)

CA: Classification Accuaricy -> Precisão da clasificação

Confusion Matrix: Matriz de confusão, que mostra os acertos e erros do modelo

Podemos salvar o modelo treinado para usá-lo para outras previsões ou testes

#### Técnica da árvore de decisão

Usa cálculos de "entropia" e "ganho de informação" para indicar quais são os atributos mais importantes de serem usados para criar a árvore de decisão.

#### Aprendizagem por regras

Faz cálculos estatísticos e retorna regras para classificar os itens

#### KNN

Calcula a distância de um objeto para o outro (k-Nearest Neighbors)

#### SVM (Máquinas de vetores de suporte)

Ecnontra uma "linha" (vetor) que separa as duas classes. O objetivo é encontrar essa linha que tenha margens máximas (com a maior distância da linha para os pontos mais próximos dela).

A distância do vetor que separa as classes para os pontos mais próximos são os "vetores de suporte", por isso o nome do algoritimo.

Utiliza contas mais complexas mas possui bons resultados dentro da aprendizagem de máquina. Além disso, demora um pouco mais para executar o treinamento do que os outros algoritmos.

Embedding: transforma um dado (ex: imagem) em tipos e atributos próprios para serem usados em algoritmos de inteligência artificial, ou seja, para passarem pelas fórmulas matemáticas que os algoritmos utilizam ou para serem testadas em modelos já prontos.

#### Regressão logística

é para classificacao

usa um sigmoide que passa pela maior quantidade de pontos que conseguir para classificar algo

### Regressão

Prever um número (e não uma classe, como ocorre na classificação)

x -> y

x: atributos previsores

y: resposta

#### Regressão linear

O objetivo é encontrar uma relação linear entre os atributos previsores e a resposta.

Para isso, precisamos calcular os coeficientes angular e linear da reta (que são os coeficientes da função linear - y = b0 + b1*x1) e isso é feito no treinamento do algoritmo.

Possui um erro, que é a distância dos pontos até a linha gerada pelo algoritmo.

Além disso, pode ser simples ou composta:

Simples: apenas um atributo -> y = b0 + b1*x1

Composta: mais de um atributo previsor -> y = b0 + b1+x1 + b2*x2 + ... + bn * xn

MAE Minumum absolute error -> Um dos parâmetros para verificar a eficiência do modelo de regressão linear (é a diferença entre o ponto na linha, gerado pela previsão, e o valor real da base de dados. Ou seja, a distância entre a linha da regressão e o ponto real na base de dados). Como é o "mínimo", é o menor valor de "erro" que o algoritmo pode ter. Então, se o resultado der 500 e o MAE for 100, sabemos que o valor real pode variar entre 600 e 400.

R2: Calcula a correlação entre os atributos previsores e o preço do carro. Quanto mais próximo de 1 melhor é o algoritmo. A partir de 0,75 temos uma correlação forte.

### Agrupamento

Não se trata de fazer previsões como na classificação ou regressão, mas sim buscar uma característica em comum para agrupar os itens.

#### K-means

Dependendo da quantidade k de grupos que queremos formar, escolhe k pontos aleatórios no nosso conjunto de dados (ex: 3) para serem os centros dos grupos (chamados centróides). Depois, calcula a distância de todos os outros pontos dos centroides e o ponto irá pertencer ao grupo cujo centróide está mais perto.

Depois disso, o algoritmo calcula um novo centróide para cada grupo de acordo com os pontos que ele encontrou no passo anterior (dessa vez o centroide não precisa ser, necessariamente, um ponto do grupo). Escolhendo os novos centroides, o cálculo do centróide mais próximo de cada ponto é refeito e, caso seja necessário, os pontos podem mudar de grupo, indo o grupo do centróide mais próximo. Depois de terminar, o algoritmo irá calcular novos centróides e calcular novamente as distâncias...

E assim o algoritmo repete os passos, calculando novos centróides e trocando os pontos de grupo até que não seja necessária realizar mais nenhuma troca, finalizando assim o agrupamento.

### Associação

Regras de associação é uma forma de encontrar regras do tipo se... então... que vão tentar prever o comportamento de algum fenômeno. Ex: Se uma pessoa compra pão no mercado, então ela comprará café.

Algoritmo mais usado: Algoritmo A priori

#### A Priori

Algoritmo usado para criar regras de associação. Precisa de um número de suporte e confiança

- Suporte:
- Confiança:

### Pré-processamento

Com machine learning, como sempre trabalhamos com bases de dados, é recomendado que façamos um pré-processamento da nossa base, ao invés de jogá-la, como ela está, para o algoritmo. Isso irá melhorar a saída do algoritmo e até mesmo a precisão do nosso modelo. Entre as principais técnicas de pré-processamento, podemos citar:

- Normalização
- Tratamento de dados faltantes
- Discretização: Transforma atributos contínuos em faixas de valores. Ex: ao invés da idade ficar como um número entre 1 e 60, teremos faixas do tipo: idade de 1 a 10, de 11 a 25, de 25 a 31 etc. Isso pode ser útil para a aplicação de alguns tipos de algoritmos (regras de associação, por ex)
- Escolher os atributos corretos (mais relevantes)
- PCA (Principal Component Analysis): Usado para diminuir a dimensionalidade dos dados (quantidade de atributos). Cria novos atributos para serem usados no lugar dos originais, mas não descarta a informação original. Ao invés disso, ele faz cálculos com os atributos originais para gerar os novos, também chamados de PC. Muito usado para criar agrupamentos, já que podemos usar todos os atributos para criar 2 PCs que serão os eixos do nosso gráfico.
- Detecção e tratamento de outliers (registros fora do padrão). Podemos usar boxplot, gráficos de dispersão (scatter plot) etc.

### Time series

Outro tipo de dados que tem tratamentos, visualização e manipulação diferentes são time series (ou linha do tempo), que são gráficos que variam de acordo com o tempo. Normalmente visualizamos esses dados com gráficos de linhas e podemos fazer tratamentos de redução de ruído, cálculo de crescimento, decrescimento e aceleração. Além disso, podemos tirar conclusões de correlação ou auto-correlação (o quanto um valor varia em um determinado período)

#### Machine Learning com Time Series

O modelo mais usado é o ARIMA model, mas também temos o VAR model (Vector Auto Regression)


### Aprendizagem por reforço

Existe um ambiente e um agente.

Agente: Faz uma série de ações no ambiente, caminhando entre diferentes estados e recebendo recompensas para quando se aproxima do objetivo

Recompensas positivas são quando o agente está se aproximando do objetivo. Já recompensas negativas são quando o agente se distancia do objetivo.

Nesse tipo de aprendizagem, não precisamos possuir uma base de dados prévia, já que o algoritmo será inteiramente treinado durante os treinamentos com o reforço.

Living penalty: penalidade pelo agente estar "vivo" no ambiente, para que ele não fique se movimentando e tomando decisões aleatórias e demoradas. Isso força ele a otimizar a resolução do problema.

Fórmula matemática muito usada na aprendizagem de reforço: Equação de Bellman (Busca o V, valor para as ações, para decidir qual é o melhor estado)

    - V=1, melhor estado

    - Gammsssa: fator de desconto (está relacionado com as recompensas)

Markov Decision Process (MDP) - Exploration (Existe uma chance pequena do agente não seguir o melhor caminho. Porém, isso faz com que ele continue explorando o ambiente) Vs Exploitation (SEMPRE serguirá para o melhor caminho)

Algoritmo Q-Learning: fórmula matemática básica para escolher as melhores ações. Com o Q-learning temos uma abordagem mais voltada para as ações e recompensas do agente. Daí, com esse algoritmo, precisamos do valor de Q para calcular o valor de V na Equação de Bellman

Episódio: rodada completa de execução do algoritmo

Diferença temporal: De acordo com cada ação/estado em que o agente toma, os valores V e qualidades Q das ações mudam.

Learning rate: Coeficiente na fórmula da diferença temporal que indica o quão rápido o algoritmo vai aprender

O objetivo é que o algoritmo aprenda a escolher as melhores ações para ganhar as melhores recompensas possíveis
