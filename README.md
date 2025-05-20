# 📦 Projeto de Análise de Dados - Olist Vendas & Satisfação do Cliente

Este projeto tem como objetivo realizar uma análise exploratória e visual dos dados de um e-commerce brasileiro (base Olist), visando identificar padrões, insights e correlações entre variáveis como avaliação dos clientes, tempo de entrega, volume de vendas e desempenho dos vendedores.

---

## 📊 Objetivos da Análise

- Compreender os principais fatores que influenciam a **satisfação do cliente**
- Avaliar a **eficiência logística** com base no tempo de entrega
- Analisar o **desempenho dos vendedores** quanto a vendas, entregas e avaliações
- Explorar a **relação entre distância e valor do frete**
- Criar um **dashboard analítico** com visualizações claras e interativas

---

## 🧰 Tecnologias e Bibliotecas Utilizadas

- **Python**: Linguagem principal
- **Pandas**: Manipulação de dados tabulares
- **Plotly**: Visualizações interativas
- **Seaborn & Matplotlib**: Visualizações estáticas
- **DuckDB**: Consultas SQL diretamente em DataFrames
- **Scikit-learn**: Modelagem preditiva com Random Forest
- **Jupyter Notebook**: Ambiente de desenvolvimento interativo

---

## 🗂️ Estrutura dos Dados

Os dados são compostos por diversos arquivos `.csv` representando aspectos diferentes do e-commerce:

| Dataset                       | Descrição                         |
|------------------------------|------------------------------------|
| olist_orders_dataset.csv     | Dados dos pedidos                 |
| olist_customers_dataset.csv  | Dados dos clientes                |
| olist_order_items_dataset.csv| Itens dos pedidos                 |
| olist_order_reviews.csv      | Avaliações dos clientes           |
| olist_order_payments.csv     | Pagamentos                        |
| olist_products_dataset.csv   | Produtos vendidos                 |
| olist_sellers_dataset.csv    | Vendedores                        |
| olist_geolocation_dataset.csv| Localizações (CEP, UF, cidade)    |
| product_category_translation.csv | Tradução de categorias       |

---

## 🧠 Etapas do Projeto

### 1. 📥 Carregamento dos Dados

Todos os datasets foram carregados com `pandas.read_csv()` e preparados para análise.

### 2. 🔍 Análise Exploratória (EDA)

Foram investigados:
- Volume e estrutura dos dados
- Valores ausentes
- Estatísticas descritivas
- Correlações

### 3. 🧩 Integração dos Dados

Os datasets foram integrados utilizando chaves como `order_id`, `customer_id` e `seller_id` para criar uma visão unificada das operações.

### 4. 📈 Visualizações e Dashboards

- **Boxplots**: Avaliação x Tempo de Entrega
- **Gráficos de barras**: Vendas por vendedor, Categoria por nota
- **Mapas e gráficos interativos (Plotly)**: Avaliação, frete e distância
- **Dashboard analítico**: Visão geral do desempenho dos vendedores

### 5. 🧪 Modelagem Preditiva

Foi treinado um modelo de **Random Forest Classifier** para prever a **avaliação do cliente** com base em variáveis como:
- Tempo de entrega
- Preço total do pedido
- Número de itens
- Localização do vendedor e cliente

---

## 📊 Principais Insights

- Há **correlação negativa entre tempo de entrega e avaliação** do cliente: quanto mais demorado, menor a nota.
- Vendedores com **melhor logística** tendem a ter maior satisfação.
- O **valor do frete cresce proporcionalmente à distância**, mas há outliers devido a promoções ou frete fixo.
- Clientes de regiões metropolitanas geralmente recebem mais rápido.

---

## 📋 Dashboard do Projeto

O dashboard interativo apresenta:

- Ranking de vendedores por satisfação, vendas e entrega
- Gráficos de dispersão: Avaliação x Tempo
- Boxplots de avaliação por categoria
- Frete médio por UF e distância

---

## 🚀 Como Executar o Projeto

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/olist-analise-vendas.git
cd olist-analise-vendas
