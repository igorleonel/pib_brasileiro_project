# Projeto de Análise e Visualização de Dados: PIB e IDEB no Brasil

Neste projeto, exploramos e visualizamos duas bases de dados: o Produto Interno Bruto (PIB) dos estados brasileiros entre 2002 e 2020 e o Índice de Desenvolvimento da Educação Básica (IDEB) de 2005 a 2021. Para a extração e transformação dos dados, utilizamos o BigQuery, enquanto a manipulação e visualização foram realizadas em Python com as bibliotecas Matplotlib, Seaborn e Plotly. Esses dados foram retirados do site [basedosdados.or](https://basedosdados.org/).

O objetivo do projeto foi apresentar diferentes tipos de visualização de dados e aprender a escolher as mais adequadas para responder a perguntas e atender demandas analíticas. Durante a execução, utilizamos gráficos de composição e de relacionamento para gerar insights visuais sobre as tendências econômicas e educacionais do Brasil.

## Base de dados:
 
1. [Tabela com os PIBs (Produto Interno Bruto) dos estados brasileiros no período de 2002 - 2020](https://basedosdados.org/dataset/96eab476-5d30-459b-82be-f888d4d0d6b9?table=bc84dea9-1126-4423-86d2-8835e6b19a72)
2. [Tabela com a pontuação do IDEB (Índice de Desenvolvimento da Educação Básica) das escolas à nivel nacional](https://basedosdados.org/dataset/fcf025ca-8b19-4131-8e2d-5ddb12492347?table=93007431-7ce9-42ee-8740-8c2274d345ad)

## Paleta de cores:

As cores utilizadas neste projeto foram cuidadosamente selecionadas para garantir uma visualização clara e atraente dos dados. A paleta de cores aplicada foi escolhida com base em ferramentas como o [Coolor](https://coolors.co/palettes/trending) e o [imagecolorpicker](https://imagecolorpicker.com/), proporcionando contraste adequado e harmonia visual. As principais cores utilizadas no projeto são:

|Azul||||||
|------|------|------|------|------|------|
| AZUL1 |AZUL2 |AZUL3 |AZUL4 |AZUL5 |AZUL6 |
|#174A7E | #4A81BF | #6495ED| #2596be | #94AFC5 | #CDDBF3 |
|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/AZUL1.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/AZUL2.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/AZUL3.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/AZUL4.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/AZUL5.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/AZUL6.png) |

&nbsp;

|Cinza||||||
|------|------|------|------|------|------|
| CINZA1 |CINZA2 |CINZA3 |CINZA4 |CINZA5|BRANCO|
|#231F20 | #414040| #555655 | #A6A6A5| #BFBEBE |#FFFFFF|
| ![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/CINZA1.png)  |![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/CINZA2.png) |![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/CINZA3.png) |![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/CINZA4.png) |![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/CINZA5.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/BRANCO.png)|

&nbsp;

|Vermelho|||Verde|||
|------|------|------|------|------|------|
| VERMELHO1 |VERMELHO2 |LARANJA1 | VERDE1 |VERDE2 | VERDE3 |
|#C3514E | #E6BAB7 | #F79747|#0C8040 | #9ABB59 |#9ECCB3|
| ![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/VERMELHO1.png) |![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/VERMELHO2.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/LARANJA1.png)| ![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/VERDE1.png) |![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/VERDE2.png)|![adicionar desc](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/paleta_cores/VERDE3.png)|

&nbsp;

## Visualizações que exploraremos

Na imagem abaixo, apresentamos um diagrama com diversos tipos de **visualização de dados** (criado por [Andrew Abela](https://extremepresentation.com/wp-content/uploads/choosing-a-good-chart-09-1.pdf)) em que é possível perceber **4 subgrupos**, dentre eles:

- Comparação
- Distribuição
- Relacionamento
- Composição

![Diagrama de Visualização de Dados (Andrew Abela - Traduzido por Afonso Rios)](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/imagens/Tipos_Graficos/Diagrama%20de%20Visualiza%C3%A7%C3%A3o%20de%20Dados%20(Andrew%20Abela%20-%20Traduzido%20por%20Afonso%20Rios).png)

Para este projeto focamos nos subgrupos da Composição e Relacionamento, levando em conta as observações que gostaríamos de apresentar em nosso portfólio.

### Gráficos de Composição

Neste projeto, vamos explorar diversos gráficos de composição dentre eles:

- Gráficos de Setores (Pizza e Rosca)
- Gráficos de Cascata
- Gráficos de Colunas Agrupadas
- Gráficos de Barras e Colunas Empilhadas
- Gráficos de Áreas
- Gráficos de Inclinação
- Treemap (Gráfico de Árvore)

### Gráficos de Relacionamento

Neste projeto, vamos explorar diversos gráficos de relacionamento dentre eles:

- Gráficos de Dispersão com linha de tendência
- Gráficos de Dispersão com cores
- Gráficos de Bolhas

## Questionamentos Explorados

Durante a análise dos dados, exploramos uma série de perguntas-chave para compreender melhor as dinâmicas econômicas e educacionais do Brasil. Os questionamentos que guiamos neste projeto incluem:

**1. Houve uma significativa mudança na distribuição do PIB por região comparando os valores de 2002 e 2020?**   

**2. Qual a participação da Região Norte nos valores agregados da indústria de todo Brasil nos anos de 2010 e 2020? Podemos notar algum comportamento?**   

**3. Qual a participação do Estado de Minas Gerais no PIB de todo o Brasil no ano de 2020?**
   
**4. Como está distribuído o PIB do Estado da Bahia em 2020, separado por impostos líquidos e os valores adicionados brutos dos bens e serviços produzidos?**
   
**5. Qual a evolução anual do PIB do Estado do Rio de Janeiro entre os anos de 2010 a 2020?**
   
**6. Qual a evolução anual do valor agregado de serviços na Região Nordeste entre os anos de 2016 a 2020?**
   
**7. Como está distribuído o PIB nos três últimos quinquênios dos dados (2010, 2015, 2020) na Região Sul do Brasil, divididos pelos Estados (Paraná, Santa Catarina e Rio Grande do Sul)?**
   
**8. Como estão distribuídos, em porcentagem, os valores adicionados de bens e serviços descritos na base de dados em relação a cada região no ano de 2020?**
   
**9. Como está composto os valores agregados brutos dos bens e serviços (em valor absoluto) em relação aos Estados da região Norte no ano de 2020?**
    
**10. Na agropecuária, como estão distribuídos seus valores adicionados por região dentro do período da base dos dados (2002 - 2020)?**
    
**11. Qual foi a variação do PIB relativo à indústria nas regiões do Brasil nos anos de 2010, 2015 e 2020?**
 
**12. Qual a relação entre as notas das disciplinas de língua portuguesa e matemática no SAEB por região no Ensino Fundamental Anos Iniciais? Conseguimos traçar algum paralelo entre elas?**
    
**13. Qual seria a relação entre a taxa de aprovação e a média da nota do SAEB no Ensino Fundamental Anos Finais? Conseguimos notar como as duas se distribuem em relação ao IDEB e as regiões?**

**14. Qual a relação entre as notas das disciplinas de língua portuguesa e matemática do SAEB no Ensino Fundamental Anos Finais no período das 5 últimas avaliações?**

**15. Qual seria a relação entre as notas do SAEB no Ensino Médio? Conseguimos notar como as duas se comportam em relação a taxa de aprovação e as regiões?**

Cada uma dessas perguntas será abordada utilizando um tipo específico de visualização de dados, juntamente com elementos visuais como anotações, destaques e legendas para focar a atenção do público nas informações mais importantes e nos insights que queremos destacar.

## Gráficos Produzidos

Para verificar um resumo com os principais gráficos gerados ao projeto clique nesse [link](https://github.com/igorleonel/pib_ideb_brasileiro_project/blob/main/project_pib_ideb_gr%C3%A1ficos_produzidos.ipynb) e para ver o projeto completo, acesse este [link](https://colab.research.google.com/drive/1KjAPYQ39CnmgacX5GfLiB47quSZL_Z4e?usp=sharing)

## Conclusão

Este projeto teve como objetivo explorar diferentes tipos de visualização de dados e demonstrar como escolher a mais adequada para representar as análises de acordo com os questionamentos e demandas apresentadas. Durante o desenvolvimento, utilizamos gráficos de composição e relacionamento dos dados, partindo do uso de bibliotecas amplamente empregadas em Python, como Matplotlib, Seaborn e Plotly. Também personalizamos as visualizações com recursos adicionais, como anotações, destaques, legendas e outras técnicas de visualização, para garantir uma comunicação clara e eficaz dos insights.

Ao final do projeto, conseguimos gerar visualizações personalizadas, focadas no público-alvo e nas informações mais relevantes, tornando os dados mais acessíveis e informativos.
