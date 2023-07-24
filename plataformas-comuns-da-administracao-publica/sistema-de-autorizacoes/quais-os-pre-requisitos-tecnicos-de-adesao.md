---
layout: default
title: Quais os pré-requisitos técnicos de adesão?
parent: Sistema de Autorizações
nav_order: 1
---

# Quais os pré-requisitos técnicos de adesão?

As comunicações eletrónicas a realizar entre os sistemas de informação da Entidade Aderente e o Sistema de Autorizações, realizam-se através da Plataforma de Integração da iAP, pelo que os requisitos técnicos a verificar são os estabelecidos para a ligação a essa plataforma.

## Requisitos de ligação segura

A comunicação da informação é efetuada por pedido e com prévia autenticação, através de ligação segura a estabelecer entre os sistemas de informação da Entidade Aderente e a iAP. &#x20;

Atualmente existem dois modos de ligação possíveis: &#x20;

* VPN sobre Internet onde a segurança da informação é garantida via transmissão por canais cifrados e autenticação dos pacotes que circulam, garantindo a integridade e privacidade dos dados; &#x20;
* Circuito dedicado dispensando o acesso à Internet. Esta opção é mais onerosa, apenas adequada a situações particulares de ligação (ex: elevado volume de tráfego, a necessidade de garantia de qualidade de serviço). As entidades que optem por este modo de ligação, terão de suportar integralmente todos os custos supervenientes. &#x20;
* Acesso via PTT (Ponto de Troca de Tráfego) em que as Entidades Aderentes estabelecem uma ligação ao PTT onde a AMA também já possui ligações estabelecidas. Este é o formato preferencial por garantir maior segurança e redundância. Neste caso a Entidade Aderente deverá contactar a entidade gestora do PTT (por exemplo a eSPap) para o estabelecimento da conetividade. &#x20;

Deverão também ser fornecidos contactos dos elementos responsáveis, a nível de infraestrutura, para operações de configuração e manutenção da infraestrutura de comunicação.&#x20;

## Requisitos para a ligação VPN



Os requisitos necessários para a ligação VPN à Plataforma de Interoperabilidade são:&#x20;

* Acesso à internet, com largura de banda disponível suficiente para assegurar a ligação em boas condições de funcionamento; &#x20;
* Um endereço IP público, com conectividade para qualquer destino da Internet, para assegurar a criação do túnel IPSec; &#x20;
* Suporte de protocolos e funcionalidades no equipamento de estabelecimento da VPN, de acordo com:

| Phase 1 IKE                           | Phase 2 IPSec                |
| ------------------------------------- | ---------------------------- |
| Key Exchange Encryption: AES 256 bits | UDP encapsulation: Yes       |
| Data Integrity: SHA256                | Protocol: ESP                |
| Diffie-Hellman (DH) group 14          | IPSec Encryption: AES 256    |
| Tempo de vida: 86400 segundos         | Diffie-Hellman (DH) group 14 |
| Type: Main mode                       | PFS: Yes                     |
|                                       | Tempo de vida: 3600 segundos |

O equipamento deverá suportar o envio de keepalives de Dead Peer Detection e deverá ter a capacidade de manter e renegociar automaticamente as SA’s de IPSec, mesmo na ausência de tráfego. &#x20;

Os equipamentos deverão ainda ter capacidade para resolver os problemas de sobreposição de endereçamento que poderão existir entre os diversos clientes no acesso aos servidores da AMA (funcionalidade NAT – Network Address Translation).&#x20;

## Requisitos da plataforma tecnológica para ligação à iAP

A Plataforma de Integração funciona baseado em webservices, no modelo de comunicação através de SOAP e REST. &#x20;

As entidades devem ter estes modelos presentes e devem assegurar os seguintes requisitos nas suas arquiteturas:

### Webservice REST

* Webservice Rest com Json; &#x20;
* Método POST;&#x20;
* Implementação assíncrona (one-way); &#x20;
* Canal de transporte http ou https(preferencial); &#x20;
* Utilização opcional de autenticação Http Basic-Auth. &#x20;

### Webservice SOAP

* Representado via WSDL 1.1 (http://www.w3.org/TR/wsdl) &#x20;
* Binding Soap 1.1 ou 1.2; &#x20;
* XML document-style; &#x20;
* Implementação assíncrona (one-way); &#x20;
* Canal de transporte http ou https(preferencial); &#x20;
* Utilização opcional de autenticação http basic auth; &#x20;
* WS-Addressing v1.0 (http://www.w3.org/TR/ws-addr-core/), como forma de correlacionamento de mensagens em modelo de comunicação assíncrona; &#x20;

> ℹ️ Deve respeitar as recomendações WS-Interoperability Basic-Profile 1.1, disponíveis em [Interoperability Testing Tools 1.1](http://www.ws-i.org/deliverables/testingtools.html).

