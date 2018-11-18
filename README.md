# eec1509T04
Trabalho de clustering

## Autores:
- Frederico Augusto Fernandes Silveira
- Lucileide Medeiros Dantas da Silva

## Introdução

O trabalho é composto de dois notebooks. O primeiro é a resolução do notebook apresentado na aula 08 de clustering. O segundo notebook é análise de dados do campeonado brasileiro empregando técnicas de clustering e árvore de decisão.

## Preenchiento do notebook da aula de clustering

O notebook utiliza dois arquivos necessários para sua execução: **114_congress.csv** e **nba_2013.csv**.

Diversas etapas são executadas para demonstrar com o objetivo de mostrar o funcionamento da metodologia de cluster.

## Notebook com análise de dados do campeonato brasileiro

Utilizamos o arquivo **dados_agregados_limpos.csv** para realizar as análises apresentadas no notebook.

Descrição dos dados:

| coluna          | descrição                                                 | observações                                                                                        |
|-----------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Rodada          | número da rodada do Brasileirão                           |                                                                                                    |
| ClubeID         | clube do jogador                                          | ver arquivo times_ids.csv                                                                          |
| AtletaID        | id do jogador                                             |                                                                                                    |
| Participou      | indica se o jogador participou daquela rodada             | FALSE:Não, TRUE:Sim                                                                                |
| Posicao         | posição do jogador                                        | gol:goleiro, zag:zagueiro, lat:lateral, mei:meia, ata:atacante, tec:técnico                        |
| Jogos           | qtde. de jogos que o jogador participou até aquela rodada |                                                                                                    |
| Pontos          | pontuação do jogador                                      |                                                                                                    |
| PontosMedia     | média da pontuação do jogador                             |                                                                                                    |
| Preco           | preço do jogador                                          |                                                                                                    |
| PrecoVariacao   | variação de preço                                         |                                                                                                    |
| FS              | faltas sofridas                                           |                                                                                                    |
| PE              | passes errados                                            |                                                                                                    |
| A               | assistências                                              |                                                                                                    |
| FT              | finalizações na trave                                     |                                                                                                    |
| FD              | finalizações defendidas                                   |                                                                                                    |
| FF              | finalizações para fora                                    |                                                                                                    |
| G               | gols                                                      |                                                                                                    |
| I               | impedimentos                                              |                                                                                                    |
| PP              | pênaltis perdidos                                         |                                                                                                    |
| RB              | roubadas de bola                                          |                                                                                                    |
| FC              | faltas cometidas                                          |                                                                                                    |
| GC              | gols contra                                               |                                                                                                    |
| CA              | cartões amarelo                                           |                                                                                                    |
| CV              | cartões vermelho                                          |                                                                                                    |
| SG              | jogos sem sofrer gols                                     |                                                                                                    |
| DD              | defesas difíceis                                          |                                                                                                    |
| DP              | defesas de pênalti                                        |                                                                                                    |
| GS              | gols sofridos                                             |                                                                                                    |
| ano             | ano dos dados                                             |                                                                                                    |
| Apelido         | nome/apelido do jogador                                   |                                                                                                    |
| Status          | status do jogador                                         | Provável, Dúvida, Suspenso, Nulo, ...                                                              |
| avg.Points      | média de pontos do jogador                                |                                                                                                    |
| avg.last05      | média de pontos do jogador nas últimas 5 rodadas          |                                                                                                    |
| avg.FS          | média de faltas sofridas                                  |                                                                                                    |
| avg.FS.l05      | média de faltas sofridas nas últimas 5 rodadas            |                                                                                                    |
| avg.PE          | média de passes errados                                   |                                                                                                    |
| avg.PE.l05      | média de passes errados nas últimas 5 rodadas             |                                                                                                    |
| avg.A           | média de assistências                                     |                                                                                                    |
| avg.A.l05       | média de assistências nas últimas 5 rodadas               |                                                                                                    |
| avg.FT          | média de finalizações na trave                            |                                                                                                    |
| avg.FT.l05      | média de finalizações na trave nas últimas 5 rodadas      |                                                                                                    |
| avg.FD          | média de finalizações defendidas                          |                                                                                                    |
| avg.FD.l05      | média de finalizações defendidas nas últimas 5 rodadas    |                                                                                                    |
| avg.FF          | média de finalizações para fora                           |                                                                                                    |
| avg.FF.l05      | média de finalizações para fora nas últimas 5 rodadas     |                                                                                                    |
| avg.G           | média de gols                                             |                                                                                                    |
| avg.G.l05       | média de gols nas últimas 5 rodadas                       |                                                                                                    |
| avg.I           | média de impedimentos                                     |                                                                                                    |
| avg.I.l05       | média de impedimentos nas últimas 5 rodadas               |                                                                                                    |
| avg.PP          | média de pênaltis perdidos                                |                                                                                                    |
| avg.PP.l05      | média de pênaltis perdidos nas últimas 5 rodadas          |                                                                                                    |
| avg.RB          | média de roubadas de bola                                 |                                                                                                    |
| avg.RB.l05      | média de roubadas de bola nas últimas 5 rodadas           |                                                                                                    |
| avg.FC          | média de faltas cometidas                                 |                                                                                                    |
| avg.FC.l05      | média de faltas cometidas nas últimas 5 rodadas           |                                                                                                    |
| avg.GC          | média de gols contra                                      |                                                                                                    |
| avg.GC.l05      | média de gols contra nas últimas 5 rodadas                |                                                                                                    |
| avg.CA          | média de cartões amarelos                                 |                                                                                                    |
| avg.CV          | média de cartões vermelhos nas últimas 5 rodadas          |                                                                                                    |
| avg.SG          | média de jogos sem sofrer gols                            |                                                                                                    |
| avg.SG.l05      | média de jogos sem sofrer gols nas últimas 5 rodadas      |                                                                                                    |
| avg.DD          | média de defesas difíceis                                 |                                                                                                    |
| avg.DD.l05      | média de defesas difíceis nas últimas 5 rodadas           |                                                                                                    |
| avg.DP          | média de defesas de pênalti                               |                                                                                                    |
| avg.DP.l05      | média de defesas de pênalti nas últimas 5 rodadas         |                                                                                                    |
| avg.GS          | média de gols sofridos                                    |                                                                                                    |
| avg.GS.l05      | média de gols sofridos nas últimas 5 rodadas              |                                                                                                    |
| risk_points     | desvio-padrão da pontuação do jogador                     |                                                                                                    |
| mes             | mês que a partida ocorreu                                 |                                                                                                    |
| dia             | dia que a partida ocorreu                                 |                                                                                                    |
| away.score.x    | placar to time visitante                                  |                                                                                                    |
| home.score.x    | placar do time da casa                                    |                                                                                                    |
| home.attack     | estimativa de força de ataque do time do jogador          | estimada a partir de uma regressão de Poisson com base no histórico de confrontos entre os times   |
| home.defend     | estimativa de força de defesa do time do jogador          | estimada a partir de uma regressão de Poisson com base no histórico de confrontos entre os times   |
| pred.home.score | estimativa de gols para o time da casa                    | estimada a partir de 10000 simulações  de confronto entre os times usando distribuições de Poisson |
| pred.away.score | estimativa de gols para o time visitante                  | estimada a partir de 10000 simulações,de confronto entre os times usando distribuições de Poisson  |
| variable        | indica se o jogador é do time da casa ou visitante        | home.team: casa, away.team: visitante                                                              |


