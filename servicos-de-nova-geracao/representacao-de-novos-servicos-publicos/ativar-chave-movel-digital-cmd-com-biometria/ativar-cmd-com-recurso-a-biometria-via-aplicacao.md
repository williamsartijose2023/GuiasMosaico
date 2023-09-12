---
title: Ativar CMD com recurso à biometria via Aplicação
layout: default
parent: Ativar Chave Móvel Digital (CMD) com biometria
grand_parent: Representação de novos serviços públicos
nav_order: 1
---

# Ativar CMD com recurso à biometria via Aplicação

Descrição da Arquitetura do Serviço Digital
{: .fs-5 .fw-300 }

O novo serviço digital “Ativação da chave móvel digital com recurso a biometria via aplicação”, será mais uma opção para ativar a sua Chave Móvel Digital. Através de um serviço, disponibilizado a partir da aplicação Autenticação.gov, o cidadão poderá realizar o registo na CMD através da recolha de dados biométricos, utilizando o reconhecimento facial, com _Liveness Detection_, como mecanismo de validação da identidade, e também leitura automática dos dados do cartão de cidadão.

## Partes Interessadas

### AMA

A Agência para Modernização Administrativa é o instituto público responsável pela promoção e desenvolvimento da modernização administrativa em Portugal. A sua atuação divide-se em três eixos: atendimento, transformação digital e inovação e participação, e encontra-se sob superintendência e tutela do Secretário de Estado da Digitalização e da Modernização Administrativa.

É responsável pelas Plataformas Comuns utilizadas na solução a desenvolver, descrita neste documento.

### IRN

O Instituto dos Registos e do Notariado é um instituto público que executa e acompanha as políticas relativas aos serviços de registo, tendo em vista assegurar a prestação de serviços aos cidadãos e às empresas no âmbito da identificação civil e do registo civil, de nacionalidade, predial, comercial, de bens móveis e de pessoas coletivas. O IRN assegura, ainda, a regulamentação, o controlo e a fiscalização da atividade notarial.

No processo de Ativação de CMD com recurso a biometria, os dados fornecidos pelo cidadão deverão ser validados, através da comparação destes com os dados do cidadão no IRN.

### Visão da Arquitetura

A Chave Móvel Digital (CMD) é um meio de autenticação e assinatura digital certificado pelo Estado português, que permite ao utilizador autenticar-se em vários portais públicos ou privados, e assinar documentos digitais, com assinatura eletrónica qualificada.

A todo o cidadão é permitida a associação do seu número de identificação civil a um único número de telemóvel, podendo também associar o seu endereço de correio eletrónico. No caso de cidadão estrangeiro que não tenha número de identificação civil1, a associação é efetuada através do número de identificação fiscal constante do título de residência, do cartão de residência ou, ainda do respetivo número de passaporte.

O sistema é composto por uma palavra-chave permanente, distinta para a autenticação e assinatura, escolhida e alterável pelo utilizador, bem como por um código numérico de utilização única e temporária por cada autenticação ou assinatura.

Este código numérico de utilização única e temporária é gerado automaticamente pelo sistema da CMD, aquando da introdução da identificação do utilizador e da palavra-chave a ela associada. Estecódigo numérico é enviado por _Short Message Service (SMS)_ para o respetivo número de telemóvel ou, por push notification para a aplicação móvel (app) Autenticação.Gov (preferencial) registada pelo utilizador.

Qualquer cidadão pode pedir a ativação da sua CMD presencialmente, num Balcão de Atendimento, ou no momento de levantamento de um novo cartão de cidadão.

Pode também ativar a sua CMD online, acedendo ao site Autenticação.Gov e, escolhendo uma das seguintes opções:

1. Ativar CMD com cartão de cidadão – Neste caso, é necessário possuir um leitor de cartões e o código PIN de autenticação do cartão de cidadão;
2. Ativar CMD via Portal das Finanças – Neste caso, é necessário o NIF e senha de acesso ao Portal das Finanças. Após o pedido, é enviada uma carta com um PIN temporário, para a morada do titular do cartão de cidadão, que permite concluir a ativação da CMD.

O novo serviço digital “Ativação da chave móvel digital com recurso a biometria via aplicação”, será mais uma opção disponibilizada ao cidadão, para ativar a sua CMD.

