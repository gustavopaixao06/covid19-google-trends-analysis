📘 VIGILÂNCIA DIGITAL DA COVID-19 EM SÃO PAULO (2020–2025) USANDO GOOGLE TRENDS
Análise Estatística, Modelagem Temporal e Evidências de Antecipação de Casos
🏷️ Badges
<p> <img src="https://img.shields.io/badge/Python-3.12-blue.svg" /> <img src="https://img.shields.io/badge/Status-Concluído-brightgreen" /> <img src="https://img.shields.io/badge/License-MIT-yellow.svg" /> <img src="https://img.shields.io/badge/Data%20Science-Project-orange" /> <img src="https://img.shields.io/badge/Google%20Trends-Analysis-red" /> </p>
📑 SUMÁRIO

📘 Descrição Geral

🧭 Objetivo do Projeto

📂 Estrutura do Repositório

🔍 Fontes de Dados

🧪 Metodologia

📊 Resultados Principais

🧠 Conclusões do Estudo

⚠️ Limitações

▶️ Como Reproduzir

📝 Licença

👥 Autores

🙏 Agradecimentos

📘 DESCRIÇÃO GERAL

Este repositório documenta todo o processo científico utilizado para desenvolver o estudo:

“Vigilância Digital da COVID-19 em São Paulo: Relação entre Casos Confirmados e Google Trends (2020–2025)”

O projeto investiga se dados de busca online — especialmente o termo “covid-19” — podem antecipar surtos epidemiológicos reais, funcionando como ferramenta complementar aos sistemas tradicionais de vigilância em saúde.

🧭 OBJETIVO DO PROJETO

Avaliar se os dados do Google Trends possuem valor preditivo — isto é, se o aumento de buscas por “covid-19” ocorre antes dos aumentos nos casos confirmados de COVID-19 no Estado de São Paulo.

🔍 Hipótese central

As buscas online aumentam antes da confirmação oficial dos casos.

📂 ESTRUTURA DO REPOSITÓRIO
📦 Estrutura do Projeto
📦 covid-google-trends
├── 📁 data/
│   ├── 📄 casos_sp.csv
│   ├── 📄 trends_sp.csv
│   └── 📁 indicadores_industria/
│
├── 📁 notebooks/
│   └── 📓 analise_covid_trends_sp_corrigido_final.ipynb
│
└── 📘 README.md

🔍 FONTES DE DADOS
1. Casos Confirmados – Ministério da Saúde

Período: 2020–2025
Frequência: Mensal
Pré-processado no notebook

2. Google Trends

Termo: “covid-19”
Localidade: São Paulo
Escala normalizada (0–100)

3. Indicadores Industriais

CNI, Abiquim, ABIT — para analisar impacto econômico/industrial.

🧪 METODOLOGIA
✔ 1. Pré-Processamento

Carregamento das bases

Tratamento de inconsistências

Agregação mensal

Normalização

Suavização (MM3)

✔ 2. Análises Estatísticas
🔹 Correlação de Pearson
🔹 Correlação de Spearman
🔹 Correlação Cruzada (Cross-Correlation)

Lags: -6 a +6 meses

🔹 Causalidade de Granger

Lags: 1 a 3

✔ 3. Tecnologias

Python 3.12 • Pandas • NumPy • SciPy • Statsmodels • Matplotlib • Pytrends

📊 RESULTADOS PRINCIPAIS
1. Evolução Temporal

Tendências semelhantes entre casos e buscas.

2. Correlações
Comparação	Pearson	Spearman
Casos × Trends	0.74	0.80
Casos_MM3 × Trends_MM3	0.83	0.91
3. Defasagem (Lag)

Maior correlação em lag = +1 mês
➡️ Trends antecipa casos em ~30 dias.

4. Causalidade de Granger

Causalidade bidirecional (p < 0.05)

5. Impacto Industrial

Picos no Trends coincidem com:

Demanda por álcool em gel

Máscaras

Reorganização produtiva

🧠 CONCLUSÕES DO ESTUDO

Google Trends funciona como indicador complementar.

Antecipação de surtos é visível.

Dados digitais captam percepção pública rapidamente.

Integração de dados digitais + tradicionais é poderosa.

⚠️ LIMITAÇÕES

Escala normalizada do Trends

Influência da mídia

Subnotificações

Mudança de comportamento social

▶️ COMO REPRODUZIR
git clone https://github.com/gustavopaixao06/covid-google-trends.git
cd covid-google-trends
pip install -r requirements.txt
jupyter notebook notebooks/analise_covid_trends_sp_corrigido_final.ipynb

📝 LICENÇA

MIT License — livre para uso acadêmico e científico.

👥 AUTORES

Gustavo Campos da Paixão
Graduando em IAD — SENAI

Evandro Miguel Martins Sperandio
Graduando em IAD — SENAI

🙏 AGRADECIMENTOS

SENAI Suíço-Brasileira

Bases oficiais de saúde pública

Professores e orientadores

Comunidade científica
