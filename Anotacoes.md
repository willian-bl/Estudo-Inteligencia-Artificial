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

---

**Algoritmo genético:**

- indivíduo -> cada solução possível
- população -> Conjunto de soluções (indivíduos)
- gene -> Cada valor/variável que compõe uma solução. No exemplo do curso e do problema dos voor, é cada voo que forma a escala de voo
- Cromossomo -> Conjunto de genes (variáveis/valores) que compõem uma solução. No exemplo do curso e do problemas dos voos, é o conjunto dos voos que formam a escala de voos da solução
- Avaliar a população -> Aplicar a função de custo ou fitness function para saber qual é o "valor" daquela população
- Critério de parada -> número de gerações (iterações) do algoritmo

Funcionamento do algoritmo genético: geramos uma população aleatória inicial. Depois, avaliamos a população e selecionamos como pais os melhores indivíduos (aqueles que possuem o melhor custo) e usamos eles de base para gerar as novas gerações. Para isso, usamos as duas técnicas de reprodução: Crossover/reprodução (que mistura os genes dos pais) e mutação (que muda um gene aleatoriamente). Agora, teremos uma nova população, que será avaliada e a população antiga descartada. Assim, caso ainda não tenhamos atingido a condição de parada, o algoritmo usa essa nova população para continuar o processo, repetindo as técnicas de reprodução e gerando novas gerações de populações.
