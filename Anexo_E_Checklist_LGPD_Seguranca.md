# Anexo E — Checklist LGPD e segurança da informação

**Objetivo do anexo:** fornecer um checklist objetivo para apoiar o co-desenho e a implantação do serviço, garantindo aderência a LGPD e boas práticas de segurança da informação, com foco em operação real (acessos, auditoria e governança).

**Como usar:** (i) revisar na Etapa 0/1 (governança e descoberta) para definir decisões e responsáveis, (ii) usar como critério de aceite do MVP do serviço e (iii) manter como rotina de auditoria/revisão periódica durante o piloto.

**Relação com a proposta:** este checklist complementa a seção de LGPD, privacidade e segurança (ver [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:389)) e se conecta à arquitetura e controles sugeridos em [`Anexo_A_Visao_Arquitetural.md`](Anexo_A_Visao_Arquitetural.md:60). Referências cruzadas: testes/evidências de segurança em [`Anexo_B_Plano_Testes_Metricas.md`](Anexo_B_Plano_Testes_Metricas.md:13) e riscos regulatórios em [`Anexo_D_Matriz_Riscos.md`](Anexo_D_Matriz_Riscos.md:1).

---

## Sumário

- [1. Papéis e governança](#1-papéis-e-governança)
- [2. Base legal e finalidade](#2-base-legal-e-finalidade)
- [3. Minimização e necessidade](#3-minimização-e-necessidade)
- [4. Direitos do titular e transparência](#4-direitos-do-titular-e-transparência)
- [5. Segurança técnica](#5-segurança-técnica)
- [6. Segurança operacional](#6-segurança-operacional)
- [7. Documentação e evidências](#7-documentação-e-evidências)

---

## 1. Papéis e governança

- [ ] definir Controlador (Município) e Operador(es) (fornecedor(es))
- [ ] mapear suboperadores (quando houver) e responsabilidades
- [ ] definir responsáveis internos (DPO/Encarregado, segurança, gestores das áreas)
- [ ] aprovar política de acessos (perfis e mínimo privilégio)

## 2. Base legal e finalidade

- [ ] listar finalidades do tratamento por fluxo (cadastro, encaminhamento, plano integrado)
- [ ] registrar base legal aplicável por finalidade (incluindo hipóteses em que consentimento **não** é base adequada)
- [ ] definir quando e como registrar consentimento (apenas quando pertinente)

## 3. Minimização e necessidade

- [ ] definir conjunto mínimo de dados por perfil/setor
- [ ] implementar mascaramento/ocultação de campos conforme perfil
- [ ] impedir exportações massivas sem justificativa e autorização

## 4. Direitos do titular e transparência

- [ ] definir fluxos de atendimento ao titular (quando aplicável)
- [ ] definir registros e prazos de resposta
- [ ] garantir rastreabilidade (quem acessou, quando, por quê)

## 5. Segurança técnica

- [ ] autenticação e gestão de identidade (mecanismo a definir com o Município)
- [ ] autorização por perfil + contexto
- [ ] logs e auditoria com retenção definida
- [ ] criptografia em trânsito (TLS) e, quando aplicável, em repouso
- [ ] segregação de ambientes e backups
- [ ] monitoramento e resposta a incidentes

## 6. Segurança operacional

- [ ] treinamento de usuários e termos de uso
- [ ] procedimento de criação/remoção de acessos (joiner/mover/leaver)
- [ ] revisão periódica de permissões

## 7. Documentação e evidências

- [ ] registro de decisões de privacidade e segurança
- [ ] inventário de dados e dicionário mínimo
- [ ] relatório de testes e correções

> Boa prática: anexar evidências simples e auditáveis (atas de decisões, prints de configuração de perfis, relatórios de logs/auditoria, resultados de testes) em vez de produzir documentos longos sem uso operacional.

