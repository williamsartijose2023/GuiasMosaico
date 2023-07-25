---
layout: default
title: Reforce a segurança
parent: Publicação de API a consumir pela Administração Pública
nav_order: 2
---

# Reforce a segurança

A utilização de HTTPS vai proteger as comunicações com a API, preserva a privacidade do utilizador e garante a integridade dos dados. É importante que o serviço não permita que os dados sejam intercetados ou modificados por terceiros. Antes de qualquer operação certifique que a autenticação é efetuada com sucesso e que o sistema a aceder está autorizado a visualizar os dados. A autenticação baseada em token é altamente recomendada para qualquer API e um token deve expirar num prazo máximo de 24 horas. Habilite o Transport Layer Security (TLS) v1.2 ou versões subsequentes. Desenhe as APIs de forma a serem resistentes a ataques, tratando todos os dados enviados como não confiáveis validando-os antes de os processar. Ao expor as APIs, use uma camada de gateway para fornecer um ponto de controlo de segurança.

De forma a garantir a robustez do código fonte e de qualquer alteração futura, automatize testes de segurança, avalie o impacto da mudança e efetue testes antes de disponibilizar as alterações.

O acesso a APIs com dados confidenciais e/ou pessoais deve ficar registado para auditoria futura devem incluir-se nos logs o sistema e os identificadores individuais que tentam aceder à API juntamente com a data/hora. Deve monitorizar-se também todas as atividades suspeitas, incluindo padrões de acesso anormais, como requisições de elevadas cargas de dados, acessos em horários fora do comum, etc.
