# Simulador de Escalonamento de Tarefas em Tempo Real

Este programa simula o escalonamento de tarefas em sistemas de tempo real, implementando os algoritmos Rate Monotonic (RM) e Earliest Deadline First (EDF). O simulador verifica a escalonabilidade das tarefas e gera um gráfico de Gantt para visualizar o escalonamento.

## Funções Principais

### 1. escalonabilidade_rm(tarefas)

Calcula a escalonabilidade usando a condição de Liu & Layland para o algoritmo Rate Monotonic (RM).

- Entrada: Lista de tarefas, onde cada tarefa é uma tupla (tempo de execução, período)
- Saída: Tupla (escalonável, utilização total)

### 2. escalonabilidade_edf(tarefas)

Calcula a escalonabilidade para o algoritmo Earliest Deadline First (EDF).

- Entrada: Lista de tarefas, onde cada tarefa é uma tupla (tempo de execução, período)
- Saída: Tupla (escalonável, utilização total)

### 3. gerar_grafico_gantt(tarefas, tipo_escalonamento)

Simula o escalonamento e gera um gráfico de Gantt para visualizar a execução das tarefas.

- Entrada: 
  - tarefas: Lista de tarefas
  - tipo_escalonamento: String 'RM' ou 'EDF'
- Saída: Exibe um gráfico de Gantt

### 4. simulador_escalonador()

Função principal que interage com o usuário, coleta dados das tarefas, verifica a escalonabilidade e gera o gráfico de Gantt se as tarefas forem escalonáveis.

## Uso do Programa

1. Execute o programa.
2. Informe o número de tarefas.
3. Para cada tarefa, insira o tempo de execução e o período.
4. Escolha o tipo de escalonamento (RM ou EDF).
5. O programa informará se as tarefas são escalonáveis e, se forem, exibirá o gráfico de Gantt.

## Limitações e Considerações

- O programa assume que todas as tarefas estão prontas no tempo 0.
- O gráfico de Gantt é limitado a 3 vezes o maior período entre as tarefas.
- O programa não considera prioridades explícitas além das definidas pelos algoritmos RM e EDF.

