# Anexo E – Checklist LGPD e segurança da informação

Checklist de referência para orientar co-desenho e implantação, alinhado às exigências de LGPD e boas práticas de segurança.

## E.1 Papéis e governança

- [ ] definir Controlador (Município) e Operador(es) (fornecedor(es))
- [ ] mapear suboperadores (quando houver) e responsabilidades
- [ ] definir responsáveis internos (DPO/Encarregado, segurança, gestores das áreas)
- [ ] aprovar política de acessos (perfis e mínimo privilégio)

## E.2 Base legal e finalidade

- [ ] listar finalidades do tratamento por fluxo (cadastro, encaminhamento, plano integrado)
- [ ] registrar base legal aplicável por finalidade (incluindo hipóteses em que consentimento **não** é base adequada)
- [ ] definir quando e como registrar consentimento (apenas quando pertinente)

## E.3 Minimização e necessidade

- [ ] definir conjunto mínimo de dados por perfil/setor
- [ ] implementar mascaramento/ocultação de campos conforme perfil
- [ ] impedir exportações massivas sem justificativa e autorização

## E.4 Direitos do titular e transparência

- [ ] definir fluxos de atendimento ao titular (quando aplicável)
- [ ] definir registros e prazos de resposta
- [ ] garantir rastreabilidade (quem acessou, quando, por quê)

## E.5 Segurança técnica

- [ ] autenticação e gestão de identidade (mecanismo a definir com o Município)
- [ ] autorização por perfil + contexto
- [ ] logs e auditoria com retenção definida
- [ ] criptografia em trânsito (TLS) e, quando aplicável, em repouso
- [ ] segregação de ambientes e backups
- [ ] monitoramento e resposta a incidentes

## E.6 Segurança operacional

- [ ] treinamento de usuários e termos de uso
- [ ] procedimento de criação/remoção de acessos (joiner/mover/leaver)
- [ ] revisão periódica de permissões

## E.7 Documentação e evidências

- [ ] registro de decisões de privacidade e segurança
- [ ] inventário de dados e dicionário mínimo
- [ ] relatório de testes e correções

