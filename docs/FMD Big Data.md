# Framework de Mineração de Dados


Baseado no trabalho de CUNHA, Roberto Sá Barreto Paiva (2024), o FMD vem com o incremento do desenvolvimento de uma integração entre um framework de AutoML e ferramentas para processamento distribuído.

## Arquitetura

Como o FMDEV já é um projeto existente e desenvolvido pela Universidade de Pernambuco, a nova arquitetura complementa a já utilizada anteriormente. A integração com ferramentas de Big Data não altera o fluxo do backend original do framework desenvolvido por Silva (2020) ou a camada de ingestão de dados do trabalho de Alves (2024). A Figura 1 exemplifica como ficou a arquitetura juntamente com as tecnologias utilizadas durante o desenvolvimento e testes.

A camada de frontend apresenta a interface de usuário desenvolvida em React, uma
biblioteca da linguagem Javascript utilizada em aplicações WEB. O React no contexto do FMDEV é utilizado para manipulações da página alterando seu HTML e CSS de forma dinâmica sem necessidade de recarregamento. Os componentes gráficos foram desenvolvidos com base nessa biblioteca. O frontend faz chamadas HTTP utilizando o Nginx40, servidor HTTP de proxy
reverso, para realizar a comunicação entre o frontend e backend por meio de chamadas REST.

O backend original foi feito em Flask utilizando Gunicorn como servidor WSGI (Sigla do Inglês: Web Server Gateway Interface), sendo este responsável por receber as requisições do Nginx e enviar ao Flask. De acordo com Alves (2024), a camada do ingestor de dados é utilziado o PDI-CE com base em seu servidor HTTP chamado Carte.

Na camada do Cluster foi desenvolvido um servidor Django Rest que é responsável por receber as requisições realizadas por meio do frontend do FMDEV e processá-las. O serviço do Django Rest é responsável pela leitura dos dados no HDFS e pela execução do treinamento de AutoML que utiliza a biblioteca H2O devido a variedade algoritmos.

A figura 1 mostra a arquitetura do FMD.
![Figura 1 - Arquitetura do FMD](https://raw.githubusercontent.com/GPCDA/fmd-docs/7225290aec040aa7b0e47edae8a2acd8a559904f/docs/img/fmd_arch_bigdata.png)	

## Referências

- CUNHA, Roberto Sá Barreto Paiva. *Desenvolvimento de uma integração entre um framework de AutoML e ferramentas para processamento distribuído* Orientador: Prof. Dr. Alexandre Magno Andrade Maciel. 2024. Coorientador: Dr. Jairson Barbosa Rodrigues. Dissertação (Mestrado em Engenharia da Computação) - Escola Politécnica de Pernambuco, Universidade de Pernambuco, Recife, 2024.

- SILVA, R. G. da. Desenvolvimento de uma Solução de Aprendizado de Máquina
Automatizado Integrável a Múltiplos Ambientes Virtuais de Aprendizagem. Dissertação
(Dissertação de Mestrado) — Universidade de Pernambuco, 2020.

- SILVA, R. G. da. Desenvolvimento de uma Solução de Aprendizado de Máquina
Automatizado Integrável a Múltiplos Ambientes Virtuais de Aprendizagem. Dissertação
(Dissertação de Mestrado) — Universidade de Pernambuco, 2020.