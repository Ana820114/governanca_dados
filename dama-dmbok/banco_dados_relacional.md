# Modelos de Dados

## Banco de Dados Relacional

Os Bancos de Dados Relacionais (RDBMS) são projetados para armazenar dados de forma estruturada em tabelas, seguindo o modelo relacional. Esses bancos de dados utilizam a linguagem SQL (Structured Query Language) para manipulação e consulta dos dados.

### Elementos Básicos
- **Relações (Tabelas):** Estruturas que armazenam dados em formato de linhas e colunas.
- **Registros (Tuplas):** Cada linha de uma tabela que representa uma instância de dados.

### Características Fundamentais
- **Restrições de Integridade:** Regras que garantem a precisão e consistência dos dados. Exemplos incluem:
  - **PK (Primary Key):** Identificador único para cada registro na tabela.
  - **FK (Foreign Key):** Chave que estabelece uma relação entre tabelas.
  - **UK (Unique Key):** Garante que todos os valores em uma coluna sejam únicos.
  - **CK (Check Key):** Restrições que validam dados inseridos.
  - **NN (Not Null):** Garante que uma coluna não possa ter valores nulos.

### Exemplos

![Exemplo de Banco de Dados Relacional](https://github.com/user-attachments/assets/d0f7f36e-dc7d-4cc2-809d-3bbad6aafa69)

## Modelo Dimensional

O Modelo Dimensional é uma abordagem utilizada para projetar bancos de dados que suportam sistemas de Business Intelligence (BI) e Data Warehousing. Ele é projetado para otimizar a consulta e a análise de grandes volumes de dados, proporcionando uma estrutura que facilita a compreensão e o uso dos dados para análises e relatórios.

### Descrição

O Modelo Dimensional organiza dados em uma estrutura que facilita a análise rápida e eficiente. Ele é baseado em duas principais entidades:

- **Fatos**: Tabelas que armazenam dados quantitativos e métricas sobre eventos ou transações. Estas tabelas contêm medidas que são analisadas, como vendas, lucros ou quantidade de produtos vendidos.
- **Dimensões**: Tabelas que contêm atributos descritivos relacionados às tabelas de fatos. As dimensões ajudam a categorizar e a fornecer contexto para as medidas. Exemplos incluem tempo, local, produto e cliente.

### Componentes Principais

#### Tabelas de Fato

- **Definição**: Contêm as métricas e medidas numéricas associadas a eventos ou transações. Exemplos incluem tabelas de vendas, transações financeiras ou desempenho de marketing.
- **Características**: Normalmente têm muitas linhas e são agregadas para fornecer resumo e análise.

#### Tabelas de Dimensão

- **Definição**: Contêm atributos descritivos sobre as dimensões de negócios. Exemplos incluem tabelas de clientes, produtos ou datas.
- **Características**: Normalmente têm menos linhas em comparação com as tabelas de fatos e são usadas para descrever e categorizar os dados.

### Esquemas de Modelagem

- **Esquema em Estrela**: Consiste em uma tabela de fatos central conectada a várias tabelas de dimensões. O modelo é simples e fácil de entender, ideal para consultas rápidas e eficientes.
  
  ![Esquema em Estrela](https://example.com/estrela.png)  <!-- Substitua o link da imagem por um válido ou remova esta linha -->

- **Esquema em Floco de Neve**: Uma variação do esquema em estrela onde as tabelas de dimensões são normalizadas. Isso pode reduzir redundâncias e melhorar a integridade dos dados, mas pode tornar as consultas mais complexas.

  ![Esquema em Floco de Neve](https://example.com/floco.png)  <!-- Substitua o link da imagem por um válido ou remova esta linha -->

### Benefícios

- **Facilidade de Uso**: Os modelos dimensionais são projetados para serem intuitivos, facilitando a criação de relatórios e análises complexas.
- **Desempenho de Consulta**: Otimiza o desempenho das consultas analíticas e relatórios devido à estrutura simplificada das tabelas de fatos e dimensões.
- **Escalabilidade**: Suporta grandes volumes de dados e permite a adição de novas dimensões e fatos conforme necessário.

### Referência

Para mais informações, consulte a [Documentação do Modelo Dimensional - Visual Paradigm](https://www.visual-paradigm.com/support/documents/vpuserguide/3563/3564/85378_conceptual,l.html).

![Imagem do Modelo Dimensional](https://github.com/user-attachments/assets/7df52494-f19c-43f0-a8a6-1d9755fbcf06)

## Modelo Conceitual

### Descrição

O Modelo Conceitual é uma representação de alto nível de um sistema de banco de dados, focado na estrutura das entidades e seus relacionamentos. É uma visão independente da tecnologia e do sistema de gerenciamento de banco de dados (DBMS) usado. O objetivo principal é definir os requisitos e o escopo do banco de dados.

### Componentes Principais

- **Entidades**: Representam objetos ou conceitos do mundo real que têm uma existência independente e são importantes para o sistema.
- **Relacionamentos**: Mostram como as entidades estão relacionadas entre si.
- **Atributos**: Características ou propriedades das entidades.

### Benefícios

- Facilita a comunicação entre analistas, designers e usuários finais.
- Ajuda a identificar os requisitos e definir o escopo do banco de dados.

### Referência

Para mais informações, consulte [Modelo Conceitual - Visual Paradigm](https://www.visual-paradigm.com/support/documents/vpuserguide/3563/3564/85378_conceptual,l.html).

## Modelo Lógico

### Descrição

O Modelo Lógico é uma representação detalhada das entidades e relacionamentos identificados no Modelo Conceitual. Ele traduz o modelo conceitual em uma estrutura mais específica, que é independente da tecnologia de banco de dados, mas inclui detalhes suficientes para a criação de um modelo físico.

### Componentes Principais

- **Entidades**: Definidas com mais detalhes, incluindo tipos de dados e restrições.
- **Relacionamentos**: Definidos com cardinalidade e outras propriedades.
- **Atributos**: Especificados com detalhes sobre tipos e formatos.

### Benefícios

- Oferece uma visão mais detalhada das estruturas de dados.
- Serve como um guia para o desenvolvimento do Modelo Físico.

### Referência

Para mais informações, consulte [Modelo Lógico - Visual Paradigm](https://www.visual-paradigm.com/support/documents/vpuserguide/3563/3564/85378_conceptual,l.html).

## Modelo Físico

### Descrição

O Modelo Físico é a implementação detalhada do Modelo Lógico em um sistema de gerenciamento de banco de dados específico. Ele descreve como os dados serão armazenados, acessados e gerenciados no banco de dados físico.

### Componentes Principais

- **Tabelas**: Representam as entidades do Modelo Lógico como tabelas em um banco de dados.
- **Colunas**: Definem os atributos das tabelas, incluindo tipos de dados e restrições.
- **Índices**: Usados para melhorar o desempenho das consultas.
- **Chaves**: Incluem chaves primárias e estrangeiras para garantir integridade referencial.

### Benefícios

- Fornece uma especificação clara e detalhada para a implementação no DBMS.
- Inclui otimizações para melhorar o desempenho e garantir a integridade dos dados.

### Referência

Para mais informações, consulte [Modelo Físico - Visual Paradigm](https://www.visual-paradigm.com/support/documents/vpuserguide/3563/3564/85378_conceptual,l.html).
