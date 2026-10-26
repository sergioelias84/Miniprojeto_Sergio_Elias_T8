# Miniprojeto_Sergio_Elias_T8
# Mini Projeto — Análise Exploratória de Dados (AED) no Varejo

**Aluno:** Sergio Elias  
**Turma:** T8  
**Projeto:** Análise Exploratória de Dados aplicada ao varejo

## 1. Objetivo

Desenvolver uma Análise Exploratória de Dados (AED) utilizando Python e Pandas para examinar uma base de dados de varejo, identificar problemas de qualidade, tratar os dados e gerar informações úteis para a compreensão do negócio.

## 2. Origem dos dados

A base utilizada é a base Varejo indicada no enunciado da atividade.

Fonte: [Kaggle — Base Varejo](https://www.kaggle.com/datasets/namespaiva/base-varejo/data)

Arquivo original: `pedidos_diagnostico.csv`

## 3. Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Google Colab
- GitHub

## 4. Etapas do projeto

1. Leitura do arquivo CSV e inspeção dos registros, colunas e tipos de dados.
2. Diagnóstico de valores ausentes, duplicatas, textos vazios e inconsistências.
3. Limpeza e padronização dos dados, conforme os problemas encontrados.
4. Criação de funções reutilizáveis para tratamento e resumo dos dados.
5. Cálculo de estatísticas descritivas, aplicação de filtros e agrupamentos.
6. Visualização dos pedidos e do faturamento por dia.
7. Exportação da base tratada para `varejo_limpo.csv`.

## 5. Decisões de limpeza

Os dados foram inspecionados antes do tratamento. Foram verificadas ocorrências de valores ausentes, duplicatas e inconsistências textuais.

As decisões de limpeza devem preservar os registros válidos e evitar a remoção de compras distintas. Valores ausentes foram tratados ou mantidos conforme a análise de cada coluna, e a padronização textual foi aplicada para reduzir diferenças de escrita.

As quantidades finais e as decisões específicas estão documentadas no notebook.

## 6. Processo de leitura, transformação e gravação

A leitura da base foi realizada com `pandas.read_csv()`. As transformações foram realizadas com funções Python e operações do Pandas para tratar os dados e executar as análises. Ao final, a base tratada foi exportada para `varejo_limpo.csv` utilizando `to_csv(index=False)`, evitando a inclusão do índice como uma coluna adicional.

## 7. Resultados e conclusões

As conclusões devem apresentar de três a seis resultados numéricos efetivamente obtidos no notebook, uma recomendação baseada nos dados e uma limitação da análise.

- Maior e menor faturamento diário: conforme os resultados apresentados no notebook.
- Faturamento total e médio diário: conforme os cálculos realizados.
- Quantidade total e média de pedidos: conforme os cálculos realizados.
- Recomendação: utilizar os resultados para orientar análises posteriores sobre o desempenho das vendas.
- Limitação: os resultados dependem da qualidade, da abrangência e do significado dos registros presentes na base.

## 8. Arquivos do repositório

- `MiniProjeto_AED_Varejo_Sergio_Elias_T8.ipynb`: notebook com o código, as análises e as visualizações.
- `varejo_limpo.csv`: base de dados tratada.
- `README.md`: documentação do projeto.

## 9. Como executar

1. Abra o notebook no Google Colab.
2. Disponibilize o arquivo CSV original no ambiente.
3. Execute as células em ordem, do início ao fim.
4. Confira os resultados e gere novamente o arquivo `varejo_limpo.csv`.

## 10. Limitação da análise

Os resultados descrevem os dados disponíveis e não devem ser generalizados para períodos ou operações que não estejam representados na base.
