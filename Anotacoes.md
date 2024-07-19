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

### Naive Bayes

Usa probabilidades (cria uma tabela de probabilidades) de acordo com a base de dados de treinamento

Cálculos que geram um modelo de dados

- Base de dados de treinamento: Que o algoritmo vai usar para aprender
- Base de dados de teste: Que iremos usar para testar como estão os resultados do nosso algoritmo (geralmente dividimos nossa base de dados que temos inicialmente em duas partes, uma maior para ser de treinamento e outra menor para os testes)

CA: Classification Accuaricy -> Precisão da clasificação

Confusion Matrix: Matriz de confusão, que mostra os acertos e erros do modelo

Podemos salvar o modelo treinado para usá-lo para outras previsões ou testes

### Técnica da árvore de decisão

Usa cálculos de "entropia" e "ganho de informação" para indicar quais são os atributos mais importantes de serem usados para criar a árvore de decisão.

### Aprendizagem por regras

Faz cálculos estatísticos e retorna regras para classificar os itens

### KNN

Calcula a distância de um objeto para o outro
