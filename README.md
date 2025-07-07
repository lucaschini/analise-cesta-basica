# Análise Exploratória de Dados da Cesta Básica

## Descrição do Projeto

Este projeto integrador e extensionista tem como objetivo central a criação de um dashboard interativo no Power BI, utilizando dados processados em Python, para sintetizar e analisar informações sobre os preços da cesta básica no município de Campinas. A iniciativa visa monitorar e analisar sistematicamente os preços dos itens que compõem a cesta básica, a fim de compreender sua evolução e os impactos causados sobre a população, especialmente as camadas mais vulneráveis, em face de fatores como inflação, instabilidade econômica e desigualdade social.

Os dados utilizados foram disponibilizados pelo Projeto Institucional Observatório PUC-Campinas. A análise contempla cinco abordagens distintas que buscam explorar diferentes aspectos da variação de preços ao longo do tempo , incluindo a evolução do valor total da cesta básica, a variação individual dos itens, a análise específica do preço do arroz e do feijão, a proporção do salário-mínimo comprometido com a cesta básica, e uma projeção futura de preços via regressão linear.

Este trabalho se alinha diretamente com a ODS 2 – Fome Zero e Agricultura Sustentável , contribuindo para a sensibilização da sociedade civil, o apoio à tomada de decisão por parte do poder público, e o fortalecimento do controle social, estimulando ações que mitiguem a insegurança alimentar na região. O projeto busca oferecer uma ferramenta de visualização acessível e compreensível, que fomenta o debate sobre segurança alimentar e justiça social.

## Tecnologias Utilizadas

O desenvolvimento deste projeto foi realizado utilizando as seguintes tecnologias e bibliotecas Python:

* **Python**: Linguagem de programação principal.
    * **Pandas**: Essencial para a manipulação, leitura e análise dos dados em formato de tabelas (DataFrames).
    * **NumPy**: Utilizado para operações numéricas e suporte a arrays.
    * **Seaborn**: Para a criação de visualizações estatísticas atraentes e informativas.
    * **Matplotlib**: Para a personalização e renderização de gráficos.
* **Microsoft Power BI**: Ferramenta de Business Intelligence utilizada para a criação de um dashboard interativo para visualização dos resultados.

## Estrutura e Processo do Projeto

O fluxo de trabalho deste projeto está dividido nas seguintes etapas principais:

1.  **Carregamento dos Dados**:
    * O projeto inicia carregando dois conjuntos de dados a partir de arquivos Excel:
        * `data.xlsx`: Contém informações de preço médio por item da cesta básica ao longo do tempo, com colunas como `Mes_Ano_Data`, `PRODUTO` e `Preço_Medio_Item`.
        * `quantidades.xlsx`: Contém as quantidades padrão de cada item da cesta básica, com colunas como `Item` e `Qtde`.
    * As primeiras linhas de ambos os DataFrames são exibidas para uma inspeção inicial da estrutura dos dados, garantindo a integridade dos dados de entrada.

2.  **Análise Exploratória de Dados (EDA) e Integração**:
    * Após o carregamento, o notebook prossegue com a exploração dos dados. Esta etapa inclui:
        * Verificação da estrutura dos DataFrames (tipos de dados, presença de valores nulos, etc.).
        * Análise descritiva dos preços médios dos itens individualmente.
        * **União dos DataFrames**: Para calcular o custo total da cesta básica e analisar seu comportamento, os DataFrames `df` (preços) e `df_quantidades` são combinados. Essa integração é realizada utilizando a operação `merge` do Pandas, que associa os preços médios de cada produto às suas respectivas quantidades na cesta básica. Isso permite a criação de uma base de dados unificada, essencial para o cálculo do custo ponderado da cesta.
        * Cálculo e visualização de tendências de preços ao longo dos meses e anos, tanto para itens individuais quanto para o custo total da cesta.

3.  **Dashboard no Power BI**:
    * Os dados tratados e as análises geradas no ambiente Python são exportados para um formato compatível (por exemplo, CSV ou Excel) para serem utilizados no Power BI.
    * Um dashboard interativo é desenvolvido no Power BI, permitindo a visualização dinâmica dos seguintes aspectos:
        * Evolução do custo total da cesta básica ao longo do tempo.
        * Preços médios por produto, com filtros por período.
        * Comparação de preços entre diferentes produtos ou períodos.
        * Gráficos e tabelas resumindo os principais insights da análise.
    * O dashboard proporciona uma interface amigável para explorar os dados e identificar tendências e anomalias de forma intuitiva.

**O dashboard pode ser acessado neste link** [Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYjJkNTNlOTQtNjQyZi00NzNlLTk0ZDYtNjFiMDk2ZmI5Nzg1IiwidCI6IjA4MGJjMDIzLTVlNWEtNDZmYi1iYmU4LWViNTQ4ZTk4NzNhNiJ9)

## Resultados Atingidos

* Preços da cesta básica em Campinas mostram instabilidade e tendência de alta;
* Nota-se um impacto significativo no orçamento das famílias de baixa renda causado pelos preços dos itens da cesta básica;
* A ferramenta de visualização de dados (PowerBI) apoia decisões públicas e conscientização social;
* Nota-se a importância de políticas para conter inflação alimentar e garantir segurança alimentar.
