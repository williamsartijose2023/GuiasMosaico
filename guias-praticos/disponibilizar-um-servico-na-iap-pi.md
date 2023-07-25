---
layout: default
title: Disponibilizar um serviço na iAP-PI
nav_order: 24
---

# Disponibilizar um serviço na iAP-PI

| Passo                                       | Entidade responsável | Descrição                                                                                                                                                                                                                                               |
| ------------------------------------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Selecionar o serviço que pretende consumir  | Entidade             | Escolha o serviço pretendido do [catálogo de serviços](https://www.iap.gov.pt/web/iap/plataforma-de-integracao) disponíveis na PI.                                                                                                                      |
| Pedido de adesão formal à AMA               | AMA                  | Preencha o [formulário de adesão](https://www.iap.gov.pt/web/iap/formulario-de-adesao?serviceId=3) a indicar o(s) serviço(s) a consumir, se possível uma estimativa do volume de invocações e o enquadramento legal para obter a informação pretendida. |
| Acordar protocolo entre entidades           | Entidade e AMA       | Acordar protocolo entre as partes envolvidas no pedido de autorização.                                                                                                                                                                                  |
| Pedir autorização à CNPD                    | Entidade e AMA       | Caso exista recolha ou transmissão de dados pessoais deverá ser efetuado um pedido de autorização à Comissão Nacional de Proteção de Dados (CNPD) para disponibilização dos dados à entidade consumidora.                                               |
| Criação de VPN                              | AMA                  | Estabelecimento da ligação à Plataforma de Interoperabilidade através de _Virtual Private Network_ (VPN) permanente (mais informação em Ligação VPN).                                                                                                   |
| Adaptar SI das entidades                    | Entidade aderente    | Adaptação dos sistemas de informação (SI) das entidades aderentes para integrar os dados do serviço.                                                                                                                                                    |
| Definir cenários de teste                   | Entidade e AMA       | Definição dos cenários de teste.                                                                                                                                                                                                                        |
| Desenvolver Serviço e disponibilizar WSDL   | Entidade             | Caso o serviço ainda não esteja disponível é necessário o seu desenvolvimento pela entidade fornecedora e a disponibilização do _Web Services Description Language_ (WSDL), ficheiro responsável pela descrição, métodos e operações do serviço.        |
| Aprovar WSDL                                | Entidade e AMA       | Aprovação dos WSDL.                                                                                                                                                                                                                                     |
| Instalar em Ambiente de Qualidade           | Entidade e AMA       | Instalação do serviço em ambiente de qualidade.                                                                                                                                                                                                         |
| Efetuar Testes Integrados                   | Entidade e AMA       | Testes integrados do serviço.                                                                                                                                                                                                                           |
| Instalar em Produção                        | Entidade e AMA       | Instalação do serviço em produção.                                                                                                                                                                                                                      |
| Assinar protocolo                           | Entidade e AMA       | Assinatura do protocolo acordado entre as partes.                                                                                                                                                                                                       |
| Entrar em Produção                          | Entidade e AMA       | Entrada em produção do serviço após validação de todos os requisitos técnicos, jurídicos e de privacidade.                                                                                                                                              |