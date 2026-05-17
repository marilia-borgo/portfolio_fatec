### Sexto Semestre (2026-1)

O projeto desenvolvido no sexto semestre teve como empresa parceira a **Tecsys**, empresa especializada em telemetria aplicada à distribuição de energia elétrica. A Tecsys comercializa dispositivos que monitoram a rede elétrica, e a capacidade de identificar quais consumidoras e locais perdem mais energia é estratégica para embasar decisões comerciais sobre onde instalar seus equipamentos.

**Problema**

A ANEEL disponibiliza publicamente os indicadores de continuidade DEC (Duração Equivalente de Interrupção por Unidade Consumidora) e FEC (Frequência Equivalente de Interrupção por Unidade Consumidora) por conjunto e período, mas esses dados são massivos e não estruturados. A Tecsys não possuía ferramental para processar esse volume, calcular scores de criticidade por seção da rede e identificar geograficamente os pontos mais críticos — informações essenciais para embasar decisões de negócio e priorizar a instalação de seus dispositivos de monitoramento.

**Solução**

Desenvolvemos o **Thunderstone**, uma plataforma que processa os dados regulatórios da ANEEL, padroniza os cálculos de perda e traduz os resultados em visualizações estratégicas — incluindo **heatmaps geoespaciais** e rankings que destacam geograficamente as seções mais críticas da rede elétrica.

[GIT](https://github.com/marilia-borgo/FATEC-API-6-SEMESTRE/tree/main)

#### Tecnologias Utilizadas

* **Backend:** Python, FastAPI
* **Processamento Assíncrono:** Celery, Redis
* **Banco de Dados:** MongoDB, PostgreSQL
* **Frontend:** Vue.js
* **Visualização Geoespacial:** geopandas, matplotlib
* **Infraestrutura:** Docker, Docker Compose

#### Contribuições Pessoais

**Neste projeto, atuei como Desenvolvedora Full-Stack**, com foco no pipeline de ETL e no processamento geoespacial.

Minhas principais contribuições técnicas foram:

- Implementei o **pipeline ETL para dados DEC/FEC da ANEEL**: endpoint `POST /etl/load-dec-fec` que aceita URLs de CSV e dispara tasks Celery paralelas (`etl.load_dec_fec_realizado` e `etl.load_dec_fec_limite`) para processamento chunked com logging de progresso e carga no MongoDB.
- Desenvolvi o **algoritmo de score de criticidade** para classificar seções da rede elétrica por severidade, e a **pipeline end-to-end** com chain Celery orquestrando download → cálculo de criticidade → renderização de heatmap geoespacial (geopandas/matplotlib → PNG), com os serviços `criticidade.py`, `render_criticidade.py` e `pipeline_trigger.py`.
- Implementei a **task de envio de relatório PDF por e-mail** (`task_send_report_email`) com retry automático (max=3, delay=60s) e rastreamento de status no MongoDB, eliminando falhas silenciosas no envio.
- Desenvolvi o endpoint `GET /dist/distributors` expondo dados de distribuidoras do PostgreSQL com ordenação determinística.
- Configurei o **pipeline de testes no CI** e apliquei o linter **Ruff** em todo o codebase.
- Trabalhei na análise e implementação dos requisitos de segurança para que o sistema esteja de acordo com as necessidades da LGPD (Lei geral de proteção de dados).

#### Hard Skills

* **Python / FastAPI** - Consigo ensinar
* **PostgreSQL** - Consigo ensinar
* **MongoDB** - Uso com autonomia
* **Docker** - Uso com autonomia
* **Vue.js** - Uso com autonomia
* **Celery / Redis** - Uso com ajuda
* **geopandas / matplotlib** - Uso com ajuda

#### Soft Skills

O projeto exigiu que a equipe trabalhasse com um domínio completamente fora da computação: regulação da distribuição de energia elétrica. Os indicadores DEC/FEC, os cálculos de criticidade e a estrutura dos dados da ANEEL eram desconhecidos para todos os membros da equipe.

Demonstrei **Aprendizagem Autônoma e Maturidade Técnica** ao liderar, junto à equipe, o processo de estudo necessário para superar essa barreira: consultamos professores e o próprio cliente da Tecsys para entender os cálculos corretos, identificar quais dados buscar e como interpretá-los dentro do contexto regulatório. Essa postura evitou que o desconhecimento do domínio se tornasse um bloqueio técnico e foi essencial para que o algoritmo de score de criticidade e os heatmaps geoespaciais fossem coerentes com a realidade da engenharia elétrica.
