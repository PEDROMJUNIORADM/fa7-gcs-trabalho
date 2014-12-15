Aluguel de livros
=================
Plano de Gerenciamento de Configuração
======================================
Versão &lt;1.0&gt;
------------------

Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|_&lt;12/12/2014&gt;_|_&lt;1.0&gt;_|_&lt;Versão inicial&gt;_|_&lt;Victor&gt;_|



1. Introdução
==============

Este Plano de Gerenciamento de Configuração estabelece e mantem a integridade dos artefatos gerados no projeto. Neste documento estão as atividades referentes ao gerenciamento de controle de configurações e mudanças que ocorrerão durante o desenvolvimento e manutenção do sistema, mantem a integridade dos artefados gerados e permite o acompanhamento através de históricos de evolução dos artefatos.
Rastreia as modificações nos itens de configuração ao longo do tempo, para auxiliar no controle das mudanças e na reproducibilidade do sistema.

1.1 Finalidade
---------------
A finalidade deste documento é organizar a evolução e mudanças deste projeto para manter o planejamento dos artefatos gerados, baseados nos padrões de nomenclatura, versionamento, oragnização do projeto (diretórios) e  responsabilidades (papéis de cada integrante).
Este documento deve ser acessível a todos os envolvidos do desenvolvimento deste sistema.

1.2 Escopo
----------
Este documento descreve toda a infra-estrutura utilizada durante o desenvolvimento do projeto, afetando diretamente no desenvolvimento, pois deverá seguir os padrões e a organização de trabalho estabelecidas neste plano.
 

1.3 Definições, Acrônimos e Abreviações
---------------------------------------
|Termo     |Significado                                   |
|----------|----------------------------------------------|
| Baseline | Um marco de uma versão, consolidada e estável, servindo de base para trabalhos futuros. |

1.4 Referências
---------------
_[Esta subseção apresenta uma lista completa de todos os documentos mencionados no Plano de Gerenciamento de Configuração. Identifique os documentos por título, número de relatório (se aplicável), data e organização responsável pela publicação. Especifique as fontes a partir das quais as referências podem ser obtidas. Essas informações podem ser fornecidas por um anexo ou outro documento.]_

1.5 Visão Geral
---------------
###### Organização do documento:
 
|Sessão     |Descrição                                   |
|-----------|--------------------------------------------|
| 2.1       | Descrição de quem será o responsável pela execução das diversas atividades de Gerenciamento de Configuração (CM) descritas no Processo de CM |
| 2.2       | Descrição do ambiente de computação e as ferramentas de software a serem utilizadas para desempenhar as funções de CM em todo o ciclo de vida do projeto ou produto e as ferramentas e procedimentos necessários para o ciclo de vida do produto. |
| 3.1.1     | Descrição do padrão de nomeação dos artefatos |
| 3.1.2     | Relação detalhada dos artefatos do sistema |
| 3.1.3     | Descrição das baselines do projeto |
| 3.1.4     | Descrição da organização de diretórios e itens que devem ser armazenados |
| 3.2.1     | Descrição do processo que define a alteração de mudança |
| 3.2.2     | Definição dos participantes do CCB e descrição dos procedimentos que lidam com as solicitações e aprovações de mudanças |
| 4         | Descrição dos padrões e procedimentos que devem ser seguidos no projeto |
| 4.1.1     | Descrição do padrão para nomeação de branchs |
| 4.1.2     | Descrição do padrão para nomeação de commits |
| 4.1.3     | Descrição do padrão para nomeação de tags    |
| 5         | Descrião dos recursos (ferramentas de software) e do treinamento |
| 6         | Descrição do que será auditado e como serão reportados os problemas encontrados, assim como as suas soluções |



2. Gerenciamento de Configuração de Software
============================================

2.1 Organização, Responsabilidades e Interfaces
------------------------------------------------
_[Descreva quem será o responsável pela execução das diversas atividades de Gerenciamento de Configuração (CM) descritas no Processo de CM.]_

