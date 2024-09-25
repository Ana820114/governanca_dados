# Bancos de Dados NoSQL e Relacionais

## Bancos de Dados NoSQL

### Descrição
NoSQL é um termo genérico que define bancos de dados não-relacionais. Desenvolvido por empresas líderes da Internet como Google, Facebook, Amazon e LinkedIn, a tecnologia NoSQL surgiu para superar as limitações dos bancos de dados relacionais, especialmente para aplicações web modernas. Não significa que seus modelos não possuam relacionamentos, mas sim que não são orientados a tabelas. O termo "NoSQL" é uma abreviação de "Not Only SQL" (não apenas SQL).

### Características
- **Escalabilidade Horizontal**: Permite a adição de mais servidores para lidar com o aumento de carga, ao contrário da escalabilidade vertical dos bancos relacionais.
- **Ausência de Esquema ou Esquema Flexível**: Não requer um esquema fixo, facilitando a adaptação a mudanças na estrutura de dados.
- **Suporte a Replicação**: Permite a cópia dos dados em múltiplos servidores para garantir alta disponibilidade e redundância.
- **API Simples**: Geralmente possui interfaces mais simples para operações de leitura e escrita.
- **Consistência Eventual**: Nem sempre prioriza a consistência imediata dos dados em favor da disponibilidade e partição.

### Ausência de Esquema
A ausência de esquema ou esquema flexível é uma característica fundamental dos bancos de dados NoSQL. Esta característica permite uma alta escalabilidade e disponibilidade, pois os dados podem ser armazenados sem a necessidade de um esquema fixo. No entanto, essa flexibilidade pode comprometer a integridade dos dados, um aspecto que é garantido no modelo relacional.

### Exemplos de Bancos de Dados NoSQL
- **Aerospike**: Famoso por sua velocidade de memória, ideal para empresas que precisam de respostas em milissegundos, como aquelas em anúncios e jogos.
- **Apache Cassandra**: Destaca-se pela modelagem de dados NoSQL e escalabilidade linear flexível, utilizando clusters.
- **Amazon DynamoDB**: Desenvolvido pela Amazon para suportar seu e-commerce com alta escalabilidade, inspirou outros projetos NoSQL.
- **MongoDB**: O banco de dados NoSQL mais popular, conhecido por sua facilidade de desenvolvimento e manejo flexível dos dados.
- **HBase**: Funciona sobre o HDFS (Hadoop Distributed File System), oferecendo grande escalabilidade e integração com Hadoop.
- **Redis**: Um banco de dados NoSQL do tipo chave-valor, amplamente utilizado para cache e armazenamento rápido.

## Bancos de Dados Relacionais

### Descrição
Os Bancos de Dados Relacionais (RDBMS) são projetados para armazenar dados de forma estruturada em tabelas, seguindo o modelo relacional. Utilizam a linguagem SQL (Structured Query Language) para manipulação e consulta dos dados.

### Elementos Básicos
- **Relações (Tabelas)**: Estruturas que armazenam dados em formato de linhas e colunas.
- **Registros (Tuplas)**: Cada linha de uma tabela que representa uma instância de dados.

### Características Fundamentais
- **Restrições de Integridade**: Regras que garantem a precisão e consistência dos dados, como:
  - **PK (Primary Key)**: Identificador único para cada registro.
  - **FK (Foreign Key)**: Estabelece relações entre tabelas.
  - **UK (Unique Key)**: Garante valores únicos em uma coluna.
  - **CK (Check Key)**: Valida dados inseridos.
  - **NN (Not Null)**: Garante que uma coluna não tenha valores nulos.

### Exemplos de Bancos de Dados Relacionais
- **MySQL**: Sistema de gerenciamento de banco de dados relacional open-source, amplamente utilizado em aplicações web.
- **PostgreSQL**: Conhecido por sua conformidade com os padrões SQL e extensibilidade.
- **Oracle Database**: Um dos principais sistemas de banco de dados comerciais, com ampla gama de funcionalidades e ferramentas.
- **Microsoft SQL Server**: Oferece integração com o ambiente Microsoft e suporte a grandes volumes de dados.

