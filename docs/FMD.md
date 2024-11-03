# Framework de Mineração de Dados


Baseado no trabalho de ALVES, Gabriel Mac’Hamilton Renaux (2024), o FMD vem com uma nova arquitetura e tem como proposta o d esenvolvimento de um Mecanismo de Ingestão de Dados Independente de Contextos para AutoML.

## Arquitetura

Foi desenvolvida para complementar a solução de AutoML existente da Universidade de Pernambuco, anteriormente conhecida como FMDEV. Uma nova camada de ingestão e processamento de dados foi adicionada à arquitetura original proposta por Silva (2020), usando Javascript para o frontend e Python para o backend, além da plataforma Pentaho Data Integration Community Edition (PDI-CE) para gerenciar a ingestão de dados.

A camada de frontend, construída com HTML, CSS e Javascript (React.js), permite a interação com o usuário e se comunica com o backend através de um servidor Nginx, que serve também como proxy reverso e para encaminhar requisições HTTP via REST. O backend, implementado em Python com Flask, processa as requisições HTTP enviadas pelo Gunicorn, um servidor WSGI que se comunica com o Nginx.

O sistema de armazenamento inclui um Data Lake com duas zonas: uma com PostgreSQL para dados relacionais e outra com sistema de arquivos para dados ingeridos e processados pelo PDI-CE, armazenados em formato CSV. O PDI-CE, através de seu servidor Carte, executa processos de ETL acionados pelo Flask, manipulando dados de diferentes fontes (bancos de dados ou arquivos CSV) e realizando transformações como seleção de colunas e carregamento no Data Lake.

A figura 1 mostra a arquitetura do FMD.

![Figura 1 - Arquitetura do FMD](https://raw.githubusercontent.com/GPCDA/fmd-docs/fb0dce0c16d1f9b21e1cd5104812507c2a54ea74/docs/img/fmd_arch.png)

## Referências

- ALVES, Gabriel Mac’Hamilton Renaux. *Desenvolvimento de um Mecanismo de Ingestão de Dados Independente de Contextos para AutoML.* Orientador: Prof. Dr. Alexandre Magno Andrade Maciel. 2024. Dissertação (Mestrado em Engenharia da Computação) - Escola Politécnica de Pernambuco, Universidade de Pernambuco, Recife, 2024.

- SILVA, R. G. da. Desenvolvimento de uma Solução de Aprendizado de Máquina
Automatizado Integrável a Múltiplos Ambientes Virtuais de Aprendizagem. Dissertação
(Dissertação de Mestrado) — Universidade de Pernambuco, 2020.