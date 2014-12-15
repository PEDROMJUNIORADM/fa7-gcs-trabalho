Aluguel de livros
=================
Plano de Gerenciamento de Configuração
======================================
Versão &lt;1.5&gt;
------------------

Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|_&lt;08/12/2014&gt;_|_&lt;1.0&gt;_|_&lt;Versão inicial&gt;_|_&lt;Victor&gt;_|
|_&lt;14/12/2014&gt;_|_&lt;1.1&gt;_|_&lt;Sessão 6 e 4&gt;_|_&lt;Yanko&gt;_|
|_&lt;14/12/2014&gt;_|_&lt;1.2&gt;_|_&lt;Sessão 3&gt;_|_&lt;Diego&gt;_|
|_&lt;12/12/2014&gt;_|_&lt;1.3&gt;_|_&lt;Sessão 2 e 5&gt;_|_&lt;Luiz&gt;_|
|_&lt;12/12/2014&gt;_|_&lt;1.4&gt;_|_&lt;Descrição do documento&gt;_|_&lt;Victor&gt;_|
|_&lt;15/12/2014&gt;_|_&lt;1.5&gt;_|_&lt;Correções e integração&gt;_|_&lt;Victor e Luiz&gt;_|


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
|Termo     |Significado |
|----------|----------------------------------------------|
| Baseline | Um marco de uma versão, consolidada e estável, servindo de base para trabalhos futuros. |
| CCB      | Comitê de controle de mudanças. |

1.4 Referências
---------------

Branching model: http://nvie.com/posts/a-successful-git-branching-model/

1.5 Visão Geral
---------------
###### Organização do documento:
 
|Sessão     |Descrição |
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

Gestor do Projeto: Victor  
Gestor de Ferramentas de Gerência de Configuração: Yanko  
Gestor de Configuração de Software: Victor, Yanko, Diego  
Auditor de Configuração de Software: Luiz  
Desenvolvedor: Diego, Luiz, Yanko  

2.2 Ferramentas, Ambiente e Infra-estrutura
-------------------------------------------

Será usado como ferramenta de versionamento o GIT, uma ferramenta distribuida, então cada participante do projeto terá em sua estação de trabalho um repositório. Para facilitar a gerencia será desiginada uma máquina onde terá a última versão estável.
Para o 'pull' dessa máquina de controle (máquina da última versão estável) deve ser feito só após passar pela ferramenta de integração continua (CruiseControl).  
Cada máquina dos desenvolvedores deve ter instalado a mesma versão do Eclipse (Luna SR1) e a mesma versão do plugin EGit (3.4.1).
O projeto deve está configurado para uso da ferramenta de inspeção continua SONAR.
A ferramenta utilizada para auxiliar as mudanças será Bugzilla. 


3. O Programa de Gerenciamento de Configuração
==============================================

3.1 Identificação da Configuração
---------------------------------
### 3.1.1 Métodos de Identificação
----------------------------------
Todos os documentos disponibilizados no repositório devem ser identificados baseados na seguinte nomenclatura:               
ID ARTEFATO-NOME ARTEFATO  
Onde:             
•	ID ARTEFATO é a sigla de identificação do artefato conforme lista abaixo
•	NOME ARTEFATO é nome de identificação do artefato conforme lista abaixo.

ID ARTEFATO    	|  NOME ARTEFATO          
BC                 bibliotecas de componentes      
MU                 manuais do usuário     
CF                 código fonte           
PE                 programas executáveis  
DR                 documento de requisitos
MAP                modelo de análise e projeto     

### 3.1.2 Itens de Configuração

| Item de Configuração | Responsável | Inclusão em Baseline |
|----------------------|-------------|----------------------|
| Documento de Requisitos | Luiz, Yanko | Quando os requisitos forem definidos pelo cliente |
| Documento de arquitetura do software | Diego, Victor | Quando for validado pelo gerente de projetos |
| Cronograma | Victor | Quando for acordado o prazo juntamente com o cliente |
| Código fonte | Diego, Luiz, Yanko | Quando os testes forem escritos e aprovados |
| Documento de casos de testes | Diego, Luiz, Yanko | Quando os testes forem validados pelo cliente |
| Manuais | Luiz, Yanko | Quando o manual for aprovado pelo cliente |

### 3.1.3 Baselines do Projeto

A criação de baselines pode ser realizada de acordo com os marcos do projeto ou de alguma outra forma definida pela gerência. A baseline é armazenada em um repositório de itens de configuração. E, a partir desse momento, só pode ser alterado por meio de uma solicitação de alteração formal para controle de mudança.
Para cada uma das fases do modelo sugere-se a criação de baselines nos seguintes marcos:

- Fase Prospecção: Solicitação de uma proposta pelo cliente
- Fase Concepção: Conduzir revisão do Estudo de Viabilidade do Projeto
-	Fase Negociação: Conduzir revisão do Contrato
-	Fase Elaboração: Conduzir revisão do Arquitetura do Software
- Fase Construção: Conduzir revisão da Capacidade Operacional
-	Fase Transição: Conduzir revisão do Entrega do Produto


