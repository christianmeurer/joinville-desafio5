# Anexo D – Matriz de riscos (tecnológicos, operacionais e regulatórios)

Este anexo apresenta riscos típicos para um projeto intersetorial com dados sensíveis, com mitigação sugerida.

## D.1 Matriz

| Categoria | Risco | Como se manifesta | Mitigação sugerida | Evidência/controle |
|---|---|---|---|---|
| Tecnológico | Integrações indisponíveis | ausência de APIs, dados inconsistentes | diagnóstico técnico; integração por fases; rotas alternativas (lote/arquivo) | plano de integração e reconciliação |
| Tecnológico | Qualidade e duplicidade de cadastros | registros divergentes por rede | regras mínimas, deduplicação assistida, governança de “fonte de verdade” | indicadores de qualidade e trilha de correção |
| Operacional | Baixa adesão das equipes | solução não entra na rotina | co-desenho; treinamento por perfil; simplificação de fluxos; champions por unidade | métricas de uso + plano de capacitação |
| Operacional | Sobrecarga de implantação | equipes sem tempo para piloto | implantação por ondas; apoio operacional; priorização do mínimo | cronograma realista + suporte |
| Regulatória/LGPD | Exposição indevida de dados | acesso além da necessidade | perfis, mínimo privilégio, logs, revisões de acesso, segregação | auditoria + revisão periódica |
| Regulatória/LAI | Confusão entre transparência e sigilo | pedido de acesso a info sensível | marcação objetiva do que é confidencial; justificativas; versão pública sempre que possível | seção de confidencialidade + modelo |
| Segurança | Incidentes (vazamento, credenciais) | ataque ou erro humano | hardening, autenticação forte, monitoramento, resposta a incidentes | plano de resposta + relatórios |
| Sustentabilidade | Descontinuidade pós-piloto | “projeto morre” ao fim | requisitos de continuidade, SLAs, documentação, plano de escala | plano de operação e evolução |
| Escopo | Crescimento descontrolado | tentativa de “resolver tudo” | MVP bem definido; critérios de aceite; gestão de mudanças | backlog priorizado |
| Stakeholders | Alinhamento institucional frágil | conflitos entre redes | comitê intersetorial; decisões registradas; metas compartilhadas | atas e governança |

## D.2 Classificação (qualitativa)

Nesta consulta, recomenda-se classificar risco por **Baixo/Médio/Alto** em probabilidade e impacto, com priorização na etapa de descoberta.

