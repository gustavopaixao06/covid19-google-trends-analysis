📘 Vigilância Digital da COVID-19 em São Paulo (2020–2025) usando Google Trends
Análise Estatística, Modelagem Temporal e Evidências de Antecipação de Casos
📌 Descrição Geral

Este repositório documenta todo o processo científico utilizado para desenvolver o estudo:

“Vigilância Digital da COVID-19 em São Paulo: Relação entre Casos Confirmados e Google Trends (2020–2025)”

O projeto investiga se dados de busca online — especialmente o termo “covid-19” — podem antecipar surtos epidemiológicos reais, funcionando como ferramenta complementar aos sistemas tradicionais de vigilância em saúde.

Este trabalho foi desenvolvido para apresentação e submissão a revista científica do SENAI.

🧭 Objetivo do Projeto

Avaliar se os dados do Google Trends possuem valor preditivo, isto é, se o aumento de buscas por “covid-19” ocorre antes dos aumentos nos casos confirmados de COVID-19 no Estado de São Paulo.

Hipótese central:

As buscas online aumentam antes da confirmação oficial dos casos, funcionando como alerta precoce epidemiológico.

📂 Estrutura do Repositório
/
├── data/
│   ├── casos_sp.csv            # Casos mensais de COVID-19 (Ministério da Saúde)
│   ├── trends_sp.csv           # Dados Google Trends (COVID-19 - São Paulo)
│   └── indicadores_industria/  # Dados e relatórios usados na análise industrial
│
├── notebooks/
│   └── analise_covid_trends_sp_corrigido_final.ipynb   # Notebook principal
│
├── docs/
│   ├── Template_ResumoExpandido2025_Covid.docx
│   └── Apresentacao_Senai_S_C_.pptx
│
└── README.md   ← ESTE ARQUIVO

🔍 Fontes de Dados Utilizadas
1. Casos Confirmados (Ministério da Saúde)

Período: Jan/2020 a Ago/2025

Frequência: Mensal

Formato bruto → pré-processado no notebook

2. Google Trends

Termo: “covid-19”

Localidade: São Paulo

Escala: 0 a 100 (normalizado)

Coletado via API do Pytrends

3. Dados Industriais (CNI, Abiquim, ABIT)

Usados para contextualizar picos de buscas por:

“álcool em gel”

“máscara respiratória”

EPIs e insumos essenciais

Esses dados permitiram relacionar comportamentos digitais com impactos produtivos reais.

🧪 Metodologia Completa

A análise seguiu rigor metodológico, replicável via notebook incluso no repositório.

1. Pré-Processamento

Carregamento dos dados

Tratamento de inconsistências

Agregação mensal dos casos

Normalização e alinhamento temporal

Suavização com Média Móvel de 3 Meses (MM3) para redução de ruído

2. Análises Estatísticas
✔ Correlação de Pearson

Mede associações lineares

✔ Correlação de Spearman

Mede associações monotônicas

✔ Correlação Cruzada (Cross-Correlation)

Testa defasagem entre as séries (lags)

Lags testados: -6 a +6 meses

✔ Causalidade de Granger

Avalia se uma série ajuda a prever a outra

Defasagens avaliadas: 1 a 3 meses

3. Ferramentas e Tecnologias

Python 3.12

Pandas — manipulação de dados

NumPy — vetorização

Matplotlib — visualização

SciPy — estatística

Statsmodels — causalidade & séries temporais

Pytrends — coleta de tendências Google

📊 Principais Resultados
1. Evolução Temporal (Casos × Google Trends)

Padrões muito semelhantes foram observados:

Picos de casos em 2020 e 2021

Picos de interesse no Google quase simultâneos

Alta sensibilidade da população ao agravamento da pandemia

2. Correlações
Comparação	Pearson	Spearman
Casos × Trends	0.74	0.80
Casos_MM3 × Trends_MM3	0.83	0.91

🟢 Conclusão: Com suavização, as séries mostram correlação forte e consistente.

3. Correlação Cruzada (Lag Analysis)

Maior correlação ocorre em:
lag = +1 mês

Significa que o Google Trends antecipa os picos de casos em cerca de 30 dias.

🔔 Alerta epidemiológico antecipado.

4. Causalidade de Granger

Foi encontrada causalidade bidirecional com p < 0.05
→ As buscas influenciam os casos futuros
→ Os casos influenciam um novo aumento nas buscas

5. Efeitos Industriais (álcool em gel & máscaras)

Os gráficos mostram:

Picos de busca por “álcool em gel” → explosão de demanda industrial

Picos de “máscara respiratória” → reorientação das fábricas têxteis para EPIs

Reflete:

ruptura da cadeia produtiva,

escassez de insumos,

adaptações rápidas da indústria nacional.

🧠 Conclusões Gerais

O Google Trends funciona como indicador complementar de vigilância epidemiológica.

Há evidência robusta de que as buscas antecipam os surtos em São Paulo.

As séries digitais captam percepção de risco da população antes dos registros oficiais.

Indicadores online podem fornecer semanas de vantagem estratégica para a gestão pública.

O cruzamento entre dados digitais + epidemiológicos melhora a detecção precoce.

⚠️ Limitações do Estudo

Índice do Google Trends é normalizado (não absoluto).

Cobertura midiática influencia picos de buscas.

Subnotificação de casos no início da pandemia.

Mudanças de comportamento populacional ao longo dos anos.

▶️ Como Reproduzir o Projeto
1. Clone o repositório
git clone https://github.com/SEU-USUARIO/covid-google-trends.git
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
Graduando em Inteligência e Análise de Dados – SENAI
Experiência em Python, Data Analysis, MongoDB, SQL, Power BI

Evandro Miguel Martins Sperandio
Graduando em Inteligência e Análise de Dados – SENAI
Formação técnica em Desenvolvimento de Sistemas – SENAI

🙏 Agradecimentos

SENAI Suíço-Brasileira “Paulo Ernesto Tolle”

Equipes responsáveis pelas bases oficiais de saúde

Professores orientadores do projeto

Comunidade de dados que manteve repositórios ativos durante a pandemia
