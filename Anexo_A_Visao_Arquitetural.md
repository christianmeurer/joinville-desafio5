# Anexo A — Visão arquitetural (referência)

**Objetivo do anexo:** apresentar uma visão arquitetural **suficiente para avaliação técnica** na consulta pública, descrevendo como a plataforma digital habilita o **serviço operando** (atendimento integrado), sem expor detalhes proprietários.

**Como usar:** utilizar este anexo como referência para (i) discutir princípios e módulos mínimos do MVP do serviço, (ii) orientar o diagnóstico técnico (integrações/dados) e (iii) apoiar a definição de controles essenciais de segurança e privacidade.

**Relação com a proposta:** este anexo detalha o que é resumido na proposta em “Solução digital (habilitador do serviço)” e em “LGPD, privacidade e segurança” (ver [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:238)). Referências cruzadas: plano de testes e métricas em [`Anexo_B_Plano_Testes_Metricas.md`](Anexo_B_Plano_Testes_Metricas.md:1) e checklist LGPD/segurança em [`Anexo_E_Checklist_LGPD_Seguranca.md`](Anexo_E_Checklist_LGPD_Seguranca.md:1).

---

## Sumário

- [1. Objetivo e escopo](#1-objetivo-e-escopo)
- [2. Princípios técnicos](#2-princípios-técnicos)
- [3. Componentes (visão lógica)](#3-componentes-visão-lógica)
- [4. Integrações (abordagem)](#4-integrações-abordagem)
- [5. Modelo de dados (mínimo)](#5-modelo-de-dados-mínimo)
- [6. Segurança (visão de controles)](#6-segurança-visão-de-controles)
- [7. TRL (estimativa orientativa)](#7-trl-estimativa-orientativa)

---

## 1. Objetivo e escopo

Esta visão arquitetural foi elaborada para apoiar o **atendimento integrado** (Saúde, Educação e Esportes) a pessoas neurodivergentes, com foco em:

- habilitar o **compartilhamento controlado** de informações entre setores, com rastreabilidade;
- reduzir retrabalho e dependência da família como “ponte” (encaminhamentos com contrarreferência e status);
- manter o desenho compatível com a consulta pública: **não presumir integrações específicas** ainda não confirmadas.

> Nota de alinhamento: integrações e regras de dados são tratadas como **progressivas**, definidas após diagnóstico/co-desenho (conforme abordagem em fases descrita na proposta em [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:270)).

## 2. Princípios técnicos

1) **Privacidade e segurança por padrão**: minimização de dados, segmentação de acesso por contexto, trilha de auditoria.
2) **Interoperabilidade por APIs** quando disponíveis; alternativas por troca de arquivos/lote quando necessário.
3) **Dados sob governança do Município**: papéis claros de Controlador/Operador e regras de acesso auditáveis.
4) **Implantação em etapas**, começando pelo MVP do serviço, com piloto e evolução.
5) **Observabilidade e rastreabilidade**: logs, métricas e auditoria para suportar operação e governança.

## 3. Componentes (visão lógica)

| Componente | Função | Observações |
|---|---|---|
| Portal/Aplicação web | Interface para profissionais e gestão | perfis por secretaria e função |
| Módulo de cadastro e vinculação | cadastro mínimo, vínculos (responsáveis, unidades) | deduplicação assistida por regras |
| Registro integrado (por camadas) | registros estruturados e anexos | “visões” por setor e finalidade |
| Planos individualizados integrados | metas, responsáveis, revisões e histórico | alinhamento PDI/PTS (quando aplicável) |
| Encaminhamentos/contrarreferência | fluxo de encaminhar, aceitar, executar, retornar | estados e justificativas |
| Relatórios e painéis | relatórios operacionais e gerenciais | anonimização/agrupamento quando cabível |
| Gestão de consentimento e bases legais | registro de base legal/consentimento quando aplicável | versionamento e trilha |
| Auditoria e logs | quem acessou/alterou o quê e quando | retenção definida em política |
| Integração (API/ETL) | conectores e rotinas de sincronização | por fases e prioridades |

## 4. Integrações (abordagem)

### 4.1 Premissas

- Não se assume integração “pronta” com sistemas específicos.
- No diagnóstico, definir:
  - quais bases são fonte de verdade (cadastro, unidades, profissionais);
  - quais eventos precisam sincronização (encaminhamentos, status);
  - periodicidade (tempo real vs. lote);
  - mecanismos disponíveis (API, arquivo, barramento).

### 4.2 Estratégia por etapas

1) **Etapa inicial (MVP do serviço):** interoperabilidade mínima para evitar retrabalho (cadastros essenciais e vínculos).
2) **Etapa de ampliação:** integrar fluxos críticos (encaminhamentos e retornos/contrarreferência).
3) **Etapa de escala:** consolidar indicadores, governança e qualidade de dados em toda a rede.

## 5. Modelo de dados (mínimo)

Campos sugeridos como “mínimos” (a ajustar no co-desenho):

- Identificação da pessoa: nome, data de nascimento, identificadores municipais (quando existentes), contatos/responsáveis
- Vínculos: unidade de referência, escola/unidade, serviços de referência
- Plano integrado: objetivos, metas, periodicidade de revisão, responsáveis
- Encaminhamentos: origem, destino, motivo, status, prazos (quando aplicável), contrarreferência
- Auditoria: usuário, data/hora, ação, justificativa

## 6. Segurança (visão de controles)

Controles recomendados (não exaustivo):

- autenticação forte (mecanismo a definir com o Município);
- autorização por perfil + contexto (necessidade de saber);
- criptografia em trânsito (TLS) e, quando aplicável, em repouso;
- segregação de ambientes (dev/homologação/produção);
- gestão de vulnerabilidades e atualização contínua;
- trilhas de auditoria e revisão periódica de acessos;
- política de retenção e descarte de dados.

## 7. TRL (estimativa orientativa)

Como a consulta pública não detalha o cenário municipal (integrações, infraestrutura, inventário de dados) nem o estado real de uma base reutilizável do proponente, recomenda-se declarar TRL **como faixa**, sujeita a confirmação na descoberta.

- **TRL 4–6**: quando o produto ainda depende de construção relevante e validações progressivas.
- **TRL 6–7**: quando existe MVP/protótipo validado em ambiente relevante, exigindo adaptação e integrações.

Critério prático: o TRL aumenta à medida que houver evidências de uso, testes e operação em condições similares às do Município (ver a orientação de maturidade na proposta em [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:261)).