Através de um serviço, disponibilizado a partir da aplicação Autenticação.gov, o cidadão poderá realizar o registo na CMD através da recolha de dados biométricos, utilizando o reconhecimento facial, com _Liveness Detection_, como mecanismo de validação da identidade, e também leitura automática dos dados do cartão de cidadão, em conformidade com a Lei n.º 37/2014 (com a redação introduzida pelo Decreto-Lei n.º 88/2021).

A recolha de dados biométricos, utilizando o reconhecimento facial, com _Liveness Detection_, é uma técnica em que a aplicação deteta com segurança se a fonte de uma amostra biométrica vem de uma representação falsa, por exemplo máscaras, fotografias ou vídeos, ou de um ser humano vivo.  Nesse caso, a amostra biométrica é a fotografia facial tirada durante o processo de adesão à CMD.

O diagrama de arquitetura apresentado para descrever a solução “via aplicação”, foi definido com base no documento de análise funcional deste serviço, nomeado no documento: “[CMD\_Adesao\_SIMPLEX\_Arquitetura\_Software\_v1\_4](https://amagovpt.sharepoint.com/:b:/r/sites/TicApp-Team/Documentos/03%20%E2%80%93%20Projectos/TICAPP202229%20-%20PRR%20-%20Arquitetura%20Empresarial/03%20-%20Execu%C3%A7%C3%A3o/C%20-%20Arquitetura/Representa%C3%A7%C3%A3o%20dos%205%20servicos%20publicos/Ativar%20CMD%20com%20biometria/research/CMD\_Adesao\_SIMPLEX\_Arquitetura\_Software\_v1\_4%20\(1\).pdf?csf=1\&web=1\&e=Bgzi6b)”, e também no documento: “[Manual\_do\_Utilizador\_Adesão\_Biometria\_v1.0](https://amagovpt.sharepoint.com/:w:/r/sites/TicApp-Team/Documentos/03%20%E2%80%93%20Projectos/TICAPP202229%20-%20PRR%20-%20Arquitetura%20Empresarial/03%20-%20Execu%C3%A7%C3%A3o/C%20-%20Arquitetura/Representa%C3%A7%C3%A3o%20dos%205%20servicos%20publicos/Ativar%20CMD%20com%20biometria/research/Manual\_do\_Utilizador\_Ades%C3%A3o\_Biometria\_v1.0.docx?d=w9cc9cbec41454194a89cd40e6e0fc62e\&csf=1\&web=1\&e=zS5aKN)”, e está de acordo com a representação do [metamodelo](../../arquitetura-de-referencia-para-a-nova-geracao-de-servicos-publicos-digitais/metamodelo.md) descrito na [Arquitetura de Referência para a nova geração de Serviços Públicos Digitais](../../arquitetura-de-referencia-para-a-nova-geracao-de-servicos-publicos-digitais/).

Apresenta:

* O processo na vertente de negócio;
* O reflexo do processo de negócio, nas etapas do processo aplicacional da solução a desenvolver.

A realização de cada etapa do processo aplicacional quer por novos componentes a desenvolver, quer por plataformas comuns reutilizáveis.

### Necessidades de negócio

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Necessidade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Oferecer ao cidadão um novo meio à distância para aderir à CMD.</td>
    <td>O novo serviço Ativação de CMD com recurso a biometria via Aplicação, permitirá ao cidadão utilizar a Aplicação Móvel Autenticação.gov, para realizar o processo de adesão.</td>
  </tr>
  <tr>
    <td>Oferecer ao cidadão a possibilidade de subscrever o serviço de assinatura digital.</td>
    <td>A opção de subscrever o serviço de assinatura digital, se o cidadão o pretender, deverá ser oferecida durante o processo de adesão à CMD.</td>
  </tr>
  <tr>
    <td>Confirmar o número de telefone do cidadão, através de um SMS com Código OTP.</td>
    <td>Deverá ser enviado um código OTP para o telemóvel do cidadão, como medida final de segurança e para garantir que o telemóvel que o cidadão indicou está correto.</td>
  </tr>
  <tr>
    <td>Cumprir requisitos para verificação da identificação do cidadão.</td>
    <td>Devem ser cumpridos os requisitos para verificação da identificação do cidadão indicados nos [Requisitos para verificação da identificação do cidadão](ativar-cmd-com-recurso-a-biometria-via-aplicacao.md#requisitos-para-verificacao-da-identificacao-do-cidadao).</td>
  </tr>
  <tr>
    <td>Recolher dados pessoais do cidadão.</td>
    <td>Para a ativação da CMD, será necessário recolher dados pessoais do cidadão, que serão conservados mediante prazos determinados. Para mais detalhes ver Tabela de [Dados pessoais recolhidos durante a videochamada](ativar-cmd-com-recurso-a-biometria-via-aplicacao.md#dados-pessoais-recolhidos-e-periodo-de-conservacao) e respetivo período de conservação.</td>
  </tr>
</table>

### Pressupostos

* O cidadão tem o cartão de cidadão atualizado.
* É obrigatório que o cidadão aceite os termos e condições antes de iniciar o processo de adesão.
* O cidadão associa um número de telemóvel válido à CMD.
* O cidadão define os PINS associados à CMD.

### Requisitos para verificação da identificação do cidadão

O processo de registo na CMD através da app Autenticação.gov recorre à identificação à distância do cidadão com base na combinação da verificação de diferentes fatores de autenticação, em conformidade com o Despacho n.º 2705/2021 do Gabinete Nacional de Segurança para os efeitos definidos na alínea d) do n.º 1 do artigo 24.º do Regulamento (eu) N.º 910/2014 do Parlamento Europeu e do Conselho, de 23 de julho de 2014, nomeadamente:

* Verificação que é a pessoa titular do documento de identificação que está, em tempo real, a efetuar o pedido de registo CMD, através de tecnologia _Liveness Detection_.
* Verificação que o documento de identificação apresentado é autêntico e corresponde à pessoa que está a efetuar o pedido de registo CMD.
* Verificação da comparação biométrica facial com base nos dados biométricos do cidadão que está a efetuar o pedido de registo CMD, recolhidos presencialmente pela autoridade nacional responsável pela emissão do documento de identificação, no momento da sua emissão.
* Verificação que o cidadão que está a efetuar o pedido de registo CMD tem acesso ao número de telemóvel indicado no processo.
* Verificação da comparação de dados recolhidos presencialmente pela autoridade nacional responsável pela emissão do documento de identificação, no momento da sua emissão.

### Dados pessoais recolhidos e período de conservação

Para a ativação da CMD, será necessário recolher dados pessoais discriminados na tabela abaixo. No âmbito destes serviços os dados recolhidos são também conservados pelos prazos indicados.

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Dados Pessoais</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Prazo de Conservação</th>
  </tr>
  <tr>
    <td>Fotografia do rosto e respetivo _template_ biométrico.</td>
    <td>Eliminado em processo diário, após conclusão do processo de adesão, conforme ponto 5.3.1.2 do Despacho n.º 2705/2021 do Gabinete Nacional de Segurança.</td>
  </tr>
  <tr>
    <td>Fotografia da frente e verso do cartão de cidadão.</td>
    <td>Eliminada no prazo de 10 dias, conforme ponto 19 do artigo 2º da Lei n.º 37/2014 (com a redação introduzida pelo Decreto-Lei n.º 88/2021) e, ponto 5.3.1.3 do Despacho n.º 2705/2021 do Gabinete Nacional de Segurança.</td>
  </tr>
  <tr>
    <td>Dados recolhidos aquando do pedido do cartão de cidadão (código postal, fotografia, número de Identificação civil, data de nascimento, data de expiração, nome, apelido, sexo, nacionalidade, nome do pai e nome da mãe).</td>
    <td>Apenas utilizados para validação dos documentos apresentados no registo, sendo eliminados imediatamente (à exceção dos dados necessário para o registo, indicados nos Dados relativos ao registo de atribuição da CMD).</td>
  </tr>
  <tr>
    <td>Dados relativos ao registo de atribuição da CMD (nome, apelido, data de nascimento, data de expiração do cartão de cidadão, número de telemóvel, _fingerprint_ do dispositivo, endereço de correio eletrónico, representação criptográfica da palavra-chave de autenticação, representação criptográfica da palavra-chave de assinatura.</td>
    <td>Conservados durante sete anos após o fim da validade do respetivo certificado, de acordo com a alínea f) do artigo 13º do Decreto-Lei nº 12/2021.</td>
  </tr>
</table>

### Legislação e regulamentação aplicável

* Lei n.º 37/2014, de 26 de junho, alterada pela Lei n.º 32/2017, de 1 de junho, pelo artigo 331.º da Lei n.º 71/2018, de 31 de dezembro, e pelo Decreto-Lei n.º 88/2021 de 3 de novembro.
* Portaria n.º 77/2018, de 16 de março, alterada pela Portaria n.º 190-A/2019, de 21 de junho.
* Regulamento (UE) 2016/679 do Parlamento Europeu e do Conselho, de 27 de abril de 2016, relativo à proteção das pessoas singulares no que diz respeito ao tratamento de dados pessoais e à livre circulação desses dados (RGPD).
* Lei n.º 58/2019, de 8 de agosto, que assegura a execução, na ordem jurídica nacional, do RGPD.
* Resolução do Conselho de Ministros n.º 41/2018.
* Regulamento (UE) 910/2014 do Parlamento Europeu e do Conselho, de 23 de julho de 2014, relativo à identificação eletrónica e aos serviços de confiança para as transações eletrónicas no mercado interno e que revoga a Diretiva 1999/93/CE.
* Decreto-Lei n.º 12/2021.
* Despacho n.º 2705/2021 do Gabinete Nacional de Segurança (“Identificação de pessoas físicas através de procedimentos de identificação à distância com recurso a sistemas biométricos automáticos de reconhecimento facial”).
* Despacho n.º 154/2017 do Gabinete Nacional de Segurança (“Identificação de pessoas físicas através de procedimentos de identificação à distância com recurso a videoconferência”).

## Arquitetura de negócio

### Serviço

Ativação de CMD com recurso a biometria via Aplicação

<div style="text-align: center;">
  <img src="../../../assets/images/image%20(37).png" alt="Vista alto nível do serviço">
  Vista alto nível do serviço
</div>
<br>

### Objetos de negócio do serviço

*   **Chave Móvel Digital** - A Chave Móvel Digital é um meio de autenticação e assinatura digital certificado pelo Estado português. Permite ao utilizador aceder a vários portais públicos ou privados, e assinar documentos digitais.

    A Chave Móvel Digital permite a associação do número de identificação civil a um único número de telemóvel, podendo também ser associada a um endereço de correio eletrónico. No caso de cidadão estrangeiro que não tenha número de identificação civil1, a associação é efetuada através do número de identificação fiscal constante do título de residência, do cartão de residência ou ainda do respetivo número de passaporte.
* **Assinatura Digital** - A assinatura digital possui certificados digitais associados que asseguram a identidade de quem assina um documento digital. O Estado português garante a certificação de assinaturas digitais realizadas com cartão de cidadão ou chave móvel digital.

### Utilizadores do serviço

* Cidadão - Entidade requerente da CMD. Participa no processo de adesão à CMD com recurso a biometria via Aplicação.

### Processo de negócio

Aderir à CMD com recurso a biometria via Aplicação.

<div style="text-align: center;">
  <img src="../../../assets/images/image%20(36).png" alt="Vista Completa do Processo de Negócio do serviço">
  Vista Completa do Processo de Negócio do serviço
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Atividade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Aceder à aplicação Autenticação.Gov</td>
    <td>O processo de adesão à CMD com recurso a biometria via Aplicação, é despoletado quando o cidadão abre a aplicação móvel Autenticação.Gov.</td>
  </tr>
  <tr>
    <td>Selecionar Opção Ativar</td>
    <td>Na página inicial da aplicação móvel Autenticação.Gov o cidadão visualiza um breve resumo do que é a CMD e escolhe a opção “Ativar”.</td>
  </tr>
  <tr>
    <td>Aceitar Termos e Condições</td>
    <td>O cidadão visualiza a página Termos e Conduções de adesão. Para poder continuar o fluxo é necessário que concorde com todos os pontos mencionados.</td>
  </tr>
  <tr>
    <td>Inserir Número Telemóvel</td>
    <td>O cidadão insere o número de telemóvel ao qual quer associar a CMD.</td>
  </tr>
  <tr>
    <td>Receber Código OTP</td>
    <td>O cidadão recebe um código OTP no número de telemóvel inserido, de modo a validar que o número corresponde de facto à pessoa que está a criar a CMD.</td>
  </tr>
  <tr>
    <td>Inserir Código OTP</td>
    <td>O cidadão insere o código OTP.</td>
  </tr>
  <tr>
    <td>Efetuar Leitura do Cartão de Cidadão</td>
    <td>O cidadão tira uma fotografia, frente e verso, do seu cartão de cidadão, seguindo as instruções apresentadas. Para uma correta leitura do cartão de cidadão é necessário que a fotografia cumpra determinados requisitos: boa luminosidade, arestas do cartão visíveis, sem brilhos nem manchas e dados legíveis.</td>
  </tr>
  <tr>
    <td>Inserir Código Postal</td>
    <td>O cidadão insere o seu código-postal. Se o código-postal não for o correto é apresentada uma mensagem de erro. O cidadão pode errar 3 vezes o código-postal e não haverá uma quarta tentativa. A única possibilidade será iniciar novamente o fluxo.</td>
  </tr>
  <tr>
    <td>Efetuar Reconhecimento Facial</td>
    <td>O cidadão segue as instruções para tirar uma fotografia ao seu rosto. A fotografia será comparada com a fotografia do cartão de cidadão e com a fotografia retirada da base de dados do IRN. Se as fotografias não corresponderem será apresentada uma mensagem de erro.</td>
  </tr>
  <tr>
    <td>Opção Substituir CMD existente</td>
    <td>Caso o cidadão já tenha uma conta CMD criada, é apresentada uma mensagem a questionar se o cidadão quer criar a CMD, substituindo a já existente. O cidadão escolhe a opção “Sim”.</td>
  </tr>
  <tr>
    <td>Associar Contactos</td>
    <td>O cidadão insere o Número de Telemóvel e o Email que ficarão associados à CMD.</td>
  </tr>
  <tr>
    <td>Definir Pins</td>
    <td>O cidadão insere o PIN de autenticação que pretende associar à CMD.</td>
  </tr>
  <tr>
    <td>Ativar Assinatura Digital (Opcional)</td>
    <td>O cidadão tem a opção de ativar também a Assinatura Digital. Caso escolha esta opção, o PIN de autenticação será o mesmo que o PIN da assinatura digital, a não ser que escolha a opção para definir um PIN diferente. Nesse caso, deverá inserir o PIN que pretende associar à Assinatura Digital.</td>
  </tr>
  <tr>
    <td>Receber Código OTP</td>
    <td>Será enviado um novo código OTP ao cidadão, para o número de telemóvel inserido.</td>
  </tr>
  <tr>
    <td>Inserir Código OTP</td>
    <td>O cidadão insere o código OTP.</td>
  </tr>
  <tr>
    <td>Visualizar Mensagem Sucesso</td>
    <td>O cidadão visualiza uma mensagem de sucesso e pode começar a utilizar a CMD.</td>
  </tr>
</table>


## Arquitetura aplicacional

### Processo aplicacional

Aderir à CMD por identificação à distância com recurso a Aplicação.

<div style="text-align: center;">
  <img src="../../../assets/images/image%20(30).png" alt="Vista do Processo Aplicacional">
  Vista do Processo Aplicacional
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Atividade</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Descrição</th>
  </tr>
  <tr>
    <td>Registar telemóvel</td>
    <td><p>Na aplicação móvel Autenticação.gov, o cidadão inicia o processo de adesão à CMD.</p><p>O número de telemóvel do cidadão é associado ao processo através da solução Chave Móvel Digital.</p></td>
  </tr>
  <tr>
    <td>Enviar SMS</td>
    <td>O envio de SMS ao cidadão é assegurado pela plataforma comum “iAP-Plataforma de Mensagens da AP (GAP)”</td>
  </tr>
  <tr>
    <td>Confirmar código</td>
    <td>O cidadão confirma o código OTP recebido por mensagem, na aplicação móvel Autenticação.gov.</td>
  </tr>
  <tr>
    <td>Criar Utilizador Biometria</td>
    <td>É efetuado o registo do dispositivo através do serviço “Create User Biometria” realizado pela solução Serviços Biometria.</td>
  </tr>
  <tr>
    <td>Iniciar Processo Biometria</td>
    <td>A solução Serviços Biometria realiza o serviço “Init Biometria Process”, que inicializa o processo de verificação biométrica para o userID/dispositivo.</td>
  </tr>
  <tr>
    <td>OCR CC</td>
    <td>O componente Software Validação Segurança cartão de cidadão realiza o serviço OCR, que efetua o envio da fotografia da frente e verso do cartão de cidadão, para verificação da veracidade e extração de dados.</td>
  </tr>
  <tr>
    <td>Obter Dados CC</td>
    <td>Através da Plataforma de Integração (iAP-PI), os dados do cartão de cidadão são obtidos do Sistema de Ciclo de Vida do Cartão de Cidadão (CVCC).</td>
  </tr>
  <tr>
    <td>Comparar Dados CC</td>
    <td>A solução Chave Móvel Digital compara os dados obtidos do cartão de cidadão.</td>
  </tr>
  <tr>
    <td>Check Comparação</td>
    <td>Verificação de que os dados extraídos por OCR correspondem aos dados do cartão registados no CVCC.</td>
  </tr>
  <tr>
    <td>Check Código Postal</td>
    <td>Verificação de que o código postal introduzido pelo cidadão corresponde aos dados registados no CVCC.</td>
  </tr>
  <tr>
    <td>Check Liveness</td>
    <td>O componente Liveness executa o serviço "Liveness Detection."</td>
  </tr>
  <tr>
    <td>Comparar Selfie e CC</td>
    <td>O Software de Comparação Facial executa o serviço Reconhecimento facial, comparando a fotografia tirada ao cidadão com a fotografia extraída do cartão de cidadão.</td>
  </tr>
  <tr>
    <td>Comparar Selfie e CVCC</td>
    <td>O Software de Comparação Facial executa o serviço Reconhecimento facial, comparando a fotografia tirada ao cidadão com a fotografia registada no CVCC.</td>
  </tr>
  <tr>
    <td>Check Existe CMD</td>
    <td>Verificação se já existe conta CMD para o cidadão, para o mesmo confirmar que deseja criar nova conta.</td>
  </tr>
  <tr>
    <td>Criar CMD</td>
    <td>A solução Chave Móvel Digital  efetua a criação da conta CMD.</td>
  </tr>
  <tr>
    <td>Ativar Assinatura Digital (Opcional)</td>
    <td>A ativação da assinatura digital, caso o cidadão tenha optado por esta opção, é assegurada pela plataforma comum “Assinatura Digital”</td>
  </tr>
  <tr>
    <td>Enviar SMS</td>
    <td>O envio de SMS ao cidadão é assegurado pela plataforma comum “iAP-Plataforma de Mensagens da AP (GAP)”</td>
  </tr>
  <tr>
    <td>Validar OTP</td>
    <td>Validação do código de segurança enviado por SMS para concluir a criação de conta</td>
  </tr>
</table>


### Soluções aplicacionais

A realização das etapas do processo aplicacional, é suportada pelas soluções:

<div style="text-align: center;">
  <img src="../../../assets/images/image%20(38).png" alt="Vista das Soluções Aplicacionais que suportam o serviço">
  Vista das Soluções Aplicacionais que suportam o serviço
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Solução Aplicacional</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Serviços</th>
  </tr>
  <tr>
    <td>Chave Móvel Digital</td>
    <td>A solução Chave Móvel Digital realiza os serviços: “Registry Frontend", “Registry Service” e “SCMD”, e suporta as diversas etapas do processo aplicacional “Aderir à CMD por identificação à distância com recurso a Aplicação”.</td>
  </tr>
  <tr>
    <td>Sistema de Ciclo de Vida do Cartão de Cidadão</td>
    <td>O Sistema de Ciclo de Vida do Cartão de Cidadão, através da Plataforma de Integração (iAP-PI), fornece os dados do cartão de cidadão.</td>
  </tr>
  <tr>
    <td>Aplicação Biometria</td>
    <td><p>A Aplicação Biometria é composta pelos componentes:</p><ul><li>Validação Segurança Cartão de Cidadão</li><li>Liveness</li><li>Comparação Facial</li></ul><p>Realiza também os serviços “Create User Biometria” e “Init Biometria Process”.</p></td>
  </tr>
  <tr>
    <td>Validação Segurança Cartão de Cidadão</td>
    <td><p>O componente Validação Segurança Cartão de Cidadão da Aplicação Biometria, é responsável pelo OCR dos dados constantes do cartão de cidadão (letras, algarismos e símbolos).</p><p>Assegura a comparação dados constantes na <em>Machine Readable Zone</em> (MRZ) do cartão de cidadão, com os restantes dados do cartão.</p><p>Procede também à recolha de fotografia constante do cartão de cidadão.</p><p>Na vertente de segurança é suportada por mecanismos de <em>Deep learning</em> para assegurar a segurança do cartão de cidadão, assegurando a sobreposição de microtexto, presença de símbolos base do cartão de cidadão, e verificação de presença de todos os campos.</p><p>Distinção de imagens de primeira geração de outras, detetando dessa forma imagens recolhidas de impressões, fotocópias ou fotografias de ecrãs.</p><p>Procede ainda à verificação da presença e veracidade de mecanismos de segurança do cartão de cidadão (microtexto, DOVID, janela com <em>Multiple Laser Image</em>, deteção de adulteração do Cartão, por exemplo, alteração de dados impressos, alteração de fotografia).</p><p>Solução da Polygon especializada para o cartão de cidadão Português.</p></td>
  </tr>
  <tr>
    <td>Liveness</td>
    <td><p>O componente Liveness da Aplicação Biometria realiza o serviço <em>Liveness Detection</em>.</p><p>Este serviço assegura a medida da profundidade 3D, a textura da pele, as reflexões oculares, entre outras – sem necessidade de interação por parte do cidadão, por exemplo, sem necessidade de movimentos os olhos ou face.</p><p>O serviço <em>Liveness Detection</em>, com certificação ISO/IEC 30107 (<em>Anti-Spoofing technology</em>, também designado <em>Presentation Attack Detection)</em> nível 1 + nível 2 – pela iBeta, assegura a resistência a ataques com fotos, vídeos de alta resolução, máscaras de papel, máscaras 3D de resina, látex e silicone usadas por humanos.</p><p>Fornecedor: Facetec (via Polygon).</p></td>
  </tr>
  <tr>
    <td>Comparação Facial</td>
    <td><p>O componente Comparação Facial da Aplicação Biometria, é responsável pela comparação da fotografia do cartão de cidadão com a imagem extraída da fotografia tirada na etapa do processo “Efetuar Reconhecimento Facial”, e com a fotografia existente no Sistema de Ciclo de Vida do Cartão de Cidadão.</p><p>Taxa de falsos positivos (<em>False accept rate - FAR</em>) inferior ou igual a 1/10 000 000, com taxa de falsos negativos (<em>False reject rate - FRR</em>) inferior a 2%. (<em>True acceptance rate</em> - TAR superior ou igual a 98%).</p><p>Fornecedor:  Ntechlab (via Polygon)</p></td>
  </tr>
</table>


### Plataformas comuns

É suportada pelas Plataformas comuns:

<div style="text-align: center;">
  <img src="../../../assets/images/image%20(32).png" alt="Vista das Plataformas comuns utilizadas no serviço">
  Vista das Plataformas comuns utilizadas no serviço
</div>
<br>

<table>
  <caption></caption>
  <tr>
    <th style="background-color: #f2f2f2; padding: 10px;">Plataforma Comum</th>
    <th style="background-color: #f2f2f2; padding: 10px;">Serviços</th>
  </tr>
  <tr>
    <td>Plataforma do Serviço de Autenticação</td>
    <td>A Plataforma do Serviço de Autenticação é composta pela interface Aplicação Móvel Autenticação.Gov, na qual o cidadão adere à CMD.</td>
  </tr>
  <tr>
    <td>iAP-Plataforma de Mensagens da AP (GAP)</td>
    <td>Realiza o serviço de notificação do cidadão por SMS.</td>
  </tr>
  <tr>
    <td>Plataforma de Integração (iAP-PI)</td>
    <td>Realiza a integração do Sistema de Ciclo de Vida do Cartão de Cidadão, para a obtenção dos dados do cartão do cidadão.</td>
  </tr>
  <tr>
    <td>Assinatura Digital</td>
    <td>Disponibiliza a Assinatura Digital.</td>
  </tr>
</table>



### Arquitetura completa

Arquitetura completa do serviço ativar CMD com recurso à biometria via aplicação:

<div style="text-align: center;">
  <img src="../../../assets/images/cmd%20app%206%20(1).png" alt="Vista Global do serviço">
  Vista Global do serviço
</div>
<br>

A representação apresentada tem por base o [metamodelo ](../../arquitetura-de-referencia-para-a-nova-geracao-de-servicos-publicos-digitais/metamodelo.md)e os respetivos artefactos.
