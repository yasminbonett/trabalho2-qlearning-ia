# Trabalho 2 – Q-learning aproximado: jogador contra goleiro

Disciplina de Inteligência Artificial – Ciência da Computação (FCT-UNESP)

## Autores

- Gabrielly Christina Moreira
- Marcos André Trajano da Silva Júnior
- Yasmin de Oliveira Bonet

## Sobre o trabalho

Implementação de um jogo de cobrança de gol e de um agente que aprende a jogá-lo com **Q-learning aproximado** (features e pesos, sem tabela de estados). O jogador atravessa o campo até a área de chute e precisa chutar quando o goleiro não está na sua linha.

O projeto usa somente Python com `numpy`, `pandas` e `matplotlib`.

## Arquivos

| Arquivo              | Conteúdo                                                                                     |
| -------------------- | -------------------------------------------------------------------------------------------- |
| `jogo.py`            | Regras do jogo, desenho do campo no terminal e agentes de referência (aleatório e de regras) |
| `agente.py`          | Features, agente de Q-learning aproximado, funções de treino e avaliação                     |
| `experimentos.py`    | Seis experimentos (alpha, gamma, epsilon, episódios, features e comportamento do goleiro)    |
| `resultados/`        | Tabelas (.csv) e gráficos (.png) gerados pelo `experimentos.py`                              |

## Como executar

1. Instalar as bibliotecas: `python -m pip install numpy pandas matplotlib`
2. Deixar os arquivos `.py` na mesma pasta.
3. Rodar, nesta ordem:
   - `python jogo.py` (jogo de exemplo e agentes de referência)
   - `python agente.py` (treino com os parâmetros padrão)
   - `python experimentos.py` (todos os experimentos; leva alguns minutos e cria a pasta `resultados`)

## Resultado principal

Com os parâmetros padrão (alpha 0,05; gamma 0,9; epsilon 0,1; 3000 episódios), o agente treinado marca gol em 100% das partidas de avaliação, contra cerca de 1,7% de um agente que joga ao acaso. Sem as features do goleiro, o agente fica em 0%. Os detalhes estão no relatório do trabalho.