## Referências

- [NoSQL Tutorial - Guru99](https://www.guru99.com/nosql-tutorial.html)
- [Comparação entre Bancos de Dados Relacionais e NoSQL - OpenClassrooms](https://openclassrooms.com/en/courses/5671741-design-the-logical-model-of-your-relational-database/6255746-compare-relational-and-nosql-databases)
- [Bancos de Dados NoSQL - FileCloud](https://www.filecloud.com/blog/2014/08/leading-nosql-databases-to-consider/)

# Modelos de Banco de Dados NoSQL

## Introdução
Os bancos de dados NoSQL são projetados para lidar com grandes volumes de dados e oferecer flexibilidade além dos modelos relacionais tradicionais. Eles se dividem em quatro categorias principais:

1. **Chave-Valor (Key-Value)**
2. **Orientado a Grafos**
3. **Orientado a Colunas (Column Family)**
4. **Orientado a Documentos**

## Modelos de NoSQL

### 1. Chave-Valor (Key-Value)
- **Descrição**: O modelo mais simples de banco de dados NoSQL. Visualiza-se o banco como uma grande tabela, onde cada item é identificado por uma chave única e associado a um valor.
- **Características**:
  - Cada entrada é composta por uma chave e um valor.
  - Simples e eficiente para operações de leitura e escrita rápidas.
  - Ideal para cache e sessões.

### 2. Orientado a Grafos
- **Descrição**: Este modelo é projetado para representar e consultar dados com relações complexas. Consiste em nós (vértices), relacionamentos (arestas) e propriedades (atributos).
- **Características**:
  - **Nós (Vértices)**: Entidades ou objetos.
  - **Relacionamentos (Arestas)**: Conexões entre os nós.
  - **Propriedades**: Atributos que descrevem nós e relacionamentos.
  - Utilizado para consultas complexas, como redes sociais e sistemas de recomendação.
- **Exemplo de Uso**: Aplicações que precisam consultar conexões entre entidades, como "Quais cidades foram visitadas anteriormente por pessoas que foram para Nova Iorque?"

### 3. Orientado a Colunas (Column Family)
- **Descrição**: Projetado para armazenar e processar grandes quantidades de dados distribuídos em várias máquinas. As colunas são organizadas em famílias e são indexadas por uma tripla (coluna, linha e timestamp).
- **Características**:
  - Dados armazenados em colunas em vez de linhas.
  - Permite o armazenamento de múltiplas versões de um dado através do uso de timestamps.
  - Ideal para grandes volumes de dados e consultas de leitura rápida.
- **Exemplo de Uso**: Modelagem de dados onde diferentes atributos de um item (como endereço e cidade) são armazenados em diferentes famílias de colunas.

### 4. Orientado a Documentos
- **Descrição**: Armazena dados em documentos estruturados e indexados, geralmente no formato JSON. Esses documentos podem conter dados complexos e hierárquicos.
- **Características**:
  - **JSON (JavaScript Object Notation)**: Formato compacto e legível por humanos, utilizado para troca de dados.
  - Permite consultas detalhadas em documentos e manipulação flexível de dados.
  - Ideal para aplicações que requerem uma estrutura de dados dinâmica e hierárquica.
- **Exemplo de Uso**: Armazenamento de dados de usuários em um formato JSON com atributos e metadados associados.

### JSON
- **Descrição**: JSON (JavaScript Object Notation) é um formato de troca de dados leve e fácil de ler e escrever por humanos. Utiliza um formato de atributo-valor e é independente de linguagem.
- **Características**:
  - **Formato**: Texto legível por humanos.
  - **Utilização**: Troca de dados entre sistemas e armazenamento de dados estruturados.

### MongoDB
- **Descrição**: MongoDB é um banco de dados NoSQL orientado a documentos que utiliza JSON para armazenar dados.
- **Características**:
  - **Open Source**: Disponível como software livre.
  - **Multiplataforma**: Funciona em diferentes sistemas operacionais.
  - **Escalável**: Suporta alta escalabilidade e desempenho.
  - **Orientado a Documentos**: Armazena dados em formato JSON e suporta documentos aninhados.
  - **Indexado**: Permite a busca eficiente através do conteúdo dos documentos.
  - **Sem Esquema Fixo**: Flexível quanto à estrutura dos dados.
  - **Sem Integridade Referencial**: Não mantém relacionamentos entre documentos como um banco de dados relacional.

## Referências
- [Guru99 - NoSQL Tutorial](https://www.guru99.com/nosql-tutorial.html)
- [Neo4j - Why NoSQL Databases?](https://neo4j.com/blog/why-nosql-databases/)
- [MongoDB - Aplicações .NET](http://netcoders.com.br/mongodb-aplicacoes-dotnet/)

# Arquitetura Banco de Dados NoSQL

## 1. Arquitetura MongoDB

### Sharding e Replica Set

A arquitetura do MongoDB utiliza dois conceitos importantes para garantir escalabilidade e alta disponibilidade: **Sharding** e **Replica Set**.

#### Sharding
- **Sharding** é a técnica de **escalabilidade horizontal** que divide grandes conjuntos de dados em **shards**, que são distribuídos entre diferentes servidores.
- Cada **shard** é um banco de dados independente, mas coletivamente, os shards formam um único banco de dados lógico. Um banco pode conter uma mistura de **coleções fragmentadas** e **não fragmentadas**.
- As coleções fragmentadas são distribuídas entre os shards, enquanto as não fragmentadas permanecem em um **shard primário**.

Referência: [Sharding MongoDB](https://www.mongodb.com/docs/v2.6/core/sharding-introduction/)

#### Replica Set
- Um **Replica Set** é um grupo de instâncias MongoDB que mantém o mesmo conjunto de dados, proporcionando **alta disponibilidade**.
- O **nó primário** é responsável por todas as operações de escrita e mantém um log de operações (oplog). Os **nós secundários** replicam essas operações de forma assíncrona.
- Em caso de falha do primário, um secundário pode se eleger como o novo nó primário, garantindo a continuidade da operação.

Referência: [Replica Set MongoDB](https://www.mongodb.com/docs/manual/replication/)

## 2. Teorema CAP

De acordo com o **Teorema CAP**, um sistema distribuído pode garantir somente **dois** dos três aspectos simultaneamente:
- **Consistência**
- **Disponibilidade**
- **Tolerância à Partição**

Em um banco de dados distribuído, você deve escolher entre consistência ou disponibilidade, pois a **tolerância à partição** é inevitável. A decisão depende dos requisitos do sistema.

Referência: [CAP Theorem](https://www.yugabyte.com/blog/tag/cap-theorem/)

## 3. Consistência Eventual

O conceito de **Consistência Eventual** surge do Teorema CAP, onde o sistema prioriza a **disponibilidade** e o **armazenamento rápido** de dados. A consistência entre os nós é garantida após um período de tempo, resultando em um estado temporário de inconsistência. Esse modelo é amplamente utilizado por sistemas como **MongoDB**, **Cassandra**, e **RavenDB**.

Referência: [Consistência Eventual](https://www.nexsoftsys.com/articles/CAP-theorem-database-dbms.html)

## 4. Escalabilidade Horizontal

Com o aumento de volume de dados, surge a necessidade de melhorar o desempenho através da **escalabilidade**. Existem duas formas de escalar:
- **Escalabilidade Vertical**: adicionar mais recursos (CPU, memória) em um único servidor.
- **Escalabilidade Horizontal**: adicionar mais servidores (nós) para distribuir a carga de trabalho, como ocorre com o **Sharding** no MongoDB.

Referência: [Escalabilidade](https://blog.router-switch.com/2021/03/what-is-the-difference-between-scale-up-and-scale-out/)

