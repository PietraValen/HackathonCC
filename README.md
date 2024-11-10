# HackathonCC

Análise e Previsão de Temperaturas com Python
Este projeto realiza a análise de uma série temporal de dados de temperatura, incluindo a geração de dados sintéticos, visualização, decomposição da série, detecção de anomalias e previsão de temperatura utilizando o modelo ARIMA.

Funcionalidades
Geração de Dados Sintéticos: Criação de dados de temperatura diária com tendência sazonal e ruído aleatório.
Visualização de Dados: Plotagem dos dados de temperatura simulados.
Decomposição da Série Temporal: Decomposição da série em tendências e sazonalidade para análise detalhada.
Detecção de Anomalias: Identificação de temperaturas anômalas, utilizando uma abordagem baseada em desvios padrão.
Previsão de Temperatura: Previsão de temperatura para os próximos 7 dias com o modelo ARIMA.
Requisitos
Para executar o projeto, você precisará das seguintes bibliotecas Python:

bash
Copiar código
pip install pandas numpy matplotlib statsmodels
Como Usar
Carregar Dados Sintéticos:

python
Copiar código
dados = carregar_dados_sinteticos()
Gera dados de temperatura simulados para análise.

Decompor Série Temporal:

python
Copiar código
decompor_serie(dados)
Decompõe os dados de temperatura em componentes de tendência, sazonalidade e ruído.

Detectar e Visualizar Anomalias:

python
Copiar código
anomalies = detectar_anomalias(dados)
visualizar_anomalias(dados, anomalies)
Detecta e plota as anomalias na série de temperatura.

Prever Temperatura para os Próximos Dias:

python
Copiar código
previsao = prever_temperatura(dados, dias=7)
Realiza a previsão de temperatura para os próximos 7 dias e visualiza o resultado junto ao histórico.

Estrutura de Código
carregar_dados_sinteticos(): Gera dados sintéticos de temperatura com uma tendência sazonal.
decompor_serie(dados): Decompõe e exibe os componentes da série.
detectar_anomalias(dados): Identifica anomalias com base em limites de desvio padrão.
visualizar_anomalias(dados, anomalies): Visualiza as anomalias em um gráfico de dispersão.
prever_temperatura(dados, dias=7): Executa previsões futuras de temperatura usando o modelo ARIMA.
Exemplo de Execução Completa
python
Copiar código
dados = carregar_dados_sinteticos()
decompor_serie(dados)
anomalies = detectar_anomalias(dados)
visualizar_anomalias(dados, anomalies)
previsao = prever_temperatura(dados)

# Visualizar previsão final
plt.figure(figsize=(10, 5))
plt.plot(dados, color='blue', label='Histórico de Temperaturas')
plt.plot(previsao, color='green', label='Previsão de Temperatura')
plt.legend()
plt.show()

Este código gera e analisa dados de temperatura diários, com etapas de decomposição, detecção de anomalias e previsão dos próximos 7 dias.
