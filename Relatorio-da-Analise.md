📊 Relatório de Análise Exploratória de Dados (EDA) – TelecomX
Projeto: Análise de Clientes e Churn
Data da Análise: 16/06/2025
Analista Responsável: Alessandro (Analista de Dados)

1. Introdução
O objetivo desta análise foi entender o perfil dos clientes da TelecomX, identificar fatores relacionados ao cancelamento de clientes (Churn), analisar padrões de cobrança, serviços contratados e o comportamento geral da base.

Os dados foram extraídos de uma API pública em formato JSON e passaram por um processo de ETL (Extração, Transformação e Carga) para garantir qualidade e consistência.

2. Qualidade dos Dados
Total de registros após limpeza: 7.043 clientes

Removemos registros sem CustomerID, garantindo integridade das análises.

Realizamos conversão dos campos numéricos relacionados a cobranças (Monthly Charges e Total Charges).

3. Análise de Churn (Cancelamento de Clientes)
📌 Churn por Tipo de Contrato:
Clientes com contratos mensais apresentam a maior taxa de cancelamento (Churn).

Contratos anual e bianual têm taxas significativamente menores de churn, indicando que contratos de longo prazo são mais estáveis.

📈 Gráfico: Churn por Tipo de Contrato (apresentado no relatório gráfico).

4. Receita Mensal Média por Tipo de Internet
Clientes com serviços de fibra ótica (Fiber optic) apresentam a maior média de cobrança mensal, mas também estão mais propensos ao churn.

Clientes sem internet ou com DSL têm uma cobrança mensal menor.

📈 Gráfico: Média da Cobrança Mensal por Tipo de Internet.

5. Distribuição do Tempo de Contrato (Tenure)
A maioria dos clientes tem menos de 20 meses de contrato.

Há uma concentração relevante de clientes com tempo muito curto de permanência (0 a 10 meses), o que pode indicar uma janela crítica de churn.

📈 Gráfico: Distribuição do Tempo de Contrato.

6. Correlação entre Variáveis Numéricas
Variáveis	Correlação
Tenure x Monthly Charges	0.11
Tenure x Total Charges	0.83 ✅ (forte)
Monthly Charges x Total Charges	0.65 ✅ (moderada)

➡️ Interpretação:
Quanto maior o tempo de contrato (tenure), maior o total pago pelo cliente (Total Charges), o que era esperado. Existe uma correlação moderada entre a cobrança mensal e o total acumulado.

📈 Gráfico: Mapa de Calor (Heatmap) da Correlação.

7. Distribuição por Gênero
A base de clientes está bem equilibrada entre Gênero Masculino e Feminino.

Não foi observada grande diferença de churn entre os gêneros.

📈 Gráfico: Distribuição por Gênero.

8. Perfil de Contratação de Serviços
Quantidade de Clientes por Serviço Prestado:
Serviço	Quantidade de Clientes
Phone Service	Alta adesão
Multiple Lines	Aproximadamente 50% têm
Internet Service	Predominância de Fiber optic e DSL
Online Security	Baixa adesão
Online Backup	Baixa adesão
Device Protection	Baixa adesão
Tech Support	Baixa adesão
Streaming TV	Uso considerável
Streaming Movies	Uso considerável

➡️ Ponto de Atenção:
Serviços de segurança e suporte técnico têm baixa penetração na base. São oportunidades para estratégias de upsell.

9. Conclusões e Recomendações
Principais Insights:
✅ Contratos mensais têm maior risco de churn.
✅ Clientes com fibra ótica pagam mais, mas também estão mais propensos a sair.
✅ A maioria dos clientes é recente (baixo tenure), o que exige ações de retenção logo nos primeiros meses.

Recomendações:
Foco em retenção para clientes com menos de 12 meses de contrato.

Campanhas para migração de contratos mensais para planos de maior duração (anual/bianual).

Cross-sell de serviços com baixa adesão (segurança, backup, suporte técnico).

Monitorar mais de perto os clientes de Fiber Optic com alto valor de mensalidade.
