### Segundo Semestre (2024-1)

O projeto desenvolvido no segundo semestre do curso é a continuação do trabalho iniciado no período anterior e teve como empresa parceira a própria Fatec. Os requisitos foram apresentados pelo professor Emanuel Mineda, que assumiu o papel de cliente final.

**Problema**

Analistas e pesquisadores que dependem de dados climáticos para o planejamento estratégico perdem tempo valioso na **consolidação manual e validação** de dados. As bases de dados públicas são fragmentadas, com **múltiplos arquivos CSV por estação**, variando o formato e dificultando a padronização. Essa situação acarreta **inconsistência de registros, lentidão na obtenção de relatórios confiáveis** e exige **retrabalho** constante, comprometendo a tomada de decisões baseadas em métricas climáticas.

**Solução**

Desenvolvemos um **Sistema de Banco de Dados Relacional (PostgreSQL)** que centraliza, valida e organiza dados climáticos brutos de múltiplas estações. A solução permite o **carregamento automatizado de arquivos CSV**, com **validação inteligente** para identificar e isolar registros suspeitos (valores de risco). O sistema oferece **funcionalidades completas de gerenciamento** de estações, cidades e unidades de medida, além de possibilitar a **geração de relatórios customizados** (valor médio por data/hora e situacional), garantindo a integridade dos dados para análise.

[GIT](https://github.com/marilia-borgo/API-2-semestre)

#### Tecnologias Utilizadas
- **Backend:** Java
- **Banco de Dados:** Postgres
- **Frontend:** JavaFx

#### Contribuições Pessoais
**Neste projeto, atuei como Desenvolvedor e Scrum Master**.

Minha contribuição principal no segundo semestre (Sprint 4) foi na **implementação das telas e *controllers* de Gerenciamento de Dados Mestres e na funcionalidade de correção de erros**. Eu desenvolvi o **`ManageCitiesController.java`** e o **`ManageStationsController.java`**, que implementam as operações de **CRUD (*Create, Read, Update, Delete*)** com validação de chaves estrangeiras (`id_cidade`) antes da exclusão, garantindo a integridade referencial do banco de dados. Além disso, implementei o **`SeeInconsistenciesController.java`** para permitir a edição de valores suspeitos diretamente na tabela, utilizando um **`TextInputDialog`** com **`TextFormatter`** para forçar a entrada de ponto flutuante no padrão Java, e o método **`ajustarValoresDataFile`** para persistir as correções na estrutura de dados.

#### Hard Skills
* **Java** - Uso com autonomia
* **PostgreSQL** - Uso com autonomia
* **JavaFX/Scene Builder** - Uso com autonomia

#### Soft Skills
No papel de Scrum Master, a equipe era composta por membros com **diferentes níveis de experiência** em Java e desenvolvimento com banco de dados. Minha função foi crucial para **equilibrar a velocidade de desenvolvimento** e **nivelar o conhecimento técnico** do time.

Demonstrei **Liderança Colaborativa e Organização** ao aplicar a técnica de **desenvolvimento em pares (*pair programming*)** em tarefas críticas do banco de dados (como as consultas BoxPlot e a lógica de persistência do CRUD). Essa abordagem permitiu que os membros com menos experiência aprendessem a **estrutura do código de persistência (JDBC)** e os membros mais experientes revisassem o projeto, garantindo uma **entrega consistente** e um **ritmo de trabalho coeso**, mesmo diante dos diferentes *speeds* individuais.