2.2 Ferramentas, Ambiente e Infra-estrutura
-------------------------------------------
_[Descreva o ambiente de computação e as ferramentas de software a serem utilizadas para desempenhar as funções de CM em todo o ciclo de vida do projeto ou produto._
_Descreva as ferramentas e os procedimentos necessários utilizados para o controle de versão dos itens de configuração gerados no ciclo de vida do projeto ou produto._
_As questões envolvidas na configuração do ambiente de CM incluem:_
* _tamanho previsto dos dados do produto_
* _distribuição da equipe do produto_
* _localização física dos servidores e clientes]_
 


3. O Programa de Gerenciamento de Configuração
==============================================

3.1 Identificação da Configuração
---------------------------------
### 3.1.1 Métodos de Identificação
----------------------------------
_[Descreva como os artefatos do projeto ou produto devem ser nomeados, marcados e numerados. O esquema de identificação deve abranger o hardware, o software do sistema, os produtos de terceiros (COTS) e todos os artefatos de desenvolvimento de aplicativos listados na estrutura de diretórios do produto; por exemplo, planos, modelos, componentes, software de teste, resultados e dados, executáveis e assim por diante.]_

### 3.1.2 Itens de Configuração
_[Relacionar os artefatos ou grupos de artefatos, separando por tipo, modulo ou subsistema, responsável ou momento em que deverão ser incluídos em baselines._
* _“Inclusão em Baseline” em branco significa que o grupo de artefatos não participará de baseline. Pode ser expresso como uma data ou identificador de uma baseline, fase ou ponto de controle_
* _“Responsável”: indicar nominalmente, sempre que possível]_

| Item (ou Tipo de Item)                 | Responsável na equipe	     | Inclusão em Baseline |
|----------------------------------------|-----------------------------|----------------------|
|_&lt;grupo de itens de configuração&gt;_|_&lt;nome do responsável&gt;_|_&lt;momento a partir do qual o conjunto de artefatos será incluído em baseline&gt;_|


### 3.1.3 Baselines do Projeto

_[As baselines funcionam como um padrão oficial no qual os trabalhos subseqüentes são baseados. Somente mudanças autorizadas podem ser efetuadas nas baselines._
_Descreva em que pontos do ciclo de vida do projeto ou produto as baselines devem ser estabelecidas. As baselines mais comuns devem ser definidas ao final de cada uma das fases de Iniciação, Elaboração, Construção e Transição. Elas também podem ser geradas no final de iterações ocorridas dentro das várias fases ou com freqüência ainda maior._
_Descreva quem autoriza uma baseline e o que ela contém.]_

### 3.1.4 Estrutura do Repositório de Versões
_[Descreva a organização de diretórios do seu repositório e que itens/arquivos devem ser armazenados em cada diretório.]_

3.2 Controle de Configuração e Mudança
--------------------------------------

### 3.2.1 Processamento e Aprovação de Solicitações de Mudança
_[Descreva o processo pelo qual os problemas e as mudanças são submetidos, revisados e dispostos. Inclua como funciona a transição de estados de uma solicitação de mudança]_

### 3.2.2 Comitê de Controle de Mudança (CCB)
_[Descreva a participação e os procedimentos para processar solicitações e aprovações de mudança a serem seguidos pelo CCB. Informe quem são os membros do CCB e suas responsabilidades.]_



4. Padrões e Procedimentos
==========================
_[Descreva os padrões e procedimentos que devem ser seguidos no projeto. Crie subseções se achar necessário, para organizá-los melhor.]_



5. Treinamento e Recursos
=========================
_[Descreva as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas.]_



6. Auditorias de Configuração
=============================
_[Descreva o cronograma das auditorias de configuração e o que será verificado. Informe também como serão reportados os problemas encontrados e onde sera feito o acompanhamento dos itens corretivos.]_
