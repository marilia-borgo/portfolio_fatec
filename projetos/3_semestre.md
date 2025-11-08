### Terceiro Semestre (2024-2)

Durante o terceiro semestre, o projeto foi desenvolvido em parceria com a empresa GSW e focado em soluções de coleta de dados para análise de mercado.

**Problema**

A **ausência de uma ferramenta automatizada** para coleta contínua e estruturada de dados de portais de notícias e APIs públicas resultava em um **processo manual custoso e ineficiente**. Isso criava um **vácuo de dados históricos robustos** e impossibilitava a aplicação de futuras análises estratégicas, incluindo o uso de inteligência artificial.

**Solução**

Desenvolvemos um **Sistema Web Full Stack (Java/Spring Boot e Vue.js)** que permite o cadastro de portais de notícias, APIs e metadados de relevância (tags/jornalistas). Implementamos um **motor de web *scraping*** que automatiza a coleta contínua de notícias, extraindo e estruturando o conteúdo para armazenamento em um **banco de dados PostgreSQL** para uso em análises futuras.

[Repositório no GitHub](https://github.com/marilia-borgo/FATEC-API-3-SEMESTRE)

#### Tecnologias Utilizadas
* **Backend:** Java 17, Spring Boot, Crawler4j, Jsoup
* **Banco de Dados:** PostgreSQL, Docker
* **Frontend:** Vue.js

#### Contribuições Pessoais
**Neste projeto, atuei como Product Owner e Desenvolvedora Full-Stack**.

Como **Product Owner**, liderei o **levantamento de requisitos** junto à empresa parceira, organizando o *backlog* e traduzindo a visão do cliente em ***user stories* claras**. Desenvolvi o ***wireframe* inicial no Figma** para alinhar as expectativas de UX (Cadastro, Edição, Listagem de APIs, Portais e Regionalismos).

Como **Desenvolvedora**, minha principal contribuição foi no **motor de *scraping*** do *backend* (Java), combinando **Crawler4j** para o rastreamento e **Jsoup** para o *parsing*. Implementei o mecanismo de **rotação de User-Agent** (`UserAgentProvider.java`) para contornar bloqueios e criei a **lógica de *parsing* inteligente** (`extractData`, `parseDate`) que utiliza **busca por palavras-chave análogas** e atributos HTML (e.g., `<time>`, `article:published_time`) para extrair data e autor, garantindo a qualidade do metadado coletado.

#### Hard Skills
* **Java e Orientação a Objetos (SOLID)** - Consigo ensinar
* **Web Scraping (Jsoup/Crawler4j)** - Consigo ensinar
* **PostgreSQL (Modelagem e Otimização)** - Consigo ensinar
* **Docker e Docker Compose** - Uso com autonomia
* **Vue.js** - Uso com autonomia

#### Soft Skills
No papel de Product Owner, a equipe era composta por membros com **diferentes níveis de experiência** em Java e desenvolvimento web.

Demonstrei **Liderança Colaborativa e Organização** ao aplicar a técnica de **desenvolvimento em pares (*pair programming*)** em tarefas críticas do *backend* e *frontend*, como a lógica de *scraping* e os componentes de cadastro em Vue.js. Essa abordagem permitiu **equilibrar a velocidade de desenvolvimento** e **nivelar o conhecimento técnico** do time, garantindo que os membros com menos experiência aprendessem a estrutura da aplicação e os mais experientes revisassem o projeto, resultando em uma entrega de *software* consistente e de alta qualidade.