| Responsável | Baseline                       | Conteúdo                     |
|-------------|--------------------------------|------------------------------|
| Victor      | Baseline da fase de Prospecção | Termo de abertura do projeto            |
| Victor      | Baseline da fase de Consepção  | Cronogramas, Doc. Requisitos, Orçamento |
| Victor      | Baseline da fase de Negociação | Contratos |
| Victor      | Baseline da fase de Elaboração | Diagramas da UML. |
| Victor      | Baseline da fase de Contrução  | Código fonte, Suites de testes, relatórios de atividades  |
| Victor      | Baseline da fase de Transição  | Manuais, Doc. de Aceite |


A identificação da baseline pode ser constituída por:
“Baseline” + “_” + ID do Projeto + “_” + (numeração sequencial iniciada por 0001)
Sendo que:
o	Os identificadores dos projetos (ID do Projeto) devem ser únicos na empresa, ou seja, nenhum projeto poderá apresentar o mesmo identificador. Sugere-se que o identificador seja composto pela sigla do projeto composta de 3 a 5 letras em maiúsculo.


### 3.1.4 Estrutura do Repositório de Versões
O repositório de versões são definidos três branches principais: master, stage e develop.

O branch 'master' é o ramo principal, onde terá as versões estáveis e testadas.
O branch 'stage' é o ramo de estágio intermediário, onde o código é testado em um ambiente idêntico ao de produção.
O branch 'develop' é o ramo onde terá todas as mudanças realizadas que farão parte de uma release. Deste brach 'develop' irão surgir vários outros branchs, e estes serão responsáveis por novas funcionalidades.
Os branchs de correções urgentes ('hotfix') são reparos realizados diretamente na versão que está em produção ('master').

![alt text](http://www.twistsystems.com/media/cms_page_media/2013/1/14/gitflow-model.png "Git flow")

3.2 Controle de Configuração e Mudança
--------------------------------------

### 3.2.1 Processamento e Aprovação de Solicitações de Mudança
Para todas as mudanças,  o cadastro e controle serão realizados na Ferramenta de
Gestão de Projetos.
As liberações dos artefatos só acontecerão após a aprovação do Comitê de Avaliação 
de Mudança nos registros realizados na Ferramenta de Gestão de Projetos.


### 3.2.2 Comitê de Controle de Mudança (CCB)
A Comissão de Controle de Mudanças  será formada pelo Líder de Projeto, integrantes da Equipe de Qualidade e integrantes da Equipe Técnica.


4. Padrões e Procedimentos
==========================

Esse seção vai documentar os padrões usados na criação de branch's, Tag's, Commit's e no versionamento do projeto. Também será documentado o procedimento para a solicitação de mudança.

###4.1 Padrões

######4.1.1 Branch

Para a criação de novos branch's deve ser adotado o seguinte padrão:
"BUG"-<ID DO BUG>

Onde o <ID DO BUG> é o número do bug guardado no sistema de solicitação -> Motivo Bug

######4.1.2 Commit

Para executar um commit é preciso seguir a seguinte padrão:
<BRANCH><VERSÃO DO SISTEMA><ID DO REQUISITO IMPLEMENTADO><COMENTARIO>

Onde o <BRANCH> identifica o branch, <VERSÃO DO SISTEMA> identidica a versão do sistema que esta sendo modificada, <ID DO REQUISITO IMPLEMENTADO> que mostra qual a funcionalidadeesta sendo implementada segundo o documento de requisitos e um comentário do commit

######4.1.2 Tag

Para a criação de uma tag deverá seguir o seguinte padrão:
 v XX.YY.ZZ e sempre usar o atributo -m para comentar.

- A 1ª e 2ª posições (XX) indicam o primeiro bloco da identificação da versão, e será modificado quando ocorrer a inclusão de um conjunto de novas funcionalidades homologadas pelo cliente.
- A 3ª e 4ª posições (YY) indicam o segundo bloco da indicação da versão e será modificado quando ocorrer alteração em funcionalidades existentes. 
- A 5ª e 6ª posições (ZZ) indicam o último bloco da identificação da versão e será modificado na correção de um erro em qualquer funcionalidade. 


5. Treinamento e Recursos
=========================

Um breve descrição de todas as ferramentas utilizadas do projeto:

- Git é um sistema de controle de versão distribuído.
- Bugzilla é uma ferramenta baseada em Web e e-mail que dá suporte ao desenvolvimento de projetos, rastreando defeitos e servindo também como plataforma para pedidos de requisitos.
- CruiseControl é um ferramenta de integração continua e um extenso framework para criação e controle do processo de compilação continua.
- Eclipse é a IDE de desenvolvimento.
- Sonar é uma plataforma para melhorar a qualidade do software.
- Maven é uma ferramenta de automação de compilação utilizada primariamente em projetos Java.

Com o objetivo de capacitar todos os participantes do projeto será feito um treinamento das ferramentas utilizadas. 

Microsoft Project: Victor
GIT avançado: Yanko  
GIT intermediário: Diego, Luiz, Victor  
Bugzilla: Todos  
CruiseControl: Yanko, Luiz  
Sonar: Todos  
Maven: Todos  
IDE Eclipse: Diego, Luiz, Yanko  


6. Auditorias de Configuração
=============================

A verificação deve ocorrer a cada fim de interação e caso haja algum itens em desacordo com os padrões definidos no PGC serão reportados ao responsável para correção imediata.
