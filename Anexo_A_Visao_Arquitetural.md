# Anexo A – Visão arquitetural (referência)

Este anexo descreve uma visão arquitetural **suficiente para avaliação técnica** na consulta pública, sem detalhar segredos industriais.

## A.1 Objetivo e escopo

- apoiar o atendimento integrado (Saúde, Educação e Esportes) a pessoas neurodivergentes;
- permitir **compartilhamento controlado** de informações entre setores, com rastreabilidade;
- evitar dependência de integrações específicas não confirmadas: as integrações são **progressivas** e definidas após diagnóstico.

## A.2 Princípios técnicos

1) **Privacidade e segurança por padrão** (minimização, segmentação de acesso, auditoria)
2) **Interoperabilidade por APIs** (quando disponíveis), com alternativas por troca de arquivos quando necessário
3) **Dados sob governança do Município** (com regras claras de controlador/operador)
4) **Implantação em fases**, com piloto e evolução
5) **Observabilidade e rastreabilidade** (logs, auditoria, métricas)

## A.3 Componentes (visão lógica)

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

## A.4 Integrações (abordagem)

### A.4.1 Premissas

- Não se assume integração “pronta” com sistemas específicos.
- No diagnóstico, definir:
  - quais bases são fonte de verdade (cadastro, unidades, profissionais);
  - quais eventos precisam sincronização (encaminhamentos, status);
  - periodicidade (tempo real vs. lote);
  - mecanismos disponíveis (API, arquivo, barramento).

### A.4.2 Estratégia por fases

1) **Fase piloto**: mínima interoperabilidade para evitar retrabalho (cadastros essenciais e vínculos)
2) **Fase ampliação**: integrar fluxos críticos (encaminhamentos e retornos)
3) **Fase escala**: consolidar indicadores e governança em toda a rede

## A.5 Modelo de dados (mínimo)

Campos sugeridos como “mínimos” (a ajustar no co-desenho):

- Identificação da pessoa: nome, data de nascimento, identificadores municipais (quando existentes), contatos/responsáveis
- Vínculos: unidade de referência, escola/unidade, serviços de referência
- Plano integrado: objetivos, metas, periodicidade de revisão, responsáveis
- Encaminhamentos: origem, destino, motivo, status, prazos (quando aplicável), contrarreferência
- Auditoria: usuário, data/hora, ação, justificativa

## A.6 Segurança (visão de controles)

Controles recomendados (não exaustivo):

- autenticação forte (mecanismo a definir com o Município);
- autorização por perfil + contexto (necessidade de saber);
- criptografia em trânsito (TLS) e, quando aplicável, em repouso;
- segregação de ambientes (dev/homologação/produção);
- gestão de vulnerabilidades e atualização contínua;
- trilhas de auditoria e revisão periódica de acessos;
- política de retenção e descarte de dados.

## A.7 TRL (estimativa orientativa)

Como a consulta pública não detalha o cenário municipal nem o estado real de uma solução prévia do proponente, recomenda-se declarar TRL **como faixa**, sujeita a confirmação:

- **TRL 4–6**: quando o produto ainda depende de construção relevante e validações progressivas.
- **TRL 6–7**: quando existe MVP/protótipo validado em ambiente relevante, exigindo adaptação e integrações.

Critério prático: o TRL aumenta à medida que houver evidências de uso, testes e operação em condições similares às do Município.

