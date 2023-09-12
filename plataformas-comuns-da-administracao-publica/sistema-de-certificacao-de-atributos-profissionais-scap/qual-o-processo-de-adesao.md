---
layout: default
title: Qual o processo de adesão?
parent: Sistema de Certificação de Atributos Profissionais (SCAP)
nav_order: 2
---

# Qual o processo de adesão?

No âmbito do SCAP, os Fornecedores de Atributos representam as entidades certificadoras com competência para associar determinados atributos profissionais a cidadãos.  &#x20;

A integração de novos Fornecedores de Atributos no SCAP é da responsabilidade da AMA, mediante pedido direto a esta por parte dos Fornecedores de Atributos.&#x20;

Para a adesão ao SCAP seguir os procedimentos:

<div style="text-align: center;">
  <img src="../../assets/images/MicrosoftTeams-image (8) (1).png" alt="Processo de adesão ao SCAP">
  Processo de adesão ao SCAP
</div>
<br>

## Passos para Integração com o SCAP

<table>
<caption></caption>
  <tr>
    <th>Passo</th>
    <th>Entidade Responsável</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td><strong>1.Comunicar interesse de adesão</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Formalizar a intenção de integrar com o SCAP enquanto Fornecedor de Atributos através do <a href="https://www.autenticacao.gov.pt/web/guest/integracao-entidade">formulário online</a> opção Atributos Profissionais.</td>
  </tr>
  <tr>
    <td><strong>2.Celebrar Protocolo</strong></td>
    <td>AMA e Fornecedor de Atributos</td>
    <td>Celebrar o Protocolo.</td>
  </tr>
  <tr>
    <td><strong>3.Preencher Template</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Preenchimento do template partilhado pelo Fornecedor de Atributos e submissão à AMA (mantendo formato word e sem qualquer assinatura).</td>
  </tr>
  <tr>
    <td><strong>4.Validar e Assinar (AMA)</strong></td>
    <td>AMA</td>
    <td>Validação, numeração, aceitação e assinatura pelo Conselho Diretivo da AMA.</td>
  </tr>
  <tr>
    <td><strong>5.Validar e Assinar (Fornecedor)</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Validação e assinatura do representante legal (ou representantes legais aplicáveis, de acordo com o descrito na Certidão Permanente) do Fornecedor de Atributos.</td>
  </tr>
  <tr>
    <td><strong>6.Entrada em Pré-Produção</strong></td>
    <td>AMA e Fornecedor de Atributos</td>
    <td>Entrada em Ambiente de pré-produção (Ver Ambiente de pré-produção).</td>
  </tr>
  <tr>
    <td><strong>7.Entrada em Produção</strong></td>
    <td>AMA e Fornecedor de Atributos</td>
    <td>Entrada em Produção do serviço de autenticação e assinatura com SCAP (Ver Ambiente de produção).</td>
  </tr>
</table>

## Ambiente de Pré-produção

<table>
<caption></caption>
  <tr>
    <th>Passo</th>
    <th>Entidade Responsável</th>
    <th>Documentos de Suporte</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td><strong>1.Enviar informação</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Ver Informação de Suporte *1</td>
    <td>Envio de informação para configuração aplicacional da entidade.</td>
  </tr>
  <tr>
    <td><strong>2.Configurar VPN</strong></td>
    <td>AMA e Fornecedor de Atributos</td>
    <td></td>
    <td>Configuração de VPN para comunicação entre Fornecedor e iAP.</td>
  </tr>
  <tr>
    <td><strong>3.Configuração Aplicacional</strong></td>
    <td>AMA</td>
    <td>Ver Informação de Suporte *2</td>
    <td>Configuração aplicacional da entidade, e envio dos ficheiros definidos no ponto *2 ao Fornecedor.</td>
  </tr>
  <tr>
    <td><strong>4.Testar</strong></td>
    <td>Fornecedor de Atributos</td>
    <td></td>
    <td>Desenvolvimento e configuração de atributos de testes pedidos pela AMA.</td>
  </tr>
  <tr>
    <td><strong>5.Validar desenvolvimento</strong></td>
    <td>AMA</td>
    <td></td>
    <td>Validação do desenvolvimento.</td>
  </tr>
</table>

## Ambiente de Produção

