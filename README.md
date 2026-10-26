# Mini Projeto — Análise Exploratória de Dados (AED) no Varejo

**Aluno:** Sergio Elias  
**Turma:** T8  
**Projeto:** Análise Exploratória de Dados aplicada ao varejo

## 1. Objetivo

Desenvolver uma Análise Exploratória de Dados (AED) utilizando Python e Pandas para examinar uma base de dados de varejo, identificar problemas de qualidade, tratar os dados e gerar informações úteis para a compreensão do negócio.

## 2. Origem dos dados

A base utilizada é a base Varejo indicada no enunciado da atividade.

**Fonte:** [Kaggle — Base Varejo](https://www.kaggle.com/datasets/namespaiva/base-varejo/data)

**Arquivo original:** `pedidos_diagnostico.csv`

## 3. Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Google Colab
- GitHub

## 4. Etapas do projeto

1. Leitura do arquivo CSV e inspeção dos registros, colunas e tipos de dados.
2. Diagnóstico de valores ausentes, duplicatas, textos vazios e inconsistências.
3. Limpeza e padronização dos dados.
4. Criação de funções reutilizáveis para limpeza e resumo dos dados.
5. Cálculo de estatísticas descritivas, aplicação de filtros e agrupamentos.
6. Visualização da quantidade de pedidos e do faturamento por dia.
7. Exportação da base tratada para `varejo_limpo.csv`.

## 5. Decisões de limpeza

A base original possuía 38 registros e 8 colunas. Após a remoção de dois registros duplicados, a base tratada passou a ter 36 registros.

Foi criada a função reutilizável `limpar_dados()`, responsável por remover espaços extras dos textos. Após o tratamento, não foram encontrados registros duplicados nem espaços extras nas colunas textuais verificadas.

A base tratada permaneceu com cinco valores ausentes:

- `cliente`: 2 valores ausentes.
- `valor_compra`: 2 valores ausentes.
- `quantidade`: 1 valor ausente.

Esses valores foram mantidos porque não havia informações suficientes para determinar os valores corretos. Por isso, devem ser considerados ao interpretar as análises dessas colunas.

Também foi criada a função `resumir_dados()`, que retorna a quantidade de registros, a quantidade de colunas e o total de valores ausentes por coluna.

## 6. Processo de leitura, transformação e gravação

A leitura da base foi realizada com `pandas.read_csv()`. As transformações foram executadas utilizando funções Python e operações do Pandas para inspecionar, limpar e analisar os dados.

Ao final, a base tratada foi exportada para `varejo_limpo.csv` utilizando `to_csv(index=False)`, evitando a inclusão do índice como uma coluna adicional.

A base exportada contém 36 registros e 8 colunas.

## 7. Resultados e conclusões

### 7.1. Estatísticas dos valores de compra

A análise da coluna `valor_compra` apresentou os seguintes resultados:

- **Quantidade de valores válidos:** 34.
- **Valor médio das compras:** R$ 465,90.
- **Menor valor de compra:** R$ 90,03.
- **Maior valor de compra:** R$ 943,30.

Os resultados demonstram variação entre os valores dos pedidos. A média fornece uma referência para compreender os valores das compras registradas, mas não significa que a maioria dos pedidos tenha exatamente esse valor.

### 7.2. Filtro de pedidos

Foi aplicado um filtro para selecionar pedidos com valor de compra superior a R$ 500,00. Foram identificados **13 pedidos** que atendem a esse critério.

Entre os pedidos filtrados, há registros com status entregue, pendente e cancelado. Isso demonstra a importância de considerar o status ao interpretar os resultados comerciais.

### 7.3. Análise por canal de venda

| Canal | Quantidade de pedidos | Faturamento observado | Ticket médio |
|---|---:|---:|---:|
| Loja | 16 | R$ 7.559,00 | R$ 503,93 |
| Site | 12 | R$ 5.605,92 | R$ 467,16 |
| App | 8 | R$ 2.675,75 | R$ 382,25 |

O canal Loja apresentou o maior faturamento observado, seguido pelo Site e pelo App.

### 7.4. Análise por categoria

| Categoria | Quantidade de pedidos | Faturamento observado | Ticket médio |
|---|---:|---:|---:|
| Beleza | 12 | R$ 6.385,18 | R$ 532,10 |
| Moda | 11 | R$ 4.694,71 | R$ 469,47 |
| Eletrônicos | 8 | R$ 2.504,68 | R$ 357,81 |
| Casa | 5 | R$ 2.256,10 | R$ 451,22 |

A categoria Beleza apresentou o maior faturamento observado e o maior ticket médio entre as categorias. Casa registrou a menor quantidade de pedidos.

### 7.5. Análise diária dos pedidos

- **Faturamento total observado:** R$ 15.840,67.
- **Faturamento médio diário:** R$ 754,32 por dia registrado na tabela.
- **Maior faturamento diário:** 25/09/2026, com R$ 1.715,76.
- **Menor faturamento diário:** 19/09/2026, com R$ 146,26.
- **Quantidade total de pedidos:** 36.
- **Média de pedidos por dia registrado:** 1,71.

O gráfico de barras permite comparar a quantidade de pedidos por dia, enquanto o gráfico de linhas ajuda a observar as variações do faturamento diário.

### 7.6. Recomendação

Acompanhar a quantidade de pedidos e o faturamento por dia, canal e categoria. Essa prática pode ajudar a identificar variações no desempenho comercial e orientar investigações sobre os fatores que influenciam as vendas.

### 7.7. Limitações da análise

Os resultados dependem dos registros disponíveis na base. As médias diárias consideram os dias presentes na tabela agrupada, não necessariamente todos os dias do mês.

A existência de valores ausentes em `valor_compra` limita algumas análises. Além disso, faturamento não representa lucro, pois não foram considerados custos e despesas. Os resultados não devem ser generalizados para períodos ou operações que não estejam representados na base.

## 8. Arquivos do repositório

- `MiniProjeto_AED_Varejo_Sergio_Elias_T8.ipynb`: notebook com o código, as análises e as visualizações.
- `varejo_limpo.csv`: base de dados tratada.
- `README.md`: documentação do projeto.

## 9. Como executar

1. Abra o notebook no Google Colab.
2. Disponibilize o arquivo CSV original no ambiente.
3. Execute as células em ordem, do início ao fim.
4. Confira os resultados e gere novamente o arquivo `varejo_limpo.csv`.

