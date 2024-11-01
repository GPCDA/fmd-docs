# Framework de Mineração de Dados Educacionais Visuais - FMDEV

O Framework de Mineração de Dados Educacionais Visual - FMDEV é um sistema de
AutoML desenvolvido originalmente em 2017 na Universidade de Pernambuco ao longo de
diversos trabalhos acadêmicos.

O projeto foi concebido inicialmente com o objetivo de permitir a mineração de dados
em ambientes virtuais de aprendizado (AVA), e com o foco de *democratizar* atividades de mineração de dados para usuários com pouco conhecimento técnico nesta área, sendo denominado
*Framework de Mineração de Dados Educacionais Visual*. 

O framework permitiria com poucos
cliques a mineração dos dados do AVA Moodle11, disponibilizando análises e gráficos de forma
visual para o usuário. O projeto foi desenvolvido com as tecnologias Hypertext Markup Language
(HTML), Cascading Style Sheets (CSS), e JavaScript, sendo integrado ao Moodle como um
bloco HTML. A arquitetura incial do FMDEV está representada na Figura 1.

![Figura 1 - Arquitetura do FMDEV](https://raw.githubusercontent.com/GPCDA/fmd-docs/5ab9666d9efbb5be727f3d3c4fa8f712026477ed/docs/img/fmdev_arch_1.png)	

Os autores Fujisawa e Maciel (2018) trouxeram melhorias para o projeto com o
objetivo de modernizar as tecnologias utilizadas e trazer mais funcionalidades de mineração
de dados, voltadas para o contexto educacional. Para atingir os objetivos do projeto foram
desenvolvidos um WebService na linguagem de programação Python para realização de atividades
de mineração de dados, e uma aplicação web desenvolvida utilizando a tecnologia React.js para
que o usuário pudesse interagir com a plataforma. 

Para os testes, o FMDEV foi conectado
diretamente com a base de dados do AVA Moodle. A arquitetura do projeto em 2018 pode ser
visualizada na Figura 2.

![Figura 2 - Arquitetura do FMDEV evoluída](https://raw.githubusercontent.com/GPCDA/fmd-docs/5ab9666d9efbb5be727f3d3c4fa8f712026477ed/docs/img/fmdev_arch_2.png)

O trabalho de Silva (2020) aprimorou o projeto levando ao estado atual, com uma
arquitetura mais robusta, tecnologias atualizadas, novas fucnionalidades e uma interface de
usuário de simples utilização. O projeto passou por uma refatoração utilizando técnicas do Lean
Inception e engenharia de requisitos, e um levantamento de tecnologias através de uma RSL,
permitindo a elaboração de uma arquitetura mais aperfeiçoada, com base no projeto original,
conforme a Figura 3. 

Neste momento o projeto deixou de ser um framework para mineração de
dados, e tornou-se um framework de AutoML, sendo capaz de realizar atividades de aprendizado
de máquina supervisionado de maneira automatizada e apresentar os resultados de forma visual
com dados relativos ao contexto de educação.

![Figura 3 - Arquitetura do FMDEV final](https://raw.githubusercontent.com/GPCDA/fmd-docs/5ab9666d9efbb5be727f3d3c4fa8f712026477ed/docs/img/fmdev_arch_3.png)	


## Referências

- ALVES, Gabriel Mac’Hamilton Renaux. *Desenvolvimento de um Mecanismo de Ingestão de Dados Independente de Contextos para AutoML.* Orientador: Prof. Dr. Alexandre Magno Andrade Maciel. 2024. Dissertação (Mestrado em Engenharia da Computação) - Escola Politécnica de Pernambuco, Universidade de Pernambuco, Recife, 2024.

- GONçALVES, A. F.; MACIEL, A. M.; RODRIGUES, R. L. Development of a data
mining education framework for visualization of data in distance learning environments.
International Conferences on Software Engineering and Knowledge Engineering, 2017.

- FUJISAWA, I. Y.; MACIEL, A. M. Desenvolvimento de um framework integrador de
mineração de dados educacionais. Revista de Engenharia e Pesquisa Aplicada, v. 3, n. 3, 2018.

- SILVA, R. G. da. Desenvolvimento de uma Solução de Aprendizado de Máquina
Automatizado Integrável a Múltiplos Ambientes Virtuais de Aprendizagem. Dissertação
(Dissertação de Mestrado) — Universidade de Pernambuco, 2020.