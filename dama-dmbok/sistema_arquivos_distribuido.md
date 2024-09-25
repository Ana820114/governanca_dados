# Sistema de Arquivos Distribuídos

## 1. Sistemas de Arquivos

- **Definição:** Desenvolvidos inicialmente como um recurso do sistema operacional, os sistemas de arquivos fornecem uma interface conveniente para armazenamento em disco.
- **Responsabilidades:** São responsáveis pela organização, armazenamento, recuperação, atribuição de nomes, compartilhamento e proteção de arquivos.
- **Recursos:**
  - Armazenamento e gerenciamento de grandes quantidades de arquivos.
  - Funções de criação, atribuição de nomes e exclusão de arquivos.
- **Diretório:** Um diretório é um arquivo especial que mapeia nomes textuais para identificadores internos e pode incluir outros diretórios.

Referência: [Sistemas de Arquivos](https://homepages.dcc.ufmg.br/~fsantos/ECO036/seminarios/sistemas_arquivos_distribuidos.pdf)

## 2. Sistemas de Arquivos Distribuídos (DFS ou SAD)

- **Definição:** Um sistema de arquivos distribuídos permite que programas armazenem e acessem arquivos remotos como se fossem locais, permitindo que usuários acessem arquivos a partir de qualquer computador na rede.
- **Objetivo:** Proporcionar o armazenamento e acesso de arquivos de forma segura e confiável em redes distribuídas.
- **Vantagens:** 
  - Compartilhamento de dados entre processos por longos períodos.
  - Desempenho e segurança comparáveis aos arquivos armazenados em discos locais.

### Requisitos de um Sistema de Arquivos Distribuídos
- **Transparência:** Acessos remotos devem parecer locais.
- **Concorrência:** Múltiplos usuários podem atualizar arquivos simultaneamente.
- **Replicação de Arquivos:** Garantir disponibilidade.
- **Heterogeneidade:** Suporte a diferentes sistemas.
- **Tolerância a Falhas:** Recuperação em caso de falhas.
- **Consistência e Segurança:** Manter a integridade e proteção dos dados.
- **Eficiência:** Otimização de desempenho.

Referência: [Sistemas de Arquivos Distribuídos](https://homepages.dcc.ufmg.br/~fsantos/ECO036/seminarios/sistemas_arquivos_distribuidos.pdf)

## 3. Arquitetura do SAD

- **Modelo Abstrato:** Usado para sistemas como Network File System (NFS) e Andrew File System (AFS).
- **Divisão em Módulos:**
  - **Cliente:** Interface com o usuário.
  - **Serviço de Arquivos Planos:** Gerencia os arquivos reais.
  - **Serviço de Diretórios:** Gerencia a estrutura hierárquica de diretórios.
- **Design Aberto:** Diferentes módulos podem implementar interfaces distintas, otimizando performance para diferentes configurações de hardware de clientes e servidores.

Referência: [Network File System](https://pt.wikipedia.org/wiki/Network_File_System)

## 4. Apache Hadoop

- **Hadoop:** Plataforma de código aberto para armazenamento e processamento distribuído de grandes volumes de dados utilizando clusters de computadores de hardware comum.
- **Serviços:** Fornece armazenamento, processamento, acesso, governança, segurança e operações de dados.

Referência: [Apache Hadoop](https://hadoop.apache.org/)

### HDFS (Hadoop Distributed File System)

- **Definição:** O HDFS é um sistema de arquivos distribuído projetado para armazenar grandes volumes de dados e suportar o acesso em modo streaming.
- **Características:**
  - Utilizado em clusters de servidores de baixo custo.
  - Não recomendado para aplicações que necessitem de acesso rápido a registros específicos ou para leitura de muitos arquivos pequenos.
- **Recursos:**
  - Dois tipos de nós: **Master (Namenode)** e **Worker (Datanode)**.
  - O Master armazena metadados e a distribuição dos arquivos, enquanto os Workers armazenam os dados propriamente ditos.
  - O Master pode ter backup ou um Master secundário para garantir alta disponibilidade.

Referência: [HDFS Design](https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html)
