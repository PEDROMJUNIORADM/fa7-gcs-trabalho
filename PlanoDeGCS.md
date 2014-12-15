Aluguel de livros
=================
Plano de Gerenciamento de Configuração
======================================
Versão &lt;1.0&gt;
------------------

_[Observação: O template a seguir é fornecido para uso com o Rational Unified Process (RUP).  O texto exibido entre colchetes e em itálico foi incluído para orientar o autor e deve ser excluído antes da publicação do documento._

_Este documento utiliza a formatação da linguagem [Markdown] (http://daringfireball.net/projects/markdown/). Você pode encontrar um guia de referência rápido [aqui] (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).]_

Histórico de Versões
--------------------

|Data                |Versão       |Descrição               |Autor          |
|--------------------|-------------|------------------------|---------------|
|_&lt;08/12/2014&gt;_|_&lt;1.0&gt;_|_&lt;Versão inicial&gt;_|_&lt;Victor&gt;_|



1. Introdução
==============

_[A introdução do Plano de Gerenciamento de Configuração  oferece uma visão geral de todo o documento. 
Ela inclui a finalidade, o escopo, as definições, os acrônimos, as abreviações, as referências e uma visão geral deste
Plano de Gerenciamento de Configuração.]_

1.1 Finalidade
---------------
_[Especifique a finalidade deste Plano de Gerenciamento de Configuração.]_

1.2 Escopo
----------
_[Uma breve descrição do escopo deste Plano de Gerenciamento de Configuração; o modelo ao qual ele está associado e tudo o que é afetado ou influenciado por este documento.]_

1.3 Definições, Acrônimos e Abreviações
---------------------------------------
_[Esta subseção apresenta as definições de todos os termos, acrônimos e abreviações necessários para a correta interpretação do Plano de Gerenciamento de Configuração.  Essas informações podem ser fornecidas mediante referência ao Glossário do projeto.]_

1.4 Referências
---------------
_[Esta subseção apresenta uma lista completa de todos os documentos mencionados no Plano de Gerenciamento de Configuração. Identifique os documentos por título, número de relatório (se aplicável), data e organização responsável pela publicação. Especifique as fontes a partir das quais as referências podem ser obtidas. Essas informações podem ser fornecidas por um anexo ou outro documento.]_

1.5 Visão Geral
---------------
_[Esta subseção descreve o conteúdo restante do Plano de Gerenciamento de Configuração e explica como o documento está organizado.]_



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
Um projeto de desenvolvimento de software produz os seguintes itens:

-Programas (código fonte, programas executáveis, bibliotecas de componentes,  etc.)                                          
-Documentação (manuais do usuário, documento de requisitos, modelode análise e projeto, etc.)                                
-Massas de dados (dados de teste e do projeto em geral).                                                                     

Um item de configuração está sujeito a mudanças e essas devem obedecer às políticas
estabelecidas. Normalmente, um item de configuração é estabelecido para cada
pedaço de software que pode ser projetado, implementado e testado de forma Plano de Gerenciamento de Configuração independente. Documentos e massas de dados, entretanto, também são passíveis de ser considerados itens de configuração.



### 3.1.3 Baselines do Projeto

A criação de baselines pode ser realizada de acordo com os marcos do projeto ou de alguma outra forma definida pela gerência A baseline é armazenada em um repositório de itens de configuração. E, a partir desse momento, só pode ser alterado por meio de uma solicitação de alteração formal para controle de mudança.
Para cada uma das fases do modelo sugere-se a criação de baselines nos seguintes marcos:                                     
•	Fase Prospecção                                                                                                            
o	Solicitação de uma proposta pelo cliente                                                                                   
•	Fase Concepção                                                                                                             
o	Após a atividade do ciclo de desenvolvimento: Conduzir revisão do Estudo de Viabilidade do Projeto                         
•	Fase Negociação                                                                                                            
o	Após a atividade do ciclo de desenvolvimento: Conduzir revisão do Contrato                                                 
•	Fase Elaboração                                                                                                            
o	Após a atividade do ciclo de desenvolvimento: Conduzir revisão do Arquitetura do Software                                  
•	Fase Construção                                                                                                            
o	Após a atividade do ciclo de desenvolvimento: Conduzir revisão do Capacidade Operacional                                   
•	Fase Transição                                                                                                             
o	Após a atividade do ciclo de desenvolvimento: Conduzir revisão do Entrega do Produto                                       


A identificação da baseline pode ser constituída por:
“Baseline” + “_” + ID do Projeto + “_” + (numeração sequencial iniciada por 0001)
Sendo que:
o	Os identificadores dos projetos (ID do Projeto) devem ser únicos na empresa, ou seja, nenhum projeto poderá apresentar o mesmo identificador. Sugere-se que o identificador seja composto pela sigla do projeto composta de 3 a 5 letras em maiúsculo.


### 3.1.4 Estrutura do Repositório de Versões
_[Descreva a organização de diretórios do seu repositório e que itens/arquivos devem ser armazenados em cada diretório.]_

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
_[Descreva os padrões e procedimentos que devem ser seguidos no projeto. Crie subseções se achar necessário, para organizá-los melhor.]_



5. Treinamento e Recursos
=========================
_[Descreva as ferramentas de software, o pessoal e o treinamento necessários para implementar as atividades de CM especificadas.]_



6. Auditorias de Configuração
=============================
_[Descreva o cronograma das auditorias de configuração e o que será verificado. Informe também como serão reportados os problemas encontrados e onde sera feito o acompanhamento dos itens corretivos.]_
