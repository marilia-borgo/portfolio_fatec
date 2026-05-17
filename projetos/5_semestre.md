### Quinto Semestre (2025-2)

O projeto desenvolvido no quinto semestre teve como empresa parceira a **Necto**, consultoria especializada em análise de dados e inteligência de negócios.

**Problema**

A Necto gerenciava múltiplos projetos simultâneos no Jira, mas a plataforma nativa não permite comparações entre projetos nem uma visão consolidada. O acompanhamento era feito projeto a projeto dentro do próprio Jira, tornando impossível visualizar métricas de progresso, esforço e custo das equipes de forma comparativa, o que fragmentava e atrasava a tomada de decisão.

**Solução**

Desenvolvemos o **Jibóia**, um sistema ETL que consome dados da API do Jira, consolida-os em um data warehouse e gera indicadores, dashboards e quadros de acompanhamento. A plataforma oferece visão consolidada entre múltiplos projetos, permitindo comparar progresso, horas trabalhadas por desenvolvedor e custo por projeto em um único painel.

[GIT](https://github.com/marilia-borgo/FATEC-API-5-SEMESTRE/tree/main)

#### Tecnologias Utilizadas

* **Backend:** Python, Django
* **Frontend:** Vue.js, TypeScript
* **Banco de Dados:** PostgreSQL
* **Infraestrutura:** Docker, AWS
* **Qualidade de Código:** SonarQube
* **APIs:** Jira

#### Contribuições Pessoais

Neste projeto, **atuei como Product Owner nas Sprints 1 e 2 e como Desenvolvedora na Sprint 3**, após a fusão com outro grupo de projeto.

Como **Product Owner**, conduzi o levantamento de requisitos junto à Necto diretamente via Slack, organizei o backlog e as user stories, e produzi a documentação inicial de produto, mantendo contato contínuo com o cliente para validar entregas e propor soluções conforme os problemas surgiam.

Com a fusão das equipes, migrei para o papel de **Desenvolvedora**, aplicando meu conhecimento técnico onde geraria maior impacto. Minhas principais contribuições técnicas foram:

- Implementei o **cron job de healthcheck da API do Jira** (`django-crontab`) com a classe `JiraService` seguindo o padrão **Strategy**, para garantir extensibilidade para a conexão com outras apis. Inclui testes unitários com mocks e gestão de segredos via Docker e GitHub Secrets.
- Desenvolvi a feature de **visão geral do projeto** (`project_overview_svc.py`), com cálculo de burndown, conversão de horas (segundos → horas), contagem de issues por status e os endpoints `list_projects_general` e `project_overview`.
- Implementei o serviço `get_project_developers()` para **agregar horas trabalhadas e custo por desenvolvedor** a partir dos dados de TimeLog, com campo `valor_hora`, ordenação por horas e cobertura completa de testes de view e service.
- Desenvolvi o **sistema de permissões de usuário** end-to-end: no backend (Django), apliquei o decorator `@ajax_login_required` em 6+ endpoints, implementei respostas 401 para acesso anônimo e criei fixtures de cliente autenticado nos testes; no frontend (Vue.js), implementei RBAC (Controle de Acesso Baseado em Funções) para ocultar custos do projeto para perfis não-gerentes.
- Configurei os **pre-commit hooks** do repositório e corrigi problemas no pipeline do SonarQube.
- Fiz o deploy automático da plataforma utilizando o github actions para atualização a cada merge na main, antes de aplicar o deploy também fiz a análise completa de requisitos para a análise de servidores adequados as necessidades da aplicação.

#### Hard Skills

* **Python / Django** - Consigo ensinar
* **Vue.js / TypeScript** - Uso com autonomia
* **PostgreSQL** - Uso com autonomia
* **Docker** - Uso com autonomia
* **AWS** - Uso com ajuda
* **SonarQube** - Uso com ajuda

#### Soft Skills

Demonstrei **Adaptabilidade e Visão de Equipe** ao migrar voluntariamente do papel de Product Owner para Desenvolvedora após a fusão com outro grupo. Com o aumento do tamanho da equipe, identifiquei que minha experiência técnica seria mais valiosa na execução do que na gestão de produto, e realizei a transição sem necessidade de direcionamento externo.

Como Product Owner, demonstrei **Comunicação com o Cliente** ao manter contato direto e contínuo com a Necto via Slack, validando entregas e propondo soluções à medida que os problemas surgiam. Essa comunicação proativa garantiu que os requisitos permanecessem alinhados com as necessidades reais do cliente durante toda a execução do projeto.
