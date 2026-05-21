### Quarto Semestre (2025-1)

O projeto desenvolvido no quarto semestre, denominado **TerraVision**, foi realizado no âmbito do curso de Banco de Dados e teve como parceira a **Visiona Tecnologia Espacial**, joint-venture entre a Embraer Defesa & Segurança e a Telebras, especializada em integração de sistemas espaciais, sensoriamento remoto e serviços baseados em satélites aplicados a setores como agricultura, defesa e meio ambiente.

**Problema**

Modelos de Inteligência Artificial usados na agricultura para mapeamento de evidências (como perdas em lavouras) possuem **deficiências na precisão de seus resultados**. Estas deficiências estão ligadas à **limitação do treinamento com amostras eficientes** (dados de *benchmark*). Há a necessidade de uma ferramenta que permita a **visualização, edição geoespacial e análise de dados em tempo real** para melhorar os resultados produzidos pelos modelos automáticos.

**Solução**

Desenvolvemos o **TerraVision**, um Sistema WEB para manipulação e gerenciamento de dados espaciais. O sistema suporta **três perfis de usuário (administrador, consultor e analista)** e permite o **Cadastro de Fazendas e Talhões** (incluindo upload de GeoJson). A funcionalidade crucial é a **Edição de Geometrias** (ferramenta de desenho/edição vetorial), permitindo que o **Analista** realize o **QA (Qualidade Assegurada)** dos resultados da IA, podendo **aprovar, reprovar ou editar** a geometria diretamente no banco de dados espacial.

[Repositório Principal](https://github.com/MarcyLeite/fatec-api-4)

#### Tecnologias Utilizadas
* **Backend:** Java, Spring Boot (APIs RESTful), Hibernate/JPA
* **Banco de Dados:** PostgreSQL, **PostGIS** (Extensão Geoespacial)
* **Frontend:** Vue.js, Leaflet (Visualização e Edição de Mapas)

#### Contribuições Pessoais
**Neste projeto, atuei como Desenvolvedora Full-Stack**, com foco na arquitetura do banco de dados e na camada de persistência.

Minha principal contribuição técnica foi na **integração Geoespacial do *backend* (Spring Boot)**. Fui responsável pela **modelagem de dados** para entidades espaciais, como `talhao` e `daninha`, no **PostgreSQL**, utilizando a extensão **PostGIS** para armazenar as **geometrias GeoJSON**. Implementei os *endpoints* de **API RESTful** para o **CRUD de entidades mestras** (`fazenda`, `talhao`) e dei suporte à *User Story* de **Edição de Geometrias (S2-1)**, garantindo que o *backend* recebesse e atualizasse corretamente os dados geoespaciais modificados no *frontend* (Leaflet).

#### Hard Skills
* **Java/Spring Boot (API RESTful)** - Uso com autonomia
* **PostGIS/PostgreSQL (Geometria)** - Consigo ensinar
* **Hibernate/Spring Data JPA** - Uso com autonomia
* **Vue.js/Leaflet** - Uso com autonomia

#### Soft Skills
O projeto exigiu uma integração complexa entre o *frontend* (Vue/Leaflet) e o *backend* Geoespacial (PostGIS).

Demonstrei **Resolução de Problemas Técnicos e Comunicação Colaborativa** ao atuar como ponte entre as equipes de *frontend* e *backend*, traduzindo os requisitos de manipulação do mapa em **contratos de API (GeoJSON)** válidos. Essa intermediação garantiu que a **Edição de Geometrias (S2-1)** funcionasse perfeitamente, superando os desafios da comunicação de dados espaciais e garantindo a qualidade da principal funcionalidade do sistema.