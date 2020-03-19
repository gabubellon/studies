# TREINAMENTO DE BIG DATA AWS 
> in loco Conta Azul
>
> 05-06-07/08/2019

## Ambiente de Estudo e Treinamento

* Treinamento: <https://www.aws.training>
* Bookshaft: <http://online.vitalsource.com/>
* Quicklabs: <https://aws.qwiklabs.com/>

## Pre Rec

* Big Data Technology Fundamentals : <https://aws.amazon.com/pt/training/course-descriptions/bigdata-fundamentals/>

* AWS Technical Essentials: <https://aws.amazon.com/training/course-descriptions/essentials/>

## AWS Tools

### Kinesis Data Firehose

* Sem administração;
* Near real-time (tenho que deixar 60s represados);
* Elástico (custo $$);
* Tempo de represamento precisa estar alinhado com necessidade;
* Quando dado for entregue (fanout) ele "some"

### Kinesis Data Streams

* Sem administração;
* Near real-time performático;
* Elástico (custo $$) mas com gerênciamento humano;
* Custo x Capacidade
* Trabalha com **Shards**
  * Taxas de leituras e escritas;
  * Particionamento por *chave* e nos *shards*;
  * Necessário controlar os *shards*
* KCL: lib para controlar consumers e shards
  * Definição de partition Keys;
  * Gerenciamento dos consumers para ocorrência de splits de shards

> * Firehose mais simplista, latência;
>
> * Data Streams flexível, complicado

### Streaming Analytics & Kinesis Data Analytics

* Analises de dados *durante* processamento de stream;
* Querys de consultas (on time ou recursivo);
* Consultas por janelas de dados;

### Apache Spark Stream & Kafka

* Consumo de toda AWS;
* EMR

## Data Lake

## EMR

* HDFS;
* EMRFS - camada de acesso dos dados para EMR:
  * Grava os metadados em DynamoDB;
  * Leitura dos indices do DynanamoDB e depois busca no S3;
  * Garante consistência de leitura
* Volumes EBS duram em tempo de estância;

## Data Analysis

* Athena
  * Cluster de Hadoop Serveless;
  * Inferência de schema para S3;
  * Presto - SQL;
  * Hive - DDL;
  * Integração com QuickSight;
  * Particionamento por bucket para permitir performance;

## AWS EMR

* Apache Hadoop & Map e Reduce
  * Processamento batch paralelo;
  * Map - Reduce e Yarn;

* EMR
  * Automatização;
  * Auto gerenciável;
