# Anexo B — Plano de testes e métricas (piloto)

**Objetivo do anexo:** descrever uma abordagem prática para validar o **MVP do serviço** e seus habilitadores digitais, combinando testes em ambiente controlado e validação em operação real, com métricas e evidências recomendadas.

**Como usar:** (i) escolher quais fluxos serão testados primeiro, (ii) definir evidências mínimas para decisão de continuidade/escala e (iii) alinhar a coleta de métricas com a rotina de governança do piloto.

**Relação com a proposta:** este anexo complementa a seção de KPIs e avaliação de resultados (ver [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:330)) e se conecta às etapas de implantação (ver [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:270)). Referências cruzadas: premissas de segurança e arquitetura em [`Anexo_A_Visao_Arquitetural.md`](Anexo_A_Visao_Arquitetural.md:1) e checklist LGPD/segurança em [`Anexo_E_Checklist_LGPD_Seguranca.md`](Anexo_E_Checklist_LGPD_Seguranca.md:1).

---

## Sumário

- [1. Objetivo](#1-objetivo)
- [2. Estratégia de validação por etapa](#2-estratégia-de-validação-por-etapa)
- [3. Métricas sugeridas](#3-métricas-sugeridas)
- [4. Evidências mínimas recomendadas](#4-evidências-mínimas-recomendadas)

---

## 1. Objetivo

Este plano busca:

- validar que o serviço (processo + plataforma) sustenta os **fluxos críticos** do atendimento integrado;
- produzir evidências objetivas para decisão de continuidade e escala;
- reduzir riscos de segurança, privacidade (LGPD) e adesão das equipes.

## 2. Estratégia de validação por etapa

### 2.1 Ambiente controlado (pré-piloto)

**Entradas:** requisitos mínimos, fluxos priorizados, perfis de usuários, dados de teste.

**Testes recomendados (checklist):**

| Categoria | Exemplos de testes | Evidência |
|---|---|---|
| Funcionais | cadastro, plano integrado, encaminhamento/contrarreferência, relatórios | casos de teste e logs de execução |
| Integração | APIs/ETL, importação/exportação, consistência de chaves | relatórios de falhas e reconciliação |
| Segurança | autenticação, autorização, logs/auditoria, hardening | relatório de validação e correções |
| Privacidade | minimização, perfis de acesso, registro de base legal/consentimento quando aplicável | checklist LGPD preenchido |
| Usabilidade | tarefas críticas por perfil (tempo e taxa de erro) | roteiros, gravações/relatos, achados |
| Desempenho | cargas compatíveis com piloto, tempos de resposta | medições e limites acordados |

> Observação: recomenda-se que os testes funcionais e de usabilidade sejam alinhados aos fluxos do **service blueprint** e às etapas do serviço descritas na proposta, evitando “testar tela” sem contexto de operação (ver jornada/blueprint em [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:178)).

### 2.2 Ambiente real (piloto)

**Entradas:** unidades selecionadas, equipe de suporte, rotinas pactuadas.

**Rotina de acompanhamento:**

- acompanhamento semanal (ou periodicidade pactuada) com gestão e usuários-chave;
- triagem e correção de incidentes;
- ajustes de fluxo e treinamento complementar;
- auditorias amostrais de acesso e alterações.

## 3. Métricas sugeridas (sem metas numéricas fixas nesta fase)

As metas devem ser pactuadas no co-desenho. Abaixo, um catálogo de métricas (com forma de medição).

> Nota: os KPIs propostos no documento principal servem como “núcleo” do que deve ser medido; aqui, a intenção é detalhar medições e boas práticas de interpretação (ver KPIs na proposta em [`Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md`](Proposta_Consulta_Publica_Inovacao_Aberta_Joinville_Desafio_5.md:330)).

### 3.1 Adoção e uso

| Métrica | Como medir | Observações |
|---|---|---|
| Usuários ativos por perfil | acessos únicos por período | separar Saúde/Educação/Esportes |
| Unidades aderentes | unidades com uso recorrente | evitar “login único” como sinal falso |
| Fluxos concluídos | % de encaminhamentos com retorno | por tipo de encaminhamento |

### 3.2 Qualidade e continuidade do cuidado

| Métrica | Como medir | Observações |
|---|---|---|
| Planos integrados ativos | planos com revisão no período | refletir periodicidade acordada |
| Alinhamento de plano | registro de objetivos compartilhados | qualitativo + amostral |
| Completude de campos essenciais | % preenchimento em campos mínimos | por etapa do fluxo |

### 3.3 Eficiência operacional

| Métrica | Como medir | Observações |
|---|---|---|
| Tempo de ciclo do encaminhamento | criação → aceite → execução → retorno | estratificar por rede/unidade |
| Retrabalho | reabertura/correções por tipo | correlacionar com treinamento |
| Redução de “ponte” pela família | pesquisa/entrevista estruturada | comparar antes/depois no piloto |

### 3.4 Segurança, auditoria e conformidade

| Métrica | Como medir | Observações |
|---|---|---|
| Eventos de auditoria relevantes | acessos indevidos/alertas | por severidade |
| Tempo de resposta a incidente | abertura → contenção/correção | processo pactuado |
| Revisão de acessos | periodicidade e execução | evidência de governança |

## 4. Evidências mínimas recomendadas

- relatório de testes (ambiente controlado);
- registros de treinamento (por perfil) e materiais de apoio;
- relatório de operação assistida do piloto (incidentes, correções, evolução);
- relatório de métricas e lições aprendidas;
- recomendação de escala e requisitos de continuidade.

