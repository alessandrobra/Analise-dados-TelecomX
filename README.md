📊 TelecomX - Análise Exploratória de Dados (EDA)
Este repositório contém um projeto de Análise Exploratória de Dados (EDA) realizado com o dataset TelecomX, focado na análise de clientes, serviços contratados, churn e perfil de cobrança.

📂 Sobre o Projeto
O objetivo deste projeto é realizar uma análise detalhada de um dataset fictício de uma operadora de telecomunicações, buscando entender:

Perfil dos clientes

Distribuição dos serviços contratados

Fatores relacionados ao cancelamento de clientes (Churn)

Comportamento de receita mensal e total

Insights iniciais para estratégias de retenção

🛠️ Tecnologias e Bibliotecas Usadas
Python 3.x

Pandas (manipulação de dados)

Requests (consumo da API JSON)

Matplotlib e Seaborn (visualização de dados)

📈 Etapas da Análise
1️⃣ Importação dos Dados
Os dados foram obtidos via uma API JSON hospedada no GitHub:

python
Copiar
Editar
import pandas as pd
import requests
import matplotlib.pyplot as plt
import seaborn as sns
Fonte: TelecomX_Data.json

Normalização dos dados com pandas.json_normalize.

2️⃣ Tratamento e Transformação dos Dados (ETL)
Padronização dos nomes das colunas para snake_case.

Remoção de registros com customerid ausente.

Conversão de colunas numéricas (charges.monthly, charges.total) para tipo numérico.

Análise de estatísticas descritivas iniciais.

3️⃣ Visualizações e Insights
📌 Churn por Tipo de Contrato
Identificação de onde ocorre mais cancelamento.

📌 Média de Receita Mensal por Tipo de Internet
Análise da relação entre serviço de internet e ticket médio.

📌 Distribuição de Tempo de Contrato (Tenure)
Entendimento do ciclo de vida dos clientes.

📌 Matriz de Correlação
Análise das relações entre as variáveis numéricas (tenure, receita mensal e total).

📌 Distribuição por Gênero
Verificação da distribuição demográfica básica.

4️⃣ Análise de Serviços Contratados
Análise da quantidade de clientes em cada serviço:

Serviço de telefonia

Multiplas linhas

Tipo de internet

Segurança online

Backup online

Proteção de dispositivos

Suporte técnico

Streaming de TV

Streaming de filmes

Exemplo de análise de frequências:

python
Copiar
Editar
for servico in servicos:
    print(df[servico].value_counts(dropna=False))
✅ Principais Insights
Contratos mensais apresentam maior taxa de churn.

Clientes com serviços de fibra ótica tendem a pagar mais mensalmente.

Há correlação positiva entre o tempo de contrato e o valor total pago.

A base de clientes tem distribuição de gênero relativamente equilibrada.

📌 Como Executar
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seu-usuario/TelecomX-EDA.git
Instale as dependências:

bash
Copiar
Editar
pip install pandas requests matplotlib seaborn
Execute o notebook ou o script Python.

📍 Possíveis Extensões Futuras
Construção de um modelo preditivo de churn.

Análise de segmentação de clientes.

Dashboard interativo com Streamlit ou Power BI.

👨‍💻 Autor
Alessandro - Cientista de Dados em formação
Conecte-se comigo no LinkedIn   www.linkedin.com/in/alessandro-brasil


