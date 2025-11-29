📘 Vigilância Digital da COVID-19 em São Paulo (2020–2025) usando Google Trends
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

▶️ Como Reproduzir o Projeto

📝 Licença

👥 Autores

🙏 Agradecimentos

📘 Descrição Geral

Este repositório documenta todo o processo científico utilizado para desenvolver o estudo:

“Vigilância Digital da COVID-19 em São Paulo: Relação entre Casos Confirmados e Google Trends (2020–2025)”

O projeto investiga se dados de busca online — especialmente o termo “covid-19” — podem antecipar surtos epidemiológicos reais, funcionando como ferramenta complementar aos sistemas tradicionais de vigilância em saúde.

Este trabalho foi desenvolvido para apresentação e submissão à Revista Científica do SENAI.

🧭 Objetivo do Projeto

Avaliar se os dados do Google Trends possuem valor preditivo, isto é, se o aumento de buscas por “covid-19” ocorre antes dos aumentos nos casos confirmados de COVID-19 no Estado de São Paulo.

🔍 Hipótese central

As buscas online aumentam antes da confirmação oficial dos casos, funcionando como alerta precoce epidemiológico.

📂 Estrutura do Repositório
## 📦 Estrutura do Projeto

```bash
📦 covid-google-trends
├── 📁 data/
│   ├── 📄 casos_sp.csv                  # Casos mensais de COVID-19 (Ministério da Saúde)
│   ├── 📄 trends_sp.csv                 # Dados do Google Trends (COVID-19 - São Paulo)
│   └── 📁 indicadores_industria/        # Relatórios CNI, Abiquim, ABIT e dados industriais
│
├── 📁 notebooks/
│   └── 📓 analise_covid_trends_sp_corrigido_final.ipynb   # Notebook principal da análise
│
├── 📁 docs/
│   ├── 📄 Template_ResumoExpandido2025_Covid.docx
│   └── 📄 Apresentacao_Senai_S_C_.pptx
│
└── 📘 README.md     # Este arquivo
```

🔍 Fontes de Dados
1. Casos Confirmados – Ministério da Saúde

Período: Jan/2020 a Ago/2025

Frequência: Mensal

Pré-processado no notebook

2. Google Trends

Termo analisado: “covid-19”

Localidade: São Paulo

Escala: 0 a 100 (normalizada)

Coleta: Pytrends

3. Indicadores Industriais (CNI, Abiquim, ABIT)

Usados para relacionar comportamento digital com:

picos de interesse por “álcool em gel”

picos de interesse por “máscara respiratória”

reorganização produtiva durante a pandemia

🧪 Metodologia
✔ 1. Pré-Processamento

Carregamento das bases

Tratamento de inconsistências

Agregação mensal dos casos

Normalização das séries

Suavização usando Média Móvel de 3 Meses (MM3)

✔ 2. Análises Estatísticas
🔹 Correlação de Pearson

Avalia associação linear entre casos × buscas.

🔹 Correlação de Spearman

Mede relações monotônicas.

🔹 Correlação Cruzada (Cross-Correlation)

Teste de defasagem autocorrelação

Lags avaliados: -6 a +6 meses

🔹 Causalidade de Granger

Testa se uma série prediz a outra

Lags avaliados: 1 a 3

✔ 3. Tecnologias Utilizadas

Python 3.12

Pandas

NumPy

Matplotlib

SciPy

Statsmodels

Pytrends

📊 Resultados Principais
1. Evolução Temporal

Padrões semelhantes entre:

📈 Casos confirmados
📉 Interesse no Google Trends

Picos de 2020 e 2021 visíveis em ambas as séries

Alta sensibilidade às ondas da pandemia

2. Correlações
Comparação	Pearson	Spearman
Casos × Trends	0.74	0.80
Casos_MM3 × Trends_MM3	0.83	0.91

🟢 Conclusão: com suavização, a relação entre as séries fica ainda mais forte.

3. Análise de Defasagem (Lag)

Maior correlação ocorre em:

➤ lag = +1 mês

Interpretado como:

📌 Google Trends antecipa a evolução dos casos em aproximadamente 30 dias.

4. Causalidade de Granger

Causalidade bidirecional (p < 0.05)

Buscas → ajudam a prever casos

Casos → estimulam novas buscas

5. Impacto Industrial

Aumento abrupto nas buscas coincide com:

Explosão da demanda de álcool em gel

Reorientação das fábricas têxteis para máscaras

Escassez de produtos essenciais

Ruptura da cadeia produtiva

🧠 Conclusões do Estudo

O Google Trends funciona como indicador complementar de vigilância epidemiológica.

Há evidência sólida de que as buscas antecipam surtos no Estado de São Paulo.

Dados digitais captam percepção de risco da população antes dos registros oficiais.

Podem fornecer semanas de vantagem estratégica à gestão pública.

Combinação de dados tradicionais + digitais melhora detecção precoce.

⚠️ Limitações

Escala do Trends é normalizada, não absoluta

Cobertura midiática influencia buscas

Subnotificação nos primeiros meses da pandemia

Mudanças de comportamento ao longo dos anos

▶️ Como Reproduzir o Projeto
1. Clone o repositório
git clone https://github.com/gustavopaixao06/covid-google-trends.git
cd covid-google-trends

2. Instale as dependências
pip install -r requirements.txt

3. Execute o notebook
jupyter notebook notebooks/analise_covid_trends_sp_corrigido_final.ipynb

📝 Licença

Este projeto está licenciado sob a MIT License.
Uso livre para fins educacionais e científicos.

👥 Autores
Gustavo Campos da Paixão

Graduando em Inteligência e Análise de Dados — SENAI
Experiência em Python, SQL, MongoDB, Power BI

Evandro Miguel Martins Sperandio

Graduando em Inteligência e Análise de Dados — SENAI
Formação técnica em Desenvolvimento de Sistemas

🙏 Agradecimentos

SENAI Suíço-Brasileira “Paulo Ernesto Tolle”

Bases oficiais de saúde pública

Professores e orientadores

Comunidade científica e de dados durante a pandemia
