# Anexo B – Plano de testes e métricas (piloto)

Este anexo detalha uma abordagem de testes **em ambiente controlado** e **em ambiente real**, com métricas e evidências recomendadas.

## B.1 Objetivo

- validar que a solução funciona para os fluxos críticos do atendimento integrado;
- produzir evidências para decisão de continuidade e escala;
- reduzir riscos de segurança, privacidade e adesão.

## B.2 Estratégia de validação por etapa

### B.2.1 Ambiente controlado (pré-piloto)

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

### B.2.2 Ambiente real (piloto)

**Entradas:** unidades selecionadas, equipe de suporte, rotinas pactuadas.

**Rotina de acompanhamento:**

- acompanhamento semanal (ou periodicidade pactuada) com gestão e usuários-chave;
- triagem e correção de incidentes;
- ajustes de fluxo e treinamento complementar;
- auditorias amostrais de acesso e alterações.

## B.3 Métricas sugeridas (sem metas numéricas fixas nesta fase)

As metas devem ser pactuadas no co-desenho. Abaixo, um catálogo de métricas (com forma de medição).

### B.3.1 Adoção e uso

| Métrica | Como medir | Observações |
|---|---|---|
| Usuários ativos por perfil | acessos únicos por período | separar Saúde/Educação/Esportes |
| Unidades aderentes | unidades com uso recorrente | evitar “login único” como sinal falso |
| Fluxos concluídos | % de encaminhamentos com retorno | por tipo de encaminhamento |

### B.3.2 Qualidade e continuidade do cuidado

| Métrica | Como medir | Observações |
|---|---|---|
| Planos integrados ativos | planos com revisão no período | refletir periodicidade acordada |
| Alinhamento de plano | registro de objetivos compartilhados | qualitativo + amostral |
| Completude de campos essenciais | % preenchimento em campos mínimos | por etapa do fluxo |

### B.3.3 Eficiência operacional

| Métrica | Como medir | Observações |
|---|---|---|
| Tempo de ciclo do encaminhamento | criação → aceite → execução → retorno | estratificar por rede/unidade |
| Retrabalho | reabertura/correções por tipo | correlacionar com treinamento |
| Redução de “ponte” pela família | pesquisa/entrevista estruturada | comparar antes/depois no piloto |

### B.3.4 Segurança, auditoria e conformidade

| Métrica | Como medir | Observações |
|---|---|---|
| Eventos de auditoria relevantes | acessos indevidos/alertas | por severidade |
| Tempo de resposta a incidente | abertura → contenção/correção | processo pactuado |
| Revisão de acessos | periodicidade e execução | evidência de governança |

## B.4 Evidências mínimas recomendadas

- relatório de testes (ambiente controlado);
- registros de treinamento (por perfil) e materiais de apoio;
- relatório de operação assistida do piloto (incidentes, correções, evolução);
- relatório de métricas e lições aprendidas;
- recomendação de escala e requisitos de continuidade.

