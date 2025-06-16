<div>
📊 TelecomX - Análise Exploratória de Dados (EDA)<br>
Este repositório contém um projeto de Análise Exploratória de Dados (EDA) realizado com o dataset TelecomX, focado na análise de clientes, serviços contratados, churn e perfil de cobrança.

📂 Sobre o Projeto<br>
O objetivo deste projeto é realizar uma análise detalhada de um dataset fictício de uma operadora de telecomunicações, buscando entender:

Perfil dos clientes<br>

Distribuição dos serviços contratados<br>

Fatores relacionados ao cancelamento de clientes (Churn)<br>

Comportamento de receita mensal e total<br>

Insights iniciais para estratégias de retenção<br>

🛠️ Tecnologias e Bibliotecas Usadas<br>
Python 3.x

Pandas (manipulação de dados)<br>

Requests (consumo da API JSON)<br>

Matplotlib e Seaborn (visualização de dados)<br>

📈 Etapas da Análise<br>
1️⃣ Importação dos Dados<br>
Os dados foram obtidos via uma API JSON hospedada no GitHub:<br>

python<br>

import pandas as pd<br>
import requests<br>
import matplotlib.pyplot as plt<br>
import seaborn as sns<br>
Fonte: TelecomX_Data.json<br>

Normalização dos dados com pandas.json_normalize.<br>

2️⃣ Tratamento e Transformação dos Dados (ETL)<br>
Padronização dos nomes das colunas para snake_case.

Remoção de registros com customerid ausente.<br>

Conversão de colunas numéricas (charges.monthly, charges.total) para tipo numérico.<br>

Análise de estatísticas descritivas iniciais.<br>

3️⃣ Visualizações e Insights<br>
📌 Churn por Tipo de Contrato<br>
Identificação de onde ocorre mais cancelamento.<br>

📌 Média de Receita Mensal por Tipo de Internet<br>
Análise da relação entre serviço de internet e ticket médio.<br>

📌 Distribuição de Tempo de Contrato (Tenure)<br>
Entendimento do ciclo de vida dos clientes.<br>

📌 Matriz de Correlação<br>
Análise das relações entre as variáveis numéricas (tenure, receita mensal e total).<br>

📌 Distribuição por Gênero<br>
Verificação da distribuição demográfica básica.<br>

4️⃣ Análise de Serviços Contratados<br>
Análise da quantidade de clientes em cada serviço:<br>

Serviço de telefonia<br>

Multiplas linhas<br>

Tipo de internet<br>

Segurança online<br>

Backup online<br>

Proteção de dispositivos<br>

Suporte técnico<br>

Streaming de TV<br>

Streaming de filmes<br>

Exemplo de análise de frequências:v

python<br>

for servico in servicos:<br>
    print(df[servico].value_counts(dropna=False))<br>
    
✅ Principais Insights<br>
Contratos mensais apresentam maior taxa de churn.<br>

Clientes com serviços de fibra ótica tendem a pagar mais mensalmente.<br>

Há correlação positiva entre o tempo de contrato e o valor total pago.<br>

A base de clientes tem distribuição de gênero relativamente equilibrada.<br>

📌 Como Executar<br>
Clone o repositório:<br>

bash<br>

git clone https://github.com/alessandrobra/TelecomX-EDA.git<br>
Instale as dependências:<br>

bash<br>

pip install pandas requests matplotlib seaborn<br>
Execute o notebook ou o script Python.<br>

📍 Possíveis Extensões Futuras<br>
Construção de um modelo preditivo de churn.<br>

Análise de segmentação de clientes.<br>

Dashboard interativo com Streamlit ou Power BI.<br>

👨‍💻 Autor<br>
Alessandro - Cientista de Dados em formação<br>
Conecte-se comigo no LinkedIn   www.linkedin.com/in/alessandro-brasil<br>
</div>