<table>
<caption></caption>
  <tr>
    <th>Passo</th>
    <th>Entidade Responsável</th>
    <th>Documentos de Suporte</th>
  </tr>
  <tr>
    <td><strong>1.Relatório de cumprimento de Guidelines</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Produção de relatório assinado com evidências de cumprimento de Guidelines de Integração do SCAP (Ver Informação de Suporte *1).</td>
  </tr>
  <tr>
    <td><strong>2.Enviar Informação</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Envio de informação para configuração aplicacional da entidade.</td>
  </tr>
  <tr>
    <td><strong>3.Configurar VPN </strong></td>
    <td>AMA e Fornecedor de Atributos</td>
    <td>Configuração de VPN para comunicação entre Fornecedor e iAP.</td>
  </tr>
  <tr>
    <td><strong>4.Configuração Aplicacional</strong></td>
    <td>AMA</td>
    <td>Configuração aplicacional da entidade, e envio dos ficheiros definidos no ponto *3 ao fornecedor (Ver Informação de Suporte *3).</td>
  </tr>
  <tr>
    <td><strong>5.Adquirir certificado</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Aquisição de certificado qualificado de selo eletrónico com base no CSR gerado no passo anterior, e envio do certificado adquirido.</td>
  </tr>
  <tr>
    <td><strong>6. Atualizar Configuração Aplicacional com Certificado</strong></td>
    <td>AMA</td>
    <td>Atualização da configuração aplicacional da entidade, com o certificado adquirido pelo fornecedor.</td>
  </tr>
  <tr>
    <td><strong>7. Testar</strong></td>
    <td>Fornecedor de Atributos</td>
    <td>Configuração de atributos de testes pedidos pela AMA.</td>
  </tr>
  <tr>
    <td><strong>8. Validar desenvolvimento</strong></td>
    <td>AMA</td>
    <td>Validação do desenvolvimento.</td>
  </tr>
</table>

<p>Para a configuração em ambiente de produção os Fornecedores de Atributos têm que efetuar a aquisição de um Certificado Qualificado Selo Eletrónico com o <em>Certificate Signing Request</em> (CSR) emitido aquando da criação da conta desse fornecedor no SCAP. Para além desse CSR, <strong>é também disponibilizado um ficheiro com a password encriptada da conta do Fornecedor de Atributos e uma</strong> <em>secret key</em> que será utilizada na validação das operações. </p>



## Informação de Suporte

<table>
<caption></caption>
  <tr>
    <th>Pontos</th>
    <th>Informação de suporte</th>
    <th>Informação de suporte</th>
  </tr>
  <tr>
    <td>*1</td>
    <td>Nome completo da entidade</td>
    <td>—</td>
  </tr>
  <tr>
    <td>*1</td>
    <td>NIPC/NIF</td>
    <td>—</td>
  </tr>
  <tr>
    <td>*1</td>
    <td>CAE</td>
    <td>Código da Classificação Portuguesa de Atividades Económicas, se aplicável</td>
  </tr>
  <tr>
    <td>*1</td>
    <td>Contacto telefónico</td>
    <td>—</td>
  </tr>
  <tr>
    <td>*1</td>
    <td>Email</td>
    <td>—</td>
  </tr>
  <tr>
    <td>*1</td>
    <td>CommonName</td>
    <td>Ficará associado ao certificado - e.g. iniciais da entidade</td>
  </tr>
  <tr>
    <td>*1</td>
    <td>Localidade</td>
    <td>Ficará associada ao certificado</td>
  </tr>
  <tr>
    <td>*2 e *3</td>
    <td>SCAP_&lt;Fornecedor&gt;_UriId</td>
    <td>Contém identificador da entidade perante o SCAP</td>
  </tr>
  <tr>
    <td>*2 e *3</td>
    <td>SCAP_&lt;Fornecedor&gt;_TotpSecreyKey</td>
    <td>Contém secretKey para geração de TOTPs</td>
  </tr>
  <tr>
    <td>*2 e *3</td>
    <td>SCAP_&lt;Fornecedor&gt;_InfoFile</td>
    <td>Contém informação da conta do Fornecedor de Atributos</td>
  </tr>
  <tr>
    <td>*3</td>
    <td>SCAP_&lt;Fornecedor&gt;_CSR</td>
    <td>Contém CSR para pedir emissão de certificado</td>
  </tr>
</table>
