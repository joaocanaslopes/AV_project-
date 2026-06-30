**🌾 Análise de Impacto Climático na Produtividade Agrícola (Alentejo e Algarve)**

Este repositório contém os conjuntos de dados, pipelines de processamento e modelos estatísticos desenvolvidos para avaliar o impacto de eventos climáticos extremos (secas) na produtividade de diversas culturas agrícolas nas regiões do Alentejo e do Algarve, compreendendo o período entre 2005 e 2018.

O projeto utiliza o SPI-12 (Standardized Precipitation Index a 12 meses) como indicador climatológico central para mapear a vulnerabilidade, a memória hidrológica e a resiliência ecofisiológica das diferentes espécies agrícolas.

📊 Sobre os Dados
Os dados utilizados neste estudo resultam de um processo de cruzamento e harmonização de duas fontes oficiais:

INE (Instituto Nacional de Estatística): Séries temporais de superfície (hectares), produção (toneladas) e produtividade (kg/ha) para 94 espécies agrícolas, além da capacidade de área irrigável.

IPMA (Instituto Português do Mar e da Atmosfera): Dados climatológicos, incluindo precipitação absoluta, anomalias e temperaturas (médias, máximas e mínimas), mapeados a partir das estações de referência (Beja para o Alentejo; Faro para o Algarve).

O dataset final consolidado encontra-se no ficheiro total_com_spi12.csv.

📂 Estrutura e Ordem de Leitura dos Notebooks
Para compreender o fluxo de trabalho metodológico deste projeto, recomenda-se a leitura e execução dos notebooks na seguinte ordem cronológica:

1. Data_Cleaning_and_Integration_of_Agro_Climatic_Dataset.ipynb

Objetivo: Ingestão de dados brutos do INE e IPMA, limpeza de strings, tratamento de dados ausentes, unificação espacial e exportação do ficheiro harmonizado base.

2. Analises_prodvsclima.ipynb

Objetivo: Análise Exploratória de Dados (EDA) clássica e extração de matrizes de correlação de Pearson. Demonstra as limitações de utilizar apenas a precipitação absoluta anual para explicar as quebras de produção.

3. calculate_SPI_some_analises.ipynb

Objetivo: Integração do índice probabilístico SPI-12 e quantificação matemática das quebras de produtividade média (em kg/ha) durante os períodos classificados como "Seca Severa" e "Seca Extrema".

4. analises_spi.ipynb

Objetivo: Mapeamento avançado das distribuições e dinâmicas de frequência do SPI-12. Inclui a visualização interativa das escalas de seca anuais sobrepostas aos rendimentos por espécie/região.

5. analise_impacto_climatico_agricola.ipynb

Objetivo: O núcleo inferencial do projeto. Implementa o Modelo de Regressão Linear Múltipla (OLS) para validar o "Efeito Tampão" da irrigação, o algoritmo de Machine Learning Random Forest (para importância de variáveis) e o Clustering K-Means (para segmentar o risco/resiliência das 94 culturas).

📖 Relatorio_Mestre_Agro_Climatico.ipynb

Objetivo: Documento integrador que compila toda a narrativa científica, o enquadramento teórico, os recortes de código fundamentais dos módulos anteriores e a extensa discussão de resultados finais.

⚠️ Avisos e Cuidados a Ter (Troubleshooting GitHub)
Ao navegar neste repositório diretamente pela interface do GitHub, tenha em atenção a seguinte limitação de renderização:

Erro "Invalid Notebook" no GitHub (analises_spi.ipynb):

O Módulo IV (analises_spi.ipynb) contém gráficos com widgets interativos (menus dropdown para selecionar culturas). O motor visualizador do GitHub não suporta o estado destes widgets, o que pode causar erros de renderização ("the 'state' key is missing from 'metadata.widgets'").

Solução: O ficheiro carregado neste repositório já foi limpo das saídas interativas para permitir a leitura de código no GitHub. Para testar os gráficos dinâmicos em pleno funcionamento, descarregue o ficheiro e abra-o no Google Colab ou Jupyter Notebook local, correndo as células sequencialmente.

👥 Autores
João Lopes (24842)

Lourenço Carvalho (29248)

Unidade Curricular: Data Visualization / Análise de Dados Avançada
