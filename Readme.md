projeto modelo
==========================
V0.0.0
==========

1.0 - Objetivo e demais informações
------------
> O Objetivo deste repositório é servir de modelo para os demais cadastrados no GitLab


### Atenção! 

Este repositório contém os documentos relacionados ao acompanhamento e controle do projeto, além do código e binários relacionados ao projeto. Neste repositório poderão constar documentos como:

- Documento atestando a necessidade do projeto
- Documento autorizando a execução do projeto
- e-mail de aprovação do projeto
- Cronograma do projeto
- Demais informações relevantes a gestão do projeto
- Análise de requisitos e casos de uso
- Padrões arquiteturais
- Casos de Testes e evidências de Testes
- Códigos e Binários relacionados

2.0 - Tipos de Configuração
---------------

Para todos os projetos armazenados nesse repositório deve ser respeitada a seguinte configuração para os artefato e fluxo de desenvolvimento:


### 2.1	Regras de Numeração de Versão

O esquema de numeração de versões adotado é baseado no esquema adotado pela organização Apache Foundation, definindo que uma versão é composta por quatro números inteiros:

                                  «MAIOR».«MENOR».«MICRO»

sendo que a alteração desses números segue o critério:

- **MAIOR**: Existe modificação na estrutura de dados ou na arquitetura do sistema, incremental; 
- **MENOR**: Existe modificação na inclusão de um ou mais conjuntos de novas funcionalidades. Inicia com zero (zero) e deve ser reiniciado sempre que houver a troca da versão maior;
- **MICRO**: Existe correção de erros ou correção de comportamentos esperados no sistema. Inicia com zero (zero) e deve ser reiniciado sempre que houver a troca da versão maior ou da versão menor.


### 2.1 Política de Controle de Versão

Para o armazenamento dos artefatos de projeto, a equipe utilizará a ferramenta GIT. Com isso a estrutura de branches a ser criada para o fluxo de trabalho é descrita como: 

- **master**: branch que referencia a linha principal de trabalho. Recebe todas as modificações planejadas nos demais branches para a próxima versão.
- **stable**: representa a versão atual em produção. Possui a versão-base para entrega e não sofrerá mais mudanças, até que exista um outro branch master homologado e definido em uma nova versão.
- **Branches de desenvolvimento**: Durante o desenvolvimento do sistema serão necessários branches que definam a versão em que se está trabalhando as modificações. Esses branches não estão no controle da GCM, mas como boa prática se utiliza essa nomenclatura para acelerar e garantir a integridade na execução dos procedimentos de mudança. Essas versões deverão seguir o seguinte método de versionamento:

  - **EVO_*MAIOR_MENOR_MICRO***: esse padrão será utilizado quando do desenvolvimento de um novo produto ou novas funcionalidades a um produto com uso das regras definidas no item 4.1;
 
  - **COR_*MAIOR_MENOR_MICRO***: esse padrão será utilizado quando do desenvolvimento de correção de incidentes identificados no sistema com uso das regras definidas no item 4.1. 
- **Branches de backup**: representam os branches para recuperação de dados antes do merge dos branches master e stable. Essas versões deverão seguir o seguinte método de versionamento:
  - **BCK_*MAJOR_MINOR_MICRO***: configuração de versão com uso das regras definidas no item 4.1 sendo espelho do branch stable.

### 2.2 Configuração Base

A configuração bases definida ao longo do projeto deverá utilizar a seguinte regra para a nomenclatura:

                               V«MAJOR».«MINOR».«MICRO»:


### 2.3 Controle de Versões no Servidor

O repositório possui dois branches principais: o master, que recebe todas as modificações planejadas para a próxima versão, e o stable, que representa a versão atual em produção.
Os branches de desenvolvimento, quando da conclusão das etapas de construção evolutiva ou corretiva do software são mergeados ao branch master. Quando a nova versão está prestes a ser lançada, é realizado um merge entre os branches master e stable. Logo após o merge, inicia-se o período de estabilização da nova versão com o objetivo de corrigir eventuais bugs introduzidos pelas novas funcionalidades. 
Para controle de versão dos branches stable e master será utilizado o recurso de Tagging disponibilizado pelo GIT. No momento do commit das alterações realizadas dos branches EVO ou COR para o branch master e do branch master para o branch stable deverá ser marcada a Tag informando a versão conforme item 2.2

