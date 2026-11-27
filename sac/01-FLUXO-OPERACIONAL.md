# 01 — FLUXO OPERACIONAL — FASE 1

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-10-16. Fonte: https://app.notion.com/p/dd7fafd5013b82c395d681a05c281940

---

# OBJETIVO

Aplicar a coleta e validação de materiais da Fase 1 às modalidades QWE e MOV do SAC, sob despacho do Bootstrap e controle de estados do Runtime.

# BOOT

A entrada e o despacho pertencem ao Bootstrap [00 — BOOTSTRAP / ATIVAÇÃO — FASE 0](./00-BOOTSTRAP-ATIVACAO.md). A ordem inicial e a rota de nova versão do mesmo produto pertencem ao BOOT SAC e aos handlers vigentes do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Esta página não inicia execução nem mantém sequência alternativa.

# EVENTO DE MATERIAL

Aplicar no Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md) os handlers MATERIALS\_WAIT\_PRODUCT, MATERIALS\_CONFIRM\_INFLUENCER e MATERIALS\_WAIT\_INFLUENCER; no loop, seguir também DURATION\_GATE conforme a rota vigente. Esses handlers definem coleta, duração, escolha da influencer, pendências e encaminhamento a CREATIVE\_PREP. Controles e recuperação seguem o ADAPTADOR\_DE\_INTERFACE; autorização de geração segue HARD BLOCK — FERRAMENTAS.

Validar materiais, evidências, produto e referência oficial da influencer pelos critérios MATERIALS\_OK, EVIDENCE\_OK, PRODUCT\_LOCK\_OK e INFLUENCER\_LOCK\_OK do Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md), inclusive a utilizabilidade de uma referência reutilizada. Esta página não redefine critérios nem cria aprovação ou transição paralela.

# CORREÇÃO DE DESVIO

Bloquear qualquer avanço que não siga esta rota. Registrar o comportamento observado e corrigir a causa na camada responsável, sem mascarar o desvio em outra etapa.
