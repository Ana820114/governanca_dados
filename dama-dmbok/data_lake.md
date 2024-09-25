# Data Lake

## Características de um Data Lake
- Centraliza os dados da organização em um único local.
- Persiste dados estruturados, semi-estruturados e não-estruturados.
- Alta performance em escrita (ingestão) e em acesso (consumo).
- Baixo custo de armazenamento em comparação a um Data Warehouse.
- Suporta regras de segurança e proteção de dados.
- Desacopla o armazenamento do processamento (ELT - Extract, Load, Transform).

## Recursos de um Data Lake
- Coleta e armazenamento de qualquer tipo de dado a baixo custo.
- Proteção de todos os dados armazenados no repositório central.
- Pesquisa e localização de dados relevantes no repositório.
- Consulta aos dados, com definição da estrutura no momento do uso (esquema na leitura).

## Armazenamento em um Data Lake
- **Dados estruturados:** Banco de dados relacionais, Excel.
- **Dados semiestruturados:** Arquivos HTML, XML.
- **Dados não-estruturados:** Arquivos de texto, imagens, vídeos, dados de redes sociais.

## Estágios para Armazenamento em um Data Lake
O Data Lake é geralmente dividido em quatro zonas, que refletem os diferentes estágios do armazenamento e processamento dos dados:

1. **Transient Zone:** 
   - Zona transitória onde os dados são inicialmente ingeridos.
   - Início do processo de governança, catalogação das origens e tipos de dados.
   - Após a alocação dos dados na Raw Data Zone, os arquivos nesta zona são excluídos, sendo temporários.

2. **Raw Data Zone:** 
   - Zona de armazenamento bruto, onde os dados são mantidos sem tratamento imediato.
   - Oferece flexibilidade para armazenar todos os dados, independentemente de quando serão consumidos.
   - Usada por cientistas de dados para modelagens de machine learning e AI.

3. **Trusted Zone:** 
   - Zona de dados tratados e transformados, prontos para consumo.
   - Garantias de Data Quality, tornando os dados exatos e confiáveis.

4. **Refined Zone:** 
   - Dados totalmente processados e enriquecidos, prontos para consumo por aplicações externas.
   - Frequentemente implementada com infraestrutura de bancos de dados relacionais.

Referência: [Data Lake Governance Best Practices](https://dzone.com/articles/data-lake-governance-best-practices)

## Zonas do Data Lake

### Transient Zone
- Primeira zona de ingestão de dados no Data Lake.
- Governança dos dados inicia-se aqui, com catalogação e identificação de linhagens.
- Arquivos temporários, excluídos após a transferência para a **Raw Data Zone**.

### Raw Data Zone
- Armazena rapidamente todos os dados das fontes, sem tratamento imediato.
- Fornece dados brutos que podem ser usados por cientistas de dados para modelagem e análises avançadas.

### Trusted Zone
- Zona de dados tratados e transformados, com garantias de qualidade e precisão, prontos para consumo.

### Refined Zone
- Dados tratados e enriquecidos, prontos para consumo por aplicativos externos, frequentemente armazenados em bancos de dados relacionais.