![Fluxo_Branch](http://git.mj.gov.br/CGTI-GC/projeto-modelo/uploads/4cf10e396a97dfa6d94f528d76aa348c/Fluxo_Branch.png)



### 2.4 Política de Merge

A política de merge define o fluxo básico para realização de merge das alterações ocorridas nas diversas frentes de trabalho para o repositório, garantindo a integridade e disponibilidade das informações contidas no mesmo.
 
As diversas fábricas de desenvolvimento poderão desenvolver suas demandas baseadas em um branch disponibilizado para tal finalidade. A partir do momento em que o trabalho desenvolvido necessita ser gravado no repositório, os desenvolvedores irão submeter suas alterações para repositórios alinhados conforme a gestão da fábrica. A partir desse ponto os líderes de projeto irão submeter suas alterações a GCM que por sua vez valida os artefatos e executa o merge com o repositório central. 

![Fluxo_Merge](http://git.mj.gov.br/CGTI-GC/projeto-modelo/uploads/2d5ce33c3a3b0ce4d4a5f7a8756a75c3/Fluxo_Merge.png)



### 2.4 Política de Mensagem Commit

O Padrão de Mensagens em commits no GIT será:


                                Demanda #«Número da Demanda»-«Título livre»
								
Com isso poderá ser identificado o solicitante e o executante da demanda.


## 3.0 Configuração de Repositório

O planejamento de configuração de repositório descreve a estrutura padrão mínima para atender as necessidades do MJ na guarda dos arquivos relacionados aos sistemas entregues Essa configuração é baseada na MDS do MJ e procura refletir os processos descritos na mesma.

### 3.1	Tipos de Configuração

Os tipos de configurações definidas para os projetos estão classificados de forma macro em dois grupos:

- Documentos: guarda de todos os entregáveis documentais do Sistema;
- Sistema: guarda dos artefatos de fontes/build que compõem os sistemas.

Para cada uma dessas Classificações se encontram os entregáveis para o sistema conforme MDS. O conteúdo das configurações bases pode ser listado na tabela abaixo:



| Grupo Macro | Sub Grupo | Itens de Configuração que compõem a configuração base |
|-------------|---------------------------|-------------------------------------------------------|
| | Acompanhamento e Controle | · Solicitação de Demanda |
| | | · Atas de Reuniões |
| | | · Arquivos de aprovações dos Entregáveis |
| | | · Relatórios do Projeto |
| | Gerência do Projeto | · Visão do Produto |
| | | · Glossário |
| | | · Cronograma |
| | | · Plano de Projeto |
| | Requisitos | · Modelo de análise |
| | | · Casos de uso |
| | | · Matriz de rastreabilidade |
| Documentos | | · Requisitos Suplementares |
| | Análise e Projeto | · Plano de Implantação |
| | | · Documento de arquitetura |
| | | · Documento de design |
| | | · Modelo de dados |
| | Testes | · Plano de Testes |
| | | · Casos de Teste |
| | | · Relatório de execução e evidência de testes |
| | Métricas | · Contagem estimada |
| | | · Contagem detalhada |
| | Configuração | · Matriz de Configuração |
| | | · Relatório de Auditoria de Configuração |
| | Homologação | · Termo de Aceite |
| | | · Solicitação de mudança |
|-------------|---------------------------|-------------------------------------------------------|
| Sistema | Build | · Código Fonte |
| | | · Build |



### 3.2 Padrão de nomenclatura

Os padrões de nomenclatura se encontram baseados na MDS e possui chaves identificadoras padronizadas para permitir a rastreabilidade e auditoria da documentação relacionada:

- «Acrônimo»: Conjunto de letras iniciais dos vocábulos que compõem o nome do Sistema. Segue em todos os documentos para permitir a comparação de forma facilitada entre Sistemas Diferentes;
- «AAMMDD»: Data de edição final do documento no formato:
  - AA: Ano (dois dígitos)
  - MM: Mês (dois dígitos)
  - DD: Dia (dois dígitos)
- «Título»: Informação sucinta e livre do que se trata o documento
- «ID do Caso de Uso»: Identificação numérica do caso de uso conforme MDS
- «Nome do Caso de Uso»: Nome do caso de uso conforme MDS
- «ID do Caso de Teste»: Identificação numérica do Caso de Teste
- «Nome do Caso de Teste»: Identificação do Caso de Teste



 ### 3.2.1 Documentos

Todos os documentos disponibilizados no repositório devem ser identificados baseados no seguinte padrão de nomenclatura:


| Sub-Grupo | Item de Configuração | Padrão |
|---------------------------|-----------------------------------------------|----------------------------------------------------------------------------------|
| Acompanhamento e Controle | Solicitação de Demanda * | SLD-Solicitação de Demanda-«Acrônimo» |
| | Atas de Reuniões | ATR-«AAMMDD»-«Acrônimo» «Título» |
| | Arquivos de aprovações dos Entregáveis | AAE-«AAMMDD»-«Acrônimo» «Título» |
| Gerência do Projeto | Visão do Produto * | DVP-Documento de Visão-Projeto «Acrônimo» |
| | Glossário * | GLS-Glossário «Acrônimo» |
| | Cronograma | CRN-Cronograma «Acrônimo» |
| | Plano de Projeto | PLP-Plano de Projeto «Acrônimo» |
| Requisitos | Modelo de análise * | MDA-Modelo de análise «Acrônimo» |
| | Casos de uso * | ECU-«ID do Caso de Uso» «Nome do caso de uso» «Acrônimo» |
| | Matriz de rastreabilidade * | MZR-Matriz de Rastreabilidade «Acrônimo» |
| | Requisitos Suplementares * | RQS-Requisitos Suplementares «Acrônimo» |
| Análise e Projeto | Plano de Implantação * | PLI-Plano de Implantação «Acrônimo» |
| | Documento de arquitetura * | DCA-Documento de Arquitetura «Acrônimo» |
| | Documento de design * | DCD-Documento de Design «Acrônimo» |
| | Modelo de dados * | MDD-Modelo de Dados «Acrônimo» |
| Testes | Plano de Testes * | PLT-Plano de Testes «Acrônimo» |
| | Casos de Teste * | ECT-«ID do Caso de Uso»_«ID do Caso de Teste» «Nome do caso de Teste» «Acrônimo» |
| | Relatório de execução e evidência de testes * | RET-«ID do Caso de Uso»_«ID do Caso de Teste» «Nome do caso de Teste» «Acrônimo» |
| Métricas | Contagem estimada * | PCE-«ID do Caso de Uso» «Acrônimo» |
| | Contagem detalhada * | PCD-«ID do Caso de Uso» «Acrônimo» |
| Configuração | Matriz de Configuração * | MCG-Matriz de Configuração «Acrônimo» |
| | Relatório de Auditoria de Configuração * | RAC-Relatório de Auditoria de Configuração«Acrônimo» |
| Homologação | Termo de Aceite * | TMA-Termo de Aceite «Acrônimo» |
| | Solicitação de mudança * | SDM-Solicitação de Mudança «Acrônimo» |


 ### 3.2.2 Fontes e Build

Todos o código fonte, além do próprio build do projeto estará incluída no repositório conforme MDS e não haverá um padrão de nomenclatura para os artefatos aqui disponibilizados.

| Sub-Grupo | Item de Configuração | Padrão |
|-----------|----------------------|--------|
| Build | Códigos Fonte | N/A |
| | Binários | N/A |


### 2.5 Política de Commit

Para a realização de Commits na ferramenta GIT é necessário que se identifique a Demanda que originou essa ação. Isso permite identificar quem é o executante dessa solicitação. Deve seguir o seguinte padrão:

                       Demanda #«Número da Demanda» - «Título Livre»

### 3.3 Padrão de diretórios para os artefatos

Todos os documentos, build e código fonte deverão estar disponíveis no repositório, seguindo além do padrão de nomenclatura, o padrão de organização nos diretórios conforme tabela a seguir:


![Estrutura_do_Repositório](http://git.mj.gov.br/CGTI-GC/projeto-modelo/uploads/2fe11f8d93c27e21fbdbadf949622c4b/Estrutura_do_Repositório.png)


| Item de Configuração | Caminho no Diretório |
|-----------------------------------------------|------------------------------------------------------------------------------------------------|
| Solicitação de Demanda * | /«Raiz do Projeto»/Documentos/Acompanhamento e Controle/ |
| Atas de Reuniões | /«Raiz do Projeto»/Documentos/Acompanhamento e Controle/Atas de Reuniões |
| Arquivos de aprovações dos Entregáveis | /«Raiz do Projeto»/Documentos/Acompanhamento e Controle/Arquivos de aprovações dos Entregáveis |
| Visão do Produto * | /«Raiz do Projeto»/Documentos/Gerência do Projeto |
| Glossário * | /«Raiz do Projeto»/Documentos/Gerência do Projeto |
| Cronograma | /«Raiz do Projeto»/Documentos/Gerência do Projeto |
| Plano de Projeto | /«Raiz do Projeto»/Documentos/Gerência do Projeto |
| Modelo de análise * | /«Raiz do Projeto»/Documentos/Requisitos |
| Casos de uso * | /«Raiz do Projeto»/Documentos/Requisitos/Casos de Uso |
| Matriz de rastreabilidade * | /«Raiz do Projeto»/Documentos/Requisitos |
| Requisitos Suplementares * | /«Raiz do Projeto»/Documentos/Requisitos |
| Plano de Implantação * | /«Raiz do Projeto»/Documentos/Análise e Projeto |
| Documento de arquitetura * | /«Raiz do Projeto»/Documentos/Análise e Projeto                                                |
| Documento de design * | /«Raiz do Projeto»/Documentos/Análise e Projeto |
| Modelo de dados * | /«Raiz do Projeto»/Documentos/Análise e Projeto |
| Plano de Testes * | /«Raiz do Projeto»/Documentos/Testes |
| Casos de Teste * | /«Raiz do Projeto»/Documentos/Testes/Casos de Teste |
| Relatório de execução e evidência de testes * | /«Raiz do Projeto»/Documentos/Testes/ Relatório de execução e evidência de testes |
| Contagem estimada * | /«Raiz do Projeto»/Documentos/Métricas/Contagem Estimada |
| Contagem detalhada * | /«Raiz do Projeto»/Documentos/Métricas/Contagem Detalhada |
| Matriz de Configuração * | /«Raiz do Projeto»/Documentos/Configuração |
| Relatório de Auditoria de Configuração * | /«Raiz do Projeto»/Documentos/ Configuração |
| Termo de Aceite * | /«Raiz do Projeto»/Documentos/Homologação |
| Solicitação de mudança * | /«Raiz do Projeto»/Documentos/Homologação |
| Códigos Fonte | /«Raiz do Projeto»/Build/Códigos Fonte |
| Binários | /«Raiz do Projeto»/Build/Binários |
| Documentos não Padronizados | /«Raiz do Projeto»/Documentos não Padronizados                                                 |

### 4.1 Demais Informações

Manual Básico do Git: [Git_Básico.pdf](http://git.mj.gov.br/CGTI-GC/projeto-modelo/uploads/cb72e0ee31fad80a0a5641bef64a6511/Git_Básico.pdf)

Editor de Readme avançado para o Git Lab: http://oscargodson.github.io/EpicEditor/