Créditos: [dados](https://github.com/henriquepgomide/caRtola/tree/master/data)

### Tarefas realizadas

Realizamos inicialmente a instalção dos pacotes necessários e o carregamento dos módulos utilizados.

Foi definida uma função de visualização do cluster chamada **visualize_clusters_s_c**.

Em seguida, fizemos o carragamento do dataset.

Fizemos inicialmente uma análise da posição **Goleiro**. Plotamos um gráfico de inércia do cluster, fazendo com que tenhamos a quantidade de cluster ideal para a clusterização.

Geramos dois gráficos: **Média de Defesas Difíceis x Média de Jogos sem sofrer gols** e **Média de Defesas Difíceis x Média de gols sofridos**

Após isso, trabalhamos com a posição **Atacante**. Da mesma forma, geramos o gráfico de inércia.

Em seguida, geramos o gráfico de cluster **Média de Gols x Média de Gols perdidos**.

Começamos a etapa da utilização de árvore de decisão. Onde, escolhemos alguns atributos para gerar a classificação da posição do jogador, dependendo do padrão encontrado.

Separamos os dados de treinamento e teste. Criamos o modelo e realizamos a predição. Após isso, geramos uma matriz de confusão, mostrando uma boa taxa de precisão. 

Após, geramos o gráfico da árvore utilziando a biblioteca **graphviz**.


