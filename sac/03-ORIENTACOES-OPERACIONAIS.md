# 03 — ORIENTAÇÕES OPERACIONAIS — FASE 2

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-10-17. Fonte: https://app.notion.com/p/016fafd5013b8340abeb01b12bb8e210

---

# OBJETIVO

Aplicar o contrato de Creative Readiness e autorizar a imagem-base somente após todas as condições de <code>IMAGE_READY</code>. A capa pertence à Fase 4 e segue rota separada.

Fontes relacionadas: entrada e interface [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md); estados [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md); evidências/locks [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); audiovisual [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); textos/capa [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); fechamento [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).

# MATERIAIS NÃO AUTORIZAM GERAÇÃO

Após o recebimento dos materiais, entrar em <code>CREATIVE_PREP</code>. Não gerar imagem nesta etapa.

# EVIDÊNCIA

Não inventar valor, benefício, abertura ou atributo do produto. Se faltar dado necessário para sustentar NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO ou MENSAGEM\_CENTRAL, bloquear avanço e pedir somente a informação ou evidência faltante.

# LEITURA INTERNA ANTES DA ESTRATÉGIA

Depois de <code>EVIDENCE_OK=TRUE</code>, fixar <code>AUDIENCE_BASE = Mulher + Brasil + TikTok Shop</code>, construir <code>AUDIENCE_CONTEXT</code> somente com evidência real da execução, registrar <code>CONTEXT_READING</code> em <b>O QUE SABEMOS / O QUE FALTA / BARREIRA OU DESEJO RELEVANTE</b> e registrar <code>NEED_DIAGNOSIS</code> entre PERCEBER / DESEJAR / ENTENDER / CONFIRMAR. Essas etapas são internas, não criam persona e não recebem aprovação humana.

# ESTRATÉGIA ANTES DA ABERTURA

Depois de <code>AUDIENCE_CONTEXT_READY=TRUE</code>, <code>CONTEXT_READING_READY=TRUE</code> e <code>NEED_DIAGNOSIS_READY=TRUE</code>, concluir objetivo DESCOBERTA e mecanismo automaticamente e seguir para <code>CREATIVE_PACKAGE_PREP</code>. Apresentar exatamente três Pacotes Criativos A/B/C, cada um integrando mensagem central, abertura e conceito audiovisual coerentes com a evidência. A única escolha estratégica humana ocorre em <code>CREATIVE_PACKAGE_GATE</code>.

# CONDIÇÕES DE IMAGE\_READY

Aplicar a lista única do CONTRATO IMAGE\_READY no Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md), incluindo aprovação do Pacote Criativo e todos os termos vigentes. Revalidação e checkpoint são executados no Runtime; esta orientação não mantém outra lista.

# CHECKPOINT E FERRAMENTA

Antes de chamar <code>image_gen</code>, registrar o CHECKPOINT PRE-TOOL com todos os termos obrigatórios TRUE, <code>CONCEPT_SELECTED</code>, <code>CONCEPT_APPROVED=TRUE</code>, <code>CONCEPT_OK=TRUE</code> e <code>IMAGE_READY=TRUE</code>. Essa é a única autorização para gerar a imagem-base. Uma chamada iniciada por recebimento de material, evidência isolada, confirmação da influencer, reutilização, comentário, silêncio ou condição parcial é bloqueada.

# PRODUCT LOCK E INFLUENCER LOCK

Se o conceito exigir alteração não autorizada do produto ou da identidade da influencer, manter a geração bloqueada e corrigir o conceito antes de seguir.

# SAÍDA

Após IMAGE\_READY e checkpoint pré-ferramenta válidos, gerar a imagem-base. Resultado real exige IMAGE\_GATE com auditoria visual e decisão REFAZER/APROVAR pelo ADAPTADOR\_DE\_INTERFACE do Runtime. Aplicar as cores obrigatórias em NATIVE ou a degradação TEXT autorizada, sem loop por falha de interface. Preservar imagem, locks e gate pendente; não iniciar roteiro ou textos sem resposta humana válida do gate atual.

# FALHA DE FERRAMENTA

Se <code>image_gen</code> falhar ou não retornar imagem válida, permanecer bloqueado em <code>IMAGE_READY</code>, sem abrir <code>IMAGE_GATE</code>. Repetir somente quando a ferramenta estiver disponível, após revalidar todas as condições obrigatórias e registrar novo checkpoint.
