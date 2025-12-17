# Previsão de Preços de Veículos (Tabela FIPE)
> Trabalho realizado para a disciplina: Linguagem de Programação Aplicada no curso de Inteligência Artifical Aplicada da UFPR

## 📌 Visão Geral

Este projeto consiste na análise de dados históricos de preços de veículos no Brasil (baseados na Tabela FIPE) e na construção de modelos de Machine Learning para a previsão do preço médio (`avg_price_brl`). O trabalho envolve o pré-processamento dos dados, engenharia de atributos e a comparação de algoritmos de regressão para identificar os principais fatores que influenciam o valor dos automóveis.

## 📂 Estrutura de Arquivos

* **`precos_carros_brasil.csv`**: Dataset principal contendo o histórico de preços. As principais colunas incluem:
* `year_of_reference` e `month_of_reference`: Data de referência da tabela FIPE.
* `brand`, `model`: Marca e modelo do veículo.
* `fuel`, `gear`: Tipo de combustível e câmbio (manual/automático).
* `engine_size`: Tamanho do motor (ex: 1.0, 2.0).
* `year_model`: Ano de fabricação do modelo.
* `avg_price_brl`: Preço médio em reais (variável alvo).
* **`trabalho_IAA2.ipynb`**: Jupyter Notebook contendo o código fonte para leitura, tratamento de dados e modelagem preditiva.
* **`PDFCOLAB.pdf`**: Exportação em PDF do notebook executado.

## 🛠 Metodologia e Tecnologias

O trabalho foi desenvolvido em **Python**, utilizando as seguintes bibliotecas e técnicas:

* **Bibliotecas:** `pandas`, `numpy`, `matplotlib` (para manipulação de dados e visualização).
* **Pré-processamento:**
* Limpeza de dados.
* Codificação de variáveis categóricas: Criação de colunas numéricas para atributos como Câmbio (`gear_numeric`) e Combustível (`fuel_numeric`).
* **Modelagem (Machine Learning):**
* Treinamento de modelos de regressão para prever o preço do veículo.
* Algoritmos utilizados: **Random Forest** e **XGBoost**.



## 📊 Principais Resultados

A análise de importância das variáveis (Feature Importance) nos modelos revelou os fatores que mais impactam a precificação do veículo. Segundo as saídas do notebook, as variáveis mais influentes foram:

1. **Engine Size (Tamanho do Motor):** Grande influência na determinação do preço (aprox. 35% de importância no Random Forest).

2. **Year Model (Ano do Modelo):** O ano de fabricação é o segundo fator determinante (aprox. 29% de importância).

3. **Authentication:** A variável de autenticação apresentou alta importância (aprox. 26%), possivelmente atuando como um identificador temporal ou de versão na base de dados.

4. **Variáveis Menores:** Fatores como tipo de câmbio (`gear`) e combustível (`fuel`) tiveram impacto menor comparado ao motor e ano.


## 🚀 Como Executar
1. Certifique-se de ter o Python instalado com as bibliotecas listadas (`pip install pandas numpy matplotlib`).
2. Mantenha o arquivo `precos_carros_brasil.csv` no mesmo diretório do notebook ou carregue-o no ambiente (ex: Google Colab).
3. Execute as células do `trabalho_IAA2.ipynb` sequencialmente para reproduzir o pré-processamento e o treinamento dos modelos.
