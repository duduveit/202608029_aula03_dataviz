# 📋 Documento de Requisitos — Dashboard PBL (Data Visualization)

**Projeto:** Dashboard do Processo de Aprendizagem Baseada em Projetos (PBL)  
**Cliente / Stakeholder:** Professor Orientador do Instituto Ápice  
**Contexto Operacional:** Módulo de 10 semanas com 5 Sprints quinzenais (entregas às sextas-feiras até 23h59)  

---

## 1. Visão Geral e Problema de Negócio

* **Papel do Cliente:** O professor orientador acompanha múltiplos grupos em paralelo, sem presenciar todas as reuniões de trabalho.
* **Necessidade Central:** Identificar, a cada sprint quinzenal, **onde e como intervir precocemente** para corrigir gargalos, desequilíbrios de esforço ou falhas na colaboração antes do início do próximo ciclo.
* **Objeto de Observação:** O **processo de aprendizagem do grupo**. As ferramentas (GitLab, Kanban) servem apenas como superfícies que registram o rastro de trabalho.

---

## 2. Pilares de Requisitos (Elicitação)

### A. Contribuição (Conteúdo Válido e Efetivo)
* **REQ-01 — Detecção de Refação e Esforço Redundante:** Identificar quando os commits ou conteúdos entregues por um integrante são constantemente sobrepostos, descartados ou reescritos por outro membro do grupo.
* **REQ-02 — Identificação de Atuação Periférica:** Detectar discentes que realizam exclusivamente tarefas periféricas (ex.: formatação, revisão ortográfica, ajuste de sumário) sem se envolver nas atividades centrais/técnicas do projeto.
* **REQ-03 — Rastreabilidade de Evidências no Kanban:** Exigir que cartões marcados como concluídos no quadro Kanban possuam links/evidências verificáveis internas (commits assinados, código em repositório) ou externas (planilhas, apresentações, Colab).

### B. Colaboração (Ritmo e Dinâmica de Trabalho)
* **REQ-04 — Análise de Cadência de Trabalho:** Monitorar se o trabalho é distribuído continuamente ao longo das duas semanas de sprint ou se há concentração excessiva de esforço na véspera da entrega (quarta a sexta-feira).
* **REQ-05 — Coerência Quadro vs. Repositório:** Verificar a movimentação de cartões e comparar se os cartões concluídos condizem com as entregas efetivamente registradas no versionamento de código do período.

### C. Aprendizagem (Visão Holística e Especialista)
* **REQ-06 — Diagnóstico de Retenção de Conhecimento:** Cruzar a dinâmica do grupo com as avaliações individuais dos professores especialistas para diferenciar a compreensão real do projeto do mero uso mecânico de IA generativa ou reprodução de conteúdo.

---

## 3. Restrições Inegociáveis

1. **Autoridade Humana:** O dashboard é um instrumento de suporte à decisão. Ele gera evidências e provocações pedagógicas, **jamais atribuindo notas, rankings, vereditos ou julgamentos automáticos**.
2. **Unidade de Análise:** A saída principal é sempre o **grupo**. A análise individual serve exclusivamente para avaliar a distribuição interna de esforço do grupo.
3. **Fuga da "Armadilha do Pedido Literal":** Evitar indicadores isolados ou quantitativos puramente superficiais (ex.: total de commits por aluno).
4. **Confidencialidade:** Respeitar a pseudonimização dos dados públicos e o acesso restrito aos dados identificados no ambiente Metabase.
5. **Declaração de Lacunas:** Reconhecer que atividades não registradas digitalmente (discussões presenciais, *pair programming* sem commit conjunto, reuniões fora do ambiente) constituem limitações da fonte de dados e não ausência de trabalho.

---

## 4. Matriz de Decisão e Evidências

| Pergunta de Decisão do Orientador | Evidência Rastreável nos Dados | Critério de Aceite |
| :--- | :--- | :--- |
| O trabalho do grupo foi distribuído de forma equilibrada? | Volume e autoria de commits e participação em *Merge Requests* por integrante/sprint. | O painel exibe a curva de contribuição relativa dos membros dentro do grupo sem ranqueá-los. |
| O grupo manteve cadência contínua ou trabalhou na véspera? | Carimbo de data/hora de commits e movimentação no Kanban ao longo dos dias da Sprint. | Gráfico temporal destacando o fluxo de atividades por dia da semana contra a data limite. |
| O quadro Kanban reflete o código entregue? | Comparativo entre cartões em coluna de concluído e entregas no repositório. | Sinalização gráfica de cartões finalizados sem entregas associadas no mesmo período. |
| As entregas de código passaram por revisão efetiva? | *Merge Requests* aprovados, tempo de abertura/fechamento e contagem de comentários de revisão. | Exibição do tempo médio de integração e identificação dos revisores dentro do grupo. |
