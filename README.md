# Análise Exploratória de Dados --- Sample Superstore

## 1. Identificação do projeto

**Título:** Análise Exploratória de Dados --- Sample Superstore\
**Autor:** Cleber Rocha de Camargo\
**Linguagem:** Python\
**Ambiente:** Google Colab\
**Dataset:** Sample Superstore (`.csv`)

## 2. Objetivo do projeto

O projeto tem como objetivo realizar uma Análise Exploratória de Dados
(AED) sobre uma base pública de vendas da rede varejista Sample
Superstore.

A análise busca compreender o desempenho comercial da empresa,
explorando vendas, lucro, margem de lucro, categorias, subcategorias,
regiões, segmentos de clientes, descontos e evolução temporal.

## 3. Etapas do desenvolvimento

### 3.1 Importação e compreensão dos dados

Foi realizada a importação do dataset e a exploração inicial de sua
estrutura, incluindo:

-   verificação das variáveis disponíveis;
-   análise dos tipos de dados;
-   estatísticas descritivas;
-   avaliação das principais características do conjunto de dados.

A base analisada possui **9.994 registros e 21 variáveis**.

### 3.2 Tratamento e preparação dos dados

Foram realizadas as seguintes verificações e tratamentos:

-   verificação de valores nulos;
-   verificação de registros duplicados;
-   conversão das colunas `Order Date` e `Ship Date` para o formato de
    data;
-   verificação da nomenclatura e organização das colunas;
-   identificação de possíveis valores atípicos utilizando o método do
    Intervalo Interquartil (IQR).

Não foram identificados valores nulos ou registros duplicados, portanto
não foi necessário realizar exclusões ou preenchimentos por esses
motivos.

Os outliers identificados foram mantidos, pois valores elevados de
vendas, lucro ou quantidade podem representar transações comerciais
legítimas e relevantes para a análise.

### 3.3 Análise exploratória

Foram utilizados filtros, ordenações, agrupamentos (`groupby`),
estatísticas descritivas e visualizações gráficas.

Entre as análises realizadas estão:

-   vendas por categoria;
-   lucro e margem por categoria;
-   desempenho por região;
-   desempenho por segmento de clientes;
-   análise das subcategorias;
-   relação entre desconto e lucro;
-   evolução das vendas e do lucro ao longo do tempo;
-   análise de períodos e meses;
-   identificação de produtos com resultados negativos;
-   análise de possíveis outliers.

## 4. Principais decisões no tratamento dos dados

As principais decisões foram:

-   manter os registros sem valores nulos;
-   manter os registros sem duplicidades;
-   converter as variáveis de data para permitir análises temporais;
-   utilizar o método IQR para identificação de possíveis outliers;
-   manter os valores atípicos identificados quando não havia evidência
    suficiente de erro de registro;
-   preservar as variáveis originais para evitar perda de informações
    relevantes.

## 5. Principais insights

Os principais resultados obtidos na análise foram:

-   A categoria **Technology** apresentou o maior faturamento, lucro e
    margem entre as categorias analisadas, com aproximadamente **US\$
    836.154,03 em vendas**, **US\$ 145.454,95 em lucro** e **17,40% de
    margem**.
-   A categoria **Furniture** apresentou aproximadamente **US\$ 742 mil
    em vendas**, mas margem de lucro de apenas **2,49%**, indicando
    baixa rentabilidade em relação às demais categorias.
-   Descontos elevados apresentaram associação com resultados médios de
    lucro negativos. Para descontos de **30% ou mais**, o lucro médio
    identificado foi de aproximadamente **US\$ -97,18**.
-   A região **West** apresentou o maior faturamento e lucro entre as
    regiões analisadas.
-   O segmento **Home Office** apresentou a maior margem de lucro entre
    os segmentos analisados.
-   Na análise das subcategorias, **Copiers** destacou-se pelo maior
    lucro absoluto, enquanto **Tables** apresentou o pior resultado, com
    prejuízo e margem negativa.
-   A análise temporal indicou crescimento das vendas e do lucro ao
    longo do período analisado, com destaque para **2017**.
-   Foi observada maior concentração dos resultados no segundo semestre,
    especialmente nos meses de **setembro, novembro e dezembro**.
-   A análise de outliers mostrou que valores extremos existem na base,
    mas podem representar operações comerciais legítimas; por isso,
    foram mantidos para não eliminar informações potencialmente
    relevantes.

## 6. Resultados gerais

Os principais indicadores calculados foram:

-   **Total de vendas:** US\$ 2.297.200,86
-   **Total de lucro:** US\$ 286.397,02
-   **Margem de lucro geral:** 12,47%
-   **Total de pedidos distintos:** 5.009

Esses indicadores foram utilizados como referência para a avaliação
geral do desempenho comercial da base.

## 7. Visualizações

As visualizações utilizadas para apoiar a interpretação dos dados estão
presentes no notebook, juntamente com os respectivos códigos e
resultados.

### Relação entre Desconto e Lucro

![Relação entre Desconto e Lucro](relacao_desconto_lucro.png)

### Vendas e Lucro por Categoria

![Vendas e Lucro por Categoria](vendas_lucro_categoria.png)

### Evolução das Vendas

![Evolução das Vendas](evolucao_vendas.png)

### Lucro por Subcategoria

![Lucro por Subcategoria](lucro_subcategoria.png)

## 8. Como executar o projeto

1.  Abrir o notebook
    `Análise_Exploratória_de_Dados_Sample_Superstore.ipynb` no Google
    Colab ou em um ambiente Jupyter compatível.
2.  Disponibilizar o arquivo `Sample - Superstore.csv` no ambiente de
    execução.
3.  Executar as células do notebook na ordem apresentada.
4.  Aguardar a execução das etapas de importação, tratamento, análise
    exploratória e geração das visualizações.
5.  Consultar a seção de principais insights e conclusões ao final do
    notebook.

### Bibliotecas utilizadas

-   Pandas
-   NumPy
-   Matplotlib
