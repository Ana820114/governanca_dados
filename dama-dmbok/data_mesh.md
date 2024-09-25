# Data Mesh

## Arquitetura Data Mesh
A arquitetura **Data Mesh** traz uma nova abordagem para trabalhar com dados, baseada na combinação de conceitos e práticas consolidadas. A inovação não está em criar novas tecnologias ou ferramentas, mas em uma filosofia diferente para lidar com os dados:

- **Data**: Enxergar os dados como parte essencial da estratégia executiva e tecnológica da organização.
- **Product Thinking**: Tratar os dados como produtos, em vez de projetos ou serviços, proporcionando uma ótima experiência aos usuários.
- **Distributed Domain-Driven Design Architecture**: Organizar os dados com base nos domínios de negócio, distribuindo autonomia e responsabilidade. Essa arquitetura é influenciada por práticas como Domain-Driven Design (DDD), microservices e service mesh.
- **Self-Service Platform Design**: Reduzir a complexidade para os usuários através de uma plataforma de autosserviço, que oferece padrões, protocolos e ferramentas independentes do domínio.

Fonte: [Data Mesh Trends](https://www.datanami.com/2022/01/21/data-meshes-set-to-spread-in-2022/)

## Princípios do Data Mesh
A arquitetura Data Mesh é fundamentada em quatro princípios principais:

1. **Domain Ownership**:
   - A propriedade dos dados é distribuída entre diferentes equipes e domínios de negócio, em vez de ser gerenciada por um único time centralizado.

2. **Data as a Product**:
   - Os dados são tratados como produtos, com equipes multifuncionais responsáveis por criar, gerenciar e manter os dados com o foco na qualidade e usabilidade.

3. **Self-Service Data Platform**:
   - Fornecer uma plataforma de dados autosserviço que permita aos domínios criar e consumir dados de forma independente, evitando duplicação de esforços.

4. **Federated Computational Governance**:
   - Implementar uma governança federada, onde cada equipe/dono de produto tem autonomia para gerenciar seus dados, mas segue regras globais para garantir a interoperabilidade e a saúde do ecossistema de dados.

## Arquitetura de Dados Descentralizada Orientada ao Domínio
O primeiro princípio do Data Mesh é mover a propriedade dos dados de um time centralizado para times distribuídos, organizados por domínios de negócio. Nessa arquitetura, os dados analíticos são modelados e geridos de acordo com domínios específicos. 

### Exemplo:
No contexto de um e-commerce, poderíamos ter os seguintes domínios:
- **Domínio de Clientes**: Forneceria APIs para obter todos os clientes (um por linha) ou disponibilizar estatísticas, como o número de clientes ativos e inadimplentes.
- **Domínio de Pedidos**: Poderia disponibilizar informações detalhadas sobre os pedidos realizados pelos clientes, com foco no ciclo de vida do pedido.

## Dados Disponibilizados como Produto
O **Data Mesh** trata os dados como produtos. Cada fonte de dados tem seu próprio dono, que pertence a uma equipe multifuncional de engenheiros de dados, sendo responsável pela qualidade e governança dos dados. Isso cria uma arquitetura distribuída, onde a responsabilidade é claramente definida e orientada ao domínio.

## Plataforma de Dados Self-Service
Uma infraestrutura **self-service** é essencial para o **Data Mesh**, permitindo que as equipes autônomas dos domínios de negócio criem seus produtos de dados de forma rápida e eficiente. A plataforma self-service reduz a duplicação de esforços e promove a agilidade no desenvolvimento de produtos de dados.

## Governança Federada
A **governança federada** no Data Mesh garante que cada dono de produto de dados tenha autonomia em suas decisões, enquanto segue um conjunto de regras globais que se aplicam a todos os produtos de dados e suas interfaces. O objetivo é manter um equilíbrio entre a descentralização, que promove a autonomia dos domínios, e a centralização, que garante um ecossistema interoperável e saudável.

### Desafios:
- Manter o equilíbrio entre a centralização (regras globais) e a descentralização (autonomia local).
- Criar um modelo de governança federada eficaz que permita flexibilidade e controle.

## Fontes de Pesquisa para Data Mesh
- [Data Mesh Learning](https://www.datameshlearning.com)
