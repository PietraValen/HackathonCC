# HackathonCC

Análise e Previsão de Temperaturas com Python
Este projeto realiza a análise de uma série temporal de dados de temperatura, incluindo a geração de dados sintéticos, visualização, decomposição da série, detecção de anomalias e previsão de temperatura utilizando o modelo ARIMA.

#Funcionalidades
1. **Geração de Dados Sintéticos**: Criação de dados de temperatura diária com tendência sazonal e ruído aleatório.
2. **Visualização de Dados**: Plotagem dos dados de temperatura simulados.
3. **Decomposição da Série Temporal**: Decomposição da série em tendências e sazonalidade para análise detalhada.
4. **Detecção de Anomalias**: Identificação de temperaturas anômalas utilizando uma abordagem baseada em desvios padrão.
5. **Previsão de Temperatura**: Previsão de temperatura para os próximos 7 dias com o modelo ARIMA.


#Requisitos
Para executar o projeto, você precisará das seguintes bibliotecas Python:

bash
Copiar código

pip install pandas numpy matplotlib statsmodels

#Como Usar
Carregar Dados Sintéticos:


python

Copiar código

dados = carregar_dados_sinteticos()
Gera dados de temperatura simulados para análise.

#Decompor Série Temporal:

python

Copiar código

decompor_serie(dados)
Decompõe os dados de temperatura em componentes de tendência, sazonalidade e ruído.

#Detectar e Visualizar Anomalias:

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
==========================================================================================================================================

  # 2 CODIGO ALTERNATIVO

# Análise e Previsão de Temperaturas com Dados Sintéticos

Este projeto realiza a análise de uma série temporal de dados sintéticos de temperatura, abarcando visualização, decomposição da série, detecção de anomalias e previsão de temperatura para os próximos 30 dias utilizando o modelo ARIMA.

## Funcionalidades

1. **Geração de Dados Sintéticos**: Criação de dados de temperatura com variação sazonal e ruído aleatório para os últimos três anos.
2. **Visualização de Dados**: Gráfico de temperatura diária simulada.
3. **Decomposição da Série Temporal**: Separação da série em componentes de tendência, sazonalidade e ruído.
4. **Detecção de Anomalias**: Identificação de valores anômalos na série utilizando limites de desvio padrão.
5. **Previsão de Temperatura**: Estimativa de temperatura para os próximos 30 dias usando o modelo ARIMA.

## Requisitos

Para executar o projeto, instale as seguintes bibliotecas Python:

pip install pandas numpy matplotlib statsmodels

#Como Usar
Geração de Dados Sintéticos:

python
Copiar código
dados = carregar_dados_sinteticos()

Cria uma série de temperatura simulada, com valores diários, tendência sazonal e ruído aleatório.

Decomposição da Série Temporal:

python
Copiar código

decompor_serie(dados)

Exibe os componentes da série de temperatura em gráficos para análise de tendência e sazonalidade.

Detecção e Visualização de Anomalias:

python
Copiar código
anomalies = detectar_anomalias(dados)
visualizar_anomalias(dados, anomalies)
Identifica temperaturas anômalas com base em desvios padrão e as exibe em um gráfico.

Previsão de Temperatura para os Próximos 30 Dias:

python
Copiar código
previsao = prever_temperatura(dados, dias=30)
Realiza a previsão de temperatura futura e exibe a estimativa em conjunto com os dados históricos.

Estrutura de Código

carregar_dados_sinteticos(): Gera uma série temporal de temperatura com dados sintéticos.
decompor_serie(dados): Decompõe a série e exibe os componentes em um gráfico.
detectar_anomalias(dados): Retorna valores que ultrapassam o limite superior ou inferior de 2 desvios padrão.
visualizar_anomalias(dados, anomalies): Exibe as anomalias detectadas em um gráfico de temperatura.
prever_temperatura(dados, dias=30): Faz a previsão para os próximos 30 dias com o modelo ARIMA.

Exemplo de Execução Completa

python
Copiar código

# Carregar dados e executar análise completa

dados = carregar_dados_sinteticos()
decompor_serie(dados)
anomalies = detectar_anomalias(dados)
visualizar_anomalias(dados, anomalies)
previsao = prever_temperatura(dados)

# Exibir gráfico de previsão final

plt.figure(figsize=(10, 5))
plt.plot(dados, color='blue', label='Histórico de Temperaturas')
plt.plot(previsao, color='green', label='Previsão de Temperatura')
plt.legend()
plt.show()

Este script realiza a análise e previsão de temperatura, visualizando tendências, detectando anomalias e projetando dados futuros de maneira visual e funcional.
