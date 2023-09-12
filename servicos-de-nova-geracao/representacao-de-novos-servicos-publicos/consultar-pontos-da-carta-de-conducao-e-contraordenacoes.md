---
layout: default
title: Consultar pontos da carta de condução e contraordenações
parent: Representação de novos serviços públicos
nav_order: 1
---

# Consultar pontos da carta de condução e contraordenações

Descrição da Arquitetura do Serviço Digital
{: .fs-5 .fw-300 }

Estes serviços digitais possibilitam ao cidadão consultar os pontos da carta de condução e consultar processos de contraordenação rodoviária, na nova área dedicada ao condutor, no portal [ePortugal](https://eportugal.gov.pt/).

## Partes Interessadas

#### ANSR

A **Autoridade Nacional de Segurança Rodoviária** é um serviço central da administração direta do Estado dotado de autonomia administrativa. A ANSR tem por missão o planeamento e coordenação a nível nacional de apoio à política do Governo em matéria de segurança rodoviária, bem como a aplicação do direito contraordenacional rodoviário.

Gere atualmente o Portal das Contraordenações, que tem um plano de evolução que prevê a reformulação dos serviços neste disponibilizados, através da criação da área do condutor, no ePortugal.

Disponibilizará os serviços de Consulta de pontos da carta de condução e Consulta de processos de contraordenação rodoviária no Balcão do Condutor, através de uma integração realizada pela plataforma comum: Plataforma de Integração (iAP-PI).

#### AMA

A **Agência para Modernização Administrativa** é o instituto público responsável pela promoção e desenvolvimento da modernização administrativa em Portugal. A sua atuação divide-se em três eixos: atendimento, transformação digital e inovação e participação, e encontra-se sob superintendência e tutela do [Secretário de Estado da Digitalização e da Modernização Administrativa](https://www.portugal.gov.pt/pt/gc23/primeiro-ministro/secretarios-de-estado?i=digitalizacooedamodernizacooadministrativa).

Gere atualmente o [Portal das Contraordenações](https://portalcontraordenacoes.ansr.pt/\_layouts/pages/login.aspx?ReturnUrl=%2f\_layouts%2fAuthenticate.aspx%3fSource%3d%252F%255Flayouts%252Fpages%252Fdefault%252Easpx\&Source=%2F%5Flayouts%2Fpages%2Fdefault%2Easpx), que tem um plano de evolução que prevê a reformulação dos serviços neste disponibilizados, através da criação da área do condutor, no [ePortugal](https://eportugal.gov.pt/).

Disponibilizará os serviços de Consulta de pontos da carta de condução e Consulta de processos de contraordenação rodoviária no Balcão do Condutor, através do sistema SIGA da ANSR (Sistema de Informação e Gestão de Autos) integrado com a Plataforma de Integração (iAP-PI).

#### IMT

O **Instituto da Mobilidade e dos Transportes**, instituto público integrado na administração indireta do Estado, dotado de autonomia administrativa e financeira e património próprio. O IMT, I.P. sucede nas atribuições: do Instituto de Infraestruturas Rodoviárias, I.P.; do Instituto Portuário e dos Transportes Marítimos, I.P.; da Comissão de Planeamento de Emergência dos Transportes Terrestres

O IMT, I.P. integra ainda as atribuições da SIEV - Sistema de Identificação Eletrónica de Veículos, S.A., respeitantes à exploração e gestão do sistema de identificação eletrónica de veículos.

Disponibiliza na área Balcão do Condutor, informação sobre a carta de condução do cidadão proveniente do seu sistema SICC (Sistema de Informação do Condutor e da Emissão de Títulos de Condução).

## Visão da arquitetura

Os serviços Consulta de pontos da carta de condução e Consulta de processos de contraordenação rodoviária, são serviços atualmente disponíveis a cidadãos registados no Portal das Contraordenações, gerido pela ANSR.

No Portal das Contraordenações o cidadão tem acesso aos serviços de Consulta de processos de contraordenação rodoviária; Consulta de Cadastro; e Consulta de Pontos da Carta de Condução. Pode também apresentar requerimentos: defesas, pedido de pagamento da coima em prestações e pedido de Consulta de processos de contraordenação rodoviária.

Para aceder a estes serviços, o cidadão tem de aceder ao Portal das Contraordenações, e autenticar-se com cartão de cidadão, chave móvel digital, ou número de identificação fiscal (NIF) e palavra-passe.

O Portal das Contraordenações tem um plano evolutivo definido, recomendado pelo TicAPP, que prevê a reformulação destes serviços, através da criação do novo Balcão do Condutor, que pretende centralizar a informação e o acesso a serviços associados ao evento de conduzir um veículo em Portugal.

O Balcão do Condutor será disponibilizado no portal ePortugal, o que permitirá não só aumentar o alcance dos serviços no canal digital, mas também lançar as bases para a sua disponibilização através do canal telefónico e do canal presencial, neste último, no modelo digital assistido, integrando o catálogo de serviços dos Espaços de Cidadão.

Os diagramas de arquitetura apresentados aqui foram definidos com base no [_blueprint_ destes serviços digitais](https://labx.gov.pt/wp-content/uploads/2022/02/BLUEPRINT-Consulta-de-pontos-e-historico-contraordenacoes-1.pdf) e estão de acordo com a representação do [metamodelo](../arquitetura-de-referencia-para-a-nova-geracao-de-servicos-publicos-digitais/metamodelo.md) definido na Arquitetura de Referência para a nova geração de serviços públicos digitais. &#x20;

Apresenta:

* O processo na vertente de negócio;
* O reflexo do processo de negócio, nas etapas do processo aplicacional da solução a desenvolver.
* A realização de cada etapa do processo aplicacional quer por novos componentes a desenvolver, quer por plataformas comuns reutilizáveis.

### Necessidades de negócio

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Necessidade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Criar o Balcão do Condutor</td>
    <td>
      <p>É necessário um ponto único de acesso, para os serviços associados ao evento conduzir um veículo em Portugal.</p>
      <p>A criação do novo Balcão do Condutor, no portal <a href="../../plataformas-comuns-da-administracao-publica/eportugal/">ePortugal</a>, permitirá centralizar estes serviços e facilitar o seu acesso.</p>
    </td>
  </tr>
  <tr>
    <td>A informação resultante dos serviços de consulta de pontos da carta de condução e consulta de processos de contraordenação rodoviária é disponibilizada pela ANSR</td>
    <td>
      <p>Os serviços serão apresentados na página do Balcão do Condutor, no portal ePortugal.</p>
      <p>Quando o cidadão selecionar o serviço “Consulta de pontos da carta de condução” ou o serviço “Consulta de processos de contraordenação rodoviária”, o Sistema da ANSR disponibilizará os resultados ao Balcão do Condutor, através de uma integração realizada pela <a href="../../plataformas-comuns-da-administracao-publica/plataforma-de-integracao-da-ap-iap-pi/">Plataforma de Integração (iAP-PI)</a>.</p>
    </td>
  </tr>
  <tr>
    <td>Quaisquer integrações utilizam a <a href="../../plataformas-comuns-da-administracao-publica/plataforma-de-integracao-da-ap-iap-pi/">Plataforma de Integração (iAP-PI)</a></td>
    <td>As integrações necessárias para realizar os serviços e apresentar os resultados ao cidadão, deverão utilizar a plataforma comum: <a href="../../plataformas-comuns-da-administracao-publica/plataforma-de-integracao-da-ap-iap-pi/">Plataforma de Integração (iAP-PI)</a>.</td>
  </tr>
  <tr>
    <td>Autenticar utilizando plataforma comum: plataforma do <a href="../../plataformas-comuns-da-administracao-publica/servico-de-autenticacao/">Serviço de Autenticação</a></td>
    <td>O Balcão do Condutor deverá utilizar a plataforma comum plataforma do <a href="../../plataformas-comuns-da-administracao-publica/servico-de-autenticacao/">Serviço de Autenticação</a> para o cidadão se autenticar no mesmo.</td>
  </tr>
</table>


### Pressupostos

* Os serviços serão disponibilizados no Balcão do Condutor, que será acedido através do portal ePortugal;
* O Balcão do Condutor estará integrado com o Sistema SIGA da ANSR, responsável por disponibilizar a informação resultante dos serviços de consulta de pontos da carta de condução e de Consulta de processos de contraordenação rodoviária;
* O Balcão do Condutor estará integrado com o Sistema SICC do IMT, responsável por disponibilizar informação sobre a carta de condução do cidadão;
* No Balcão do Condutor será apresentada uma lista de serviços relacionados ao evento de conduzir um veículo em Portugal;
* Os serviços requerem a autenticação do cidadão para serem utilizados;
* A apresentação da informação que consta no Balcão carece de consentimento/ autorização prévia do cidadão aos dados ali apresentados, aquando da primeira vez que acede à aplicação.

## Arquiterura de negócio

### Consulta de pontos da carta de condução

#### **Serviço**

Consulta de pontos da carta de condução.

<div style="text-align: center;">
  <img src="../../assets/images/image%20(8).png" alt="Vista alto nível do serviço Consulta de pontos da carta de condução">
</div>
 <div style="text-align: center;">Vista alto nível do serviço Consulta de pontos da carta de condução</div>

<br>

#### **Objetos de negócio do serviço**

* Carta de condução - Documento pelo qual a habilitação de conduzir um veículo é válida.

#### **Utilizadores do serviço**

* Condutor - Acede ao Balcão do Condutor no portal ePortugal e autentica-se com o Cartão de Cidadão ou Chave Móvel Digital. Consulta o serviço consulta de pontos da carta de condução.

#### Processo de negócio

Consultar pontos da carta de condução.

<div style="text-align: center;">
  <img src="../../assets/images/image%20(19).png" alt="Vista do Processo de Negócio do serviço Consultar pontos da carta de condução">
  Vista do Processo de Negócio do serviço Consultar pontos da carta de condução
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Atividade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Acesso via redes sociais</td>
    <td>O processo começa com o acesso do cidadão à página de Enquadramento do Balcão do Condutor, via redireccionamento de rede social.</td>
  </tr>
  <tr>
    <td>Acesso via ePortugal</td>
    <td>O processo começa com o acesso do cidadão ao portal ePortugal.</td>
  </tr>
  <tr>
    <td>Acesso via motor de pesquisa</td>
    <td>O processo começa com o acesso do cidadão à página da ficha do serviço, via resultado de uma pesquisa na internet.</td>
  </tr>
  <tr>
    <td>Visualizar página de enquadramento</td>
    <td>Na página de enquadramento do Balcão do Condutor, o cidadão seleciona o serviço, sendo encaminhado para a página da ficha do serviço do mesmo.</td>
  </tr>
  <tr>
    <td>Selecionar destaque Balcão do Condutor</td>
    <td>No portal ePortugal, o cidadão seleciona o destaque do Balcão do Condutor e é encaminhado para a página de enquadramento do Balcão do Condutor.</td>
  </tr>
  <tr>
    <td>Selecionar serviço no quadro de serviços</td>
    <td>No portal ePortugal, o cidadão seleciona o serviço no quadro de serviços e é encaminhado para a página da ficha de serviço.</td>
  </tr>
  <tr>
    <td>Pesquisar e selecionar serviço</td>
    <td>No portal ePortugal, o cidadão pesquisa pelo serviço e ao selecioná-lo é encaminhado para a página da ficha de serviço.</td>
  </tr>
  <tr>
    <td>Visualizar ficha de serviço</td>
    <td>Na página da ficha de serviço, é apresentada a informação sobre o serviço.</td>
  </tr>
  <tr>
    <td>Autenticar</td>
    <td>O cidadão efetua o login, utilizando o cartão de cidadão, ou chave móvel digital.</td>
  </tr>
  <tr>
    <td>Visualizar área Balcão do Condutor</td>
    <td>Após o login, o cidadão é encaminhado para a página inicial do Balcão do Condutor.</td>
  </tr>
  <tr>
    <td>Consultar Pontos</td>
    <td>Na página inicial do Balcão do Condutor, o cidadão pode visualizar a informação referente aos seus pontos da carta de condução.</td>
  </tr>
</table>


### Consulta de processos de contraordenação rodoviária

#### Serviço

Consulta de processos de contraordenação rodoviária.

<div style="text-align: center;">
  <img src="../../assets/images/image%20(16).png" alt="Vista alto nível do serviço Consulta de processos de contraordenação rodoviária">
  Vista alto nível do serviço Consulta de processos de contraordenação rodoviária
</div>
<br>

#### Objetos de negócio do serviço

Contraordenação - Define-se como contraordenação rodoviária todo o facto ilícito e censurável que preencha um tipo legal correspondente á violação de norma do Código da Estrada e de legislação complementar, para a qual se estabeleça uma coima (art.º 131º do Código da Estrada).

#### Utilizadores do serviço

Condutor:

* Acede ao Balcão do Condutor no ePortugal, e autentica-se com o Cartão de Cidadão ou Chave Móvel Digital.&#x20;
* Consulta o serviço Consulta de processos de contraordenação rodoviária.

#### Processo de negócio

Consulta de processos de contraordenação rodoviária.

<div style="text-align: center;">
  <img src="../../assets/images/image%20(26).png" alt="Vista do Processo de Negócio Consulta de processos de contraordenação rodoviária">
  Vista do Processo de Negócio Consulta de processos de contraordenação rodoviária
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Atividade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Acesso via redes sociais</td>
    <td>O processo começa com o acesso do cidadão à página de enquadramento do Balcão do Condutor, via redirecionamento de rede social.</td>
  </tr>
  <tr>
    <td>Acesso via ePortugal</td>
    <td>O processo começa com o acesso do cidadão ao portal ePortugal.</td>
  </tr>
  <tr>
    <td>Acesso via motor de pesquisa</td>
    <td>O processo começa com o acesso do cidadão à página da ficha do serviço, via resultado de uma pesquisa na internet.</td>
  </tr>
  <tr>
    <td>Visualizar página de enquadramento</td>
    <td>Na página de enquadramento do Balcão do Condutor, o cidadão seleciona o serviço, sendo encaminhado para a página da ficha do serviço do mesmo.</td>
  </tr>
  <tr>
    <td>Selecionar destaque Balcão do Condutor</td>
    <td>No portal ePortugal, o cidadão seleciona o destaque do Balcão do Condutor e é encaminhado para a página de enquadramento do Balcão do Condutor.</td>
  </tr>
  <tr>
    <td>Selecionar serviço no quadro de serviços</td>
    <td>No portal ePortugal, o cidadão seleciona o serviço no quadro de serviços e é encaminhado para a página da ficha de serviço.</td>
  </tr>
  <tr>
    <td>Pesquisar serviço e selecionar serviço</td>
    <td>No portal ePortugal, o cidadão pesquisa pelo serviço e ao selecioná-lo é encaminhado para a página da ficha de serviço.</td>
  </tr>
  <tr>
    <td>Visualizar ficha de serviço</td>
    <td>Na página da ficha de serviço, é apresentada a informação sobre o serviço.</td>
  </tr>
  <tr>
    <td>Autenticar</td>
    <td>O cidadão efetua o login, utilizando o cartão de cidadão ou chave móvel digital.</td>
  </tr>
  <tr>
    <td>Visualizar área Balcão do Condutor</td>
    <td>Após o login, o cidadão é encaminhado para a página inicial do Balcão do Condutor.</td>
  </tr>
  <tr>
    <td>Consultar processo contraordenação rodoviária</td>
    <td>Na página do Balcão do Condutor, o cidadão pode visualizar a informação referente aos Processos de contraordenação rodoviária.</td>
  </tr>
</table>


## Arquitetura aplicacional

### Consulta de pontos da carta de condução

#### Processo aplicacional

Consultar pontos da carta de condução.

<div style="text-align: center;">
  <img src="../../assets/images/image%20(18).png" alt="Vista do Processo Aplicacional do serviço Consultar Pontos da Carta de Condução">
  Vista do Processo Aplicacional do serviço Consultar Pontos da Carta de Condução
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Atividade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Apresentação de conteúdos do ePortugal</td>
    <td>Apresentação de Conteúdos do ePortugal</td>
  </tr>
  <tr>
    <td>Autenticação com single sign-on</td>
    <td>
      <p>O cidadão seleciona o serviço a que pretende aceder no portal ePortugal. É redirecionado para a página correspondente ao serviço, de acordo com o mapeamento definido na ficha de serviço.</p>
      <p>Neste caso, a realização do serviço requer a prévia autenticação do cidadão.</p>
      <p>A recolha dos dados de autenticação é feita pela plataforma comum <a href="../../plataformas-comuns-da-administracao-publica/servico-de-autenticacao/">Serviço de Autenticação</a>, que:</p>
      <ul>
        <li>informa o cidadão dos dados que serão recolhidos, de acordo com o solicitado pela solução;</li>
        <li>aceita e valida as credenciais de autenticação introduzidas pelo cidadão;</li>
        <li>obtém e transmite à solução, os dados solicitados.</li>
      </ul>
      <p>Após a autenticação com sucesso do cidadão, o controlo é atribuído à solução.</p>
    </td>
  </tr>
  <tr>
    <td>Apresentação de conteúdos da área Balcão do Condutor</td>
    <td>
      A apresentação dos conteúdos do Balcão do Condutor é gerida pela solução aplicacional Balcão do Condutor e apresentada através do portal ePortugal.gov. A página inicial do Balcão do Condutor apresenta informação relativa aos dados da carta de condução, o saldo dos pontos da carta de condução e sobre os processos de contraordenação rodoviária do cidadão, que é disponibilizada pelo sistema SICC do IMT e o Sistema SIGA da ANSR respetivamente. Estes sistemas estão integrados com o Balcão do Condutor através da plataforma comum: Plataforma de Integração (iAP-PI).
    </td>
  </tr>
  <tr>
    <td>Apresentar informação sobre Carta de Condução</td>
    <td>O Sistema SICC do IMT realiza o serviço responsável por apresentar a informação sobre a carta de condução do cidadão, no Balcão do Condutor.</td>
  </tr>
  <tr>
    <td>Apresentar pontos</td>
    <td>A Plataforma de Integração (iAP-PI) realiza um pedido ao componente de backoffice do Sistema SIGA da ANSR, e este retorna a informação referente aos pontos da carta de condução do cidadão, que são apresentados na página do Balcão do Condutor.</td>
  </tr>
</table>


A realização das etapas do processo aplicacional, é suportada pelas soluções:

<div style="text-align: center;">
  <img src="../../assets/images/image%20(27).png" alt="Vista das Solução Aplicacionais que suportam o serviço Consulta de pontos da carta de condução">
  Vista das Solução Aplicacionais que suportam o serviço Consulta de pontos da carta de condução
</div>
<br>


<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Solução Aplicacional</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Serviços</th>
  </tr>
  <tr>
    <td>Balcão do Condutor</td>
    <td>
      <p>A solução Balcão do Condutor é acedida através do portal ePortugal.GOV, e disponibiliza ao cidadão um “balcão” com diversos serviços relacionados ao evento conduzir em Portugal.</p>
      <p>Toda a informação apresentada é proveniente dos sistemas das entidades através da Plataforma de Integração (iAP-PI).</p>
      <p>Ainda backend da solução “Balcão do Condutor”, este integra com o gestor de eventos através de uma API Rest. É através desta API que o Balcão envia para o gestor os eventos (atividades) previamente definidos.</p>
    </td>
  </tr>
  <tr>
    <td>SIGA</td>
    <td>O Componente de Backoffice do Sistema SIGA da ANSR realiza o serviço “Disponibilizar informação sobre Pontos”, que está integrado com o Balcão do Condutor através da Plataforma de Integração (iAP-PI).</td>
  </tr>
  <tr>
    <td>SICC</td>
    <td>O Componente de Backoffice do Sistema SICC do IMT realiza o serviço “Disponibilizar info sobre carta de condução”, de modo a apresentar esta informação no Balcão do Condutor.</td>
  </tr>
</table>


E é suportada também pelas Plataformas Comuns:

<div style="text-align: center;">
  <img src="../../assets/images/image%20(4).png" alt="Vista das Plataformas comuns utilizadas no serviço Consulta de pontos da carta de condução">
  Vista das Plataformas comuns utilizadas no serviço Consulta de pontos da carta de condução
</div>
<br>


<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Plataforma Comum</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Serviços</th>
  </tr>
  <tr>
    <td>ePortugal.gov</td>
    <td>Realiza o serviço de acesso eletrónico aos serviços públicos.</td>
  </tr>
  <tr>
    <td>Catálogo de Entidades e Serviços (CES)</td>
    <td>A apresentação da página inicial feita pela interface do ePortugal, com base na informação registada na Ficha do Serviço no CES pela Entidade Aderente responsável pelo serviço, onde consta também o destino e o tipo do redireccionamento a realizar.</td>
  </tr>
  <tr>
    <td>Plataforma do Serviço de Autenticação</td>
    <td>Realiza o serviço de autenticação no portal ePortugal.</td>
  </tr>
  <tr>
    <td>Plataforma de Integração (iAP-PI)</td>
    <td>Realiza a integração entre o Balcão do Condutor e o serviço de consulta de pontos da carta de condução, realizado pelo Sistema da ANSR.</td>
  </tr>
  <tr>
    <td>Gestor de Eventos</td>
    <td>Disponibiliza os serviços e interfaces necessários para coletar, catalogar e armazenar os atributos que caracterizam os eventos ocorridos no Balcão do condutor. Como exemplo de eventos, temos o pedido de consulta de pontos e a respetiva resposta via iAP-PI aos serviços aplicacionais do SIGA.</td>
  </tr>
</table>


#### Arquitetura completa do serviço

<div style="text-align: center;">
  <img src="../../assets/images/MicrosoftTeams-image%20(8).png" alt="Vista Global do serviço Consulta de pontos da carta de condução">
  Vista Global do serviço Consulta de pontos da carta de condução
</div>
<br>


### &#x20;Consulta de processos de contraordenação rodoviária

#### Processo aplicacional

Consultar Processos de Contraordenação Rodoviária.

<div style="text-align: center;">
  <img src="../../assets/images/image%20(23).png" alt="Vista do Processo Aplicacional Consultar processos de contraordenação rodoviária">
  Vista do Processo Aplicacional Consultar processos de contraordenação rodoviária
</div>
<br>


<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Atividade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Apresentação de Conteúdos do ePortugal</td>
    <td>
      <p>Ao aceder ao portal ePortugal, o cidadão pode pesquisar pelos serviços disponíveis.</p>
      <p>Ao clicar no serviço que pretende realizar, o cidadão é redirecionado para a ficha de serviço.</p>
      <p>A apresentação da página inicial é feita pela interface do ePortugal, com base na informação registada na Ficha do Serviço no CES, pela Entidade Aderente responsável, onde também consta o destino e o tipo do redireccionamento a realizar.</p>
    </td>
  </tr>
  <tr>
    <td>Autenticação com single sign-on</td>
    <td>
      <p>O cidadão seleciona o serviço a que pretende aceder no portal ePortugal. É redirecionado para a página correspondente ao serviço, de acordo com o mapeamento definido na Ficha de Serviço.</p>
      <p>Neste caso, a realização do serviço requer a prévia autenticação do cidadão.</p>
      <p>A recolha dos dados de autenticação é feita pela plataforma comum <a href="../../plataformas-comuns-da-administracao-publica/servico-de-autenticacao/">Serviço de Autenticação</a> que:</p>
      <ul>
        <li>informa o cidadão dos dados que serão recolhidos, de acordo com o solicitado pela solução;</li>
        <li>aceita e valida as credenciais de autenticação introduzidas pelo cidadão;</li>
        <li>obtém e transmite à solução, os dados solicitados.</li>
      </ul>
      <p>Após a autenticação com sucesso do cidadão, o controlo é atribuído à solução.</p>
    </td>
  </tr>
  <tr>
    <td>Apresentação de Conteúdos da Área Balcão do Condutor</td>
    <td>
      <p>A apresentação dos conteúdos do Balcão do Condutor é gerida pela solução aplicacional Balcão do Condutor e apresentada através do portal ePortugal.gov. A página inicial do Balcão do Condutor apresenta informação relativa aos dados da carta de condução, o saldo dos pontos da carta de condução e sobre os processos de contraordenação rodoviária do cidadão, que é disponibilizada pelo sistema SICC do IMT e o Sistema SIGA da ANSR respetivamente. Estes sistemas estão integrados com o Balcão do Condutor através da plataforma comum: Plataforma de Integração (iAP-PI).</p>
    </td>
  </tr>
  <tr>
    <td>Apresentar Informação sobre Carta de Condução</td>
    <td>
      <p>O Sistema SICC do IMT disponibiliza a informação sobre a carta de condução do cidadão no Balcão do Condutor, através da plataforma comum: Plataforma de Integração (iAP-PI).</p>
    </td>
  </tr>
  <tr>
    <td>Apresentar Processos de Contraordenação Rodoviária</td>
    <td>
      <p>A Plataforma de Integração (iAP-PI) realiza um pedido ao componente de backend (Webservices) do Sistema SIGA da ANSR, e este retorna informação referente aos processos de contraordenação rodoviária do cidadão, que são apresentados na página do Balcão do Condutor.</p>
    </td>
  </tr>
</table>



A realização das etapas do processo aplicacional, é suportada pelas soluções:

<div style="text-align: center;">
  <img src="../../assets/images/image%20(20).png" alt="Vista das Soluções Aplicacionais que suportam o serviço Consulta de processos de contraordenação rodoviária">
  Vista das Soluções Aplicacionais que suportam o serviço Consulta de processos de contraordenação rodoviária
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Solução Aplicacional</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Serviços</th>
  </tr>
  <tr>
    <td>Balcão do Condutor</td>
    <td>
      <p>A solução Balcão do Condutor é acedida atraves do portal ePortugal.GOV, e disponibiliza ao cidadão um “balcão” com diversos serviços relacionados ao evento conduzir em Portugal.</p>
      <p>Toda a informação apresentada é proveniente dos sistemas das entidades através da Plataforma de Integração (iAP-PI).</p>
      <p>Ainda backend da solução “Balcão do Condutor”, este integra com o gestor de eventos através de uma API Rest. É através desta API que o Balcão envia para o gestor os eventos (atividades) previamente definidos.</p>
    </td>
  </tr>
  <tr>
    <td>SIGA</td>
    <td>
      <p>Os componentes de backend do sistema SIGA da ANSR realizam os serviços aplicacionais necessários (Webservices) que permitem a execução dos pedidos “Consulta contraordenações”, que está integrado com o Balcão do Condutor através da Plataforma de Integração (iAP-PI).</p>
    </td>
  </tr>
  <tr>
    <td>SICC</td>
    <td>
      <p>Os componentes de backend do Sistema SICC da IMT realizam os serviços aplicacionais necessários (Webservices) que permitem a execução dos pedidos “Obter dados da Carta de Condução”, que está integrado com o Balcão do Condutor através da Plataforma de Integração (iAP-PI).</p>
    </td>
  </tr>
</table>




E é suportada também pelas Plataformas Comuns:

<div style="text-align: center;">
  <img src="../../assets/images/image%20(22).png" alt="Vista das Plataformas comuns utilizadas no serviço Consulta de Processos de contraordenação rodoviária">
  Vista das Plataformas comuns utilizadas no serviço Consulta de Processos de contraordenação rodoviária
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Plataforma Comum</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Serviços</th>
  </tr>
  <tr>
    <td>ePortugal.gov</td>
    <td>Realiza o serviço de acesso eletrónico aos serviços públicos.</td>
  </tr>
  <tr>
    <td>Catálogo de Entidades e Serviços (CES)</td>
    <td>
      A apresentação da página inicial feita pela interface do ePortugal, com base na informação registada na Ficha do Serviço no CES pela Entidade Aderente responsável pelo serviço, onde consta também o destino e o tipo do redireccionamento a realizar.
    </td>
  </tr>
  <tr>
    <td>Plataforma do Serviço de Autenticação</td>
    <td>Realiza o serviço de autenticação no portal ePortugal.</td>
  </tr>
  <tr>
    <td>Plataforma de Integração (iAP-PI)</td>
    <td>Realiza a integração entre o Balcão do Condutor e o serviço de Consulta de processos de contraordenação rodoviária realizado pelo Sistema da ANSR.</td>
  </tr>
  <tr>
    <td>Gestor de Eventos</td>
    <td>
      Disponibiliza os serviços e interfaces necessários para coletar, catalogar e armazenar os atributos que caracterizam os eventos ocorridos no Balcão do condutor. Como exemplo de eventos, temos o pedido de consulta de contraordenações e a respetiva resposta via iAP-PI aos serviços aplicacionais do SIGA.
    </td>
  </tr>
</table>


#### Arquitetura completa do serviço

Arquitetura completa do serviço consulta de processos de contraordenação rodoviária.


<div style="text-align: center;">
  <img src="../../assets/images/MicrosoftTeams-image%20(9).png" alt="Vista Global do serviço Consulta de processos de contraordenação rodoviária">
  Vista Global do serviço Consulta de processos de contraordenação rodoviária
</div>
<br>


A representação apresentada tem por base o [metamodelo](../arquitetura-de-referencia-para-a-nova-geracao-de-servicos-publicos-digitais/metamodelo.md) definido na Arquitetura de Referência.

