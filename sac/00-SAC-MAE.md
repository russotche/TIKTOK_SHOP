# SAC MÃE

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-10-17. Fonte: https://app.notion.com/p/3eefafd5013b81c7b34ce27c7adf41f5

---

## MAPA DE AUTORIDADES POR ASSUNTO — GRUPOS 2 E 7

Mapa de responsabilidades do SAC. Cada assunto tem uma fonte responsável:

- <b>Entrada SAC:</b> [00 — BOOTSTRAP / ATIVAÇÃO — FASE 0](./00-BOOTSTRAP-ATIVACAO.md).
- <b>Estados e transições:</b> [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).
- <b>Evidências e locks:</b> [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md).
- <b>Roteiro:</b> [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md).
- <b>Elementos de Texto e capa:</b> [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md).
- <b>Contadores e encerramento:</b> [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).
- <b>Interface e primeiro despacho do Runtime:</b> [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md).

As demais páginas referenciam essas autoridades e não redefinem o assunto. A SAC MÃE conserva este mapa e a visão geral; Fluxo Integrado, Padrão do Roteiro e páginas de apoio remetem à fonte responsável. Aplicar somente os contratos vigentes de QWE e MOV.

## GRUPO 7 — GOVERNANÇA DA ARQUITETURA (16/10/2026)

<b>ESTADO:</b> governança aprovada e documentada; validação prática permanece na P08. Este grupo organiza manutenção e evidência, sem criar gate humano nem alterar a sequência SAC.

### Fontes responsáveis e vigência

Aplicar o MAPA DE AUTORIDADES POR ASSUNTO desta página. Cada regra operacional possui uma seção responsável; os consumidores usam referência à fonte, preservando apenas as pré-condições e transições que lhes cabem. A manutenção atualiza a regra responsável e suas referências, em vez de acrescentar outra cópia da mesma instrução.

Aprovação nova altera somente seu assunto e escopo. Uma correção mantém produto, modalidade, duração, estratégia, artefatos e gates já aprovados que não sejam afetados. Mudança material de artefato segue seu gate existente. Conflito real entre fontes exige verificar a decisão vigente e corrigir a menor dependência; data mais recente, isoladamente, não autoriza mudar outro contrato.

Cada fonte responsável mantém somente a regra vigente do seu assunto.

### Controle de tamanho

Teto inicial de manutenção por página:

| Fonte | Teto em caracteres |
| --- | --- |
| [SAC MÃE](./00-SAC-MAE.md) | 45000 |
| [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md) | 85000 |
| [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md) | 34000 |
| [03 — ORIENTAÇÕES OPERACIONAIS — FASE 2](./03-ORIENTACOES-OPERACIONAIS.md) | 5000 |
| [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md) | 55000 |
| [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md) | 32000 |
| [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md) | 13000 |
| [00 — BOOTSTRAP / ATIVAÇÃO — FASE 0](./00-BOOTSTRAP-ATIVACAO.md) | 9000 |
| [01 — FLUXO OPERACIONAL — FASE 1](./01-FLUXO-OPERACIONAL.md) | 2000 |
| [05 — PADRÃO OPERACIONAL DO ROTEIRO — FASE 3](./05-PADRAO-OPERACIONAL-ROTEIRO.md) | 2500 |
| [08 — FLUXO OPERACIONAL INTEGRADO — V2](./08-FLUXO-OPERACIONAL-INTEGRADO.md) | 4500 |
| [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md) | 8000 |
| — | 45000 |

<b>Medição reproduzível:</b> contar pontos de código Unicode do conteúdo Markdown devolvido por fetch, sem o envelope page/properties/ancestor-path; normalizar CRLF para LF, remover espaços/quebras apenas nas extremidades e representar menções de página como tags autocontidas com a mesma URL, sem o título resolvido. Contar o restante integralmente. O teto limita o documento; não é limite de prompt de vídeo.

Antes e depois de uma alteração, medir as páginas afetadas. Dentro do teto e sem cópia operacional concorrente: PASS de tamanho. Acima do teto: FAIL de manutenção documental; condensar duplicações ou separar conteúdo por responsabilidade dentro da árvore SAC, preservando regras válidas e páginas filhas. Não aumentar o teto silenciosamente.

Esse controle é de manutenção, não uma nova condição de IMAGE\_READY, de aprovação humana ou de encerramento. Nenhum artefato aprovado é invalidado apenas pelo tamanho de um documento.

### Rastreabilidade das alterações

Os Engines mantêm seus contratos atuais; a SAC MÃE conserva apenas o mapa de responsabilidades, os limites e o estado vigente.

A releitura compara o resultado com a alteração prevista e verifica links de autoridade, gates, contratos QWE/MOV, locks, regras de persistência, páginas filhas e fontes não afetadas. Uma divergência exige correção e nova releitura do trecho afetado. A escrita só é declarada confirmada após retorno verificável.

### PASS/FAIL e conclusão

<b>DOCUMENTAL PASS:</b> alteração autorizada gravada e relida, conteúdo previsto confirmado, dependências resolvidas, preservações conferidas e páginas dentro do teto registrado. <b>DOCUMENTAL FAIL:</b> qualquer divergência, dependência quebrada ou manutenção fora do teto. Sem leitura ou evidência suficiente, registrar PENDENTE.

<b>PRÁTICO PASS:</b> execução observada satisfaz o caso da matriz do Runtime, com evidência do estado, controle, evento, resultado e próxima ação. <b>PRÁTICO FAIL:</b> resultado observado diverge do esperado. Sem execução observada, registrar PENDENTE.

A matriz única de casos por gate está em [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md), seção MATRIZ DE TESTES POR GATE — GRUPO 7. Os critérios consultam os contratos atuais de cada autoridade; não os substituem. PASS de teste e autoauditoria não aprovam artefato nem resolvem gate humano.

A governança fecha documentalmente quando os quatro componentes deste grupo — autoridades, tamanho, rastreabilidade e matriz — estiverem gravados e conferidos. O fechamento documental não encerra a P08 nem comprova renderização real de botões.

## ENCERRAMENTO ENXUTO — CORREÇÃO APROVADA (16/10/2026)

Decisão aprovada preservada. O contrato completo de encerramento, tentativa única de atualização, idempotência e sincronização pendente pertence ao Lifecycle [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md), seção ARCHIVE\_WRITE → EXECUTION\_DONE. O Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md) aplica esse contrato em seus handlers de fechamento e apresenta a conclusão/loop pelo adaptador, sem narrar rotina administrativa. Esta seção não mantém outro algoritmo.

## CORREÇÃO CANÔNICA P07 — INTERFACE LIMPA CONSOLIDADA (15/10/2026)

Regra operacional vigente no SAC, QWE e MOV.

<b>INTERFACE:</b> aplicar o contrato de saída, os rótulos oficiais, os controles funcionais e as preferências visuais definidos no Runtime: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

<b>CRIAÇÃO:</b> aplicar a composição dos pacotes da seção P03 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md) e a exclusividade da escolha/derivação definida em P01 e GATE CRIATIVO UNIFICADO do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

<b>FLUXO PRESERVADO:</b> não acrescentar gate e não pular seleção de modalidade, materiais, duração, aprovação criativa, IMAGE\_READY, IMAGE\_GATE, SCRIPT\_GATE, TEXT\_ELEMENTS\_GATE, COVER\_GATE nem demais gates reais previstos. PRODUCT\_LOCK, INFLUENCER\_LOCK e evidências permanecem obrigatórios. QWE pode utilizar fala; MOV permanece sem fala. Confirmar efetivamente cada ação antes de anunciar conclusão.

<b>AUDITORIA:</b> validar a interface e o fluxo pelos contratos vigentes; testes de ponta a ponta permanecem uma verificação prática separada.

## P06 — CONTROLE VISUAL DO IMAGE\_READY (15/10/2026)

Decisão aprovada preservada. Aplicar a verificação de coerência visual e os requisitos IMAGE\_READY da seção P06 e do CONTRATO IMAGE\_READY no Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md). O Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md) controla a barreira e a chamada de ferramenta; a direção audiovisual está no Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md).

## CORREÇÃO CANÔNICA P05 — MOV: BENEFÍCIO VISUAL SEM FALA (15/10/2026)

Decisão aprovada preservada. A comunicação de benefício por ações visuais, sem fala, segue P05 e MOV V2 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). Evidências e fidelidade seguem o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); o fluxo é controlado pelo Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## CORREÇÃO CANÔNICA P04 — DIREÇÃO DE ENQUADRAMENTO DA IMAGEM-BASE (15/10/2026)

Decisão aprovada preservada. A direção de enquadramento e continuidade imagem → vídeo está na seção P04 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md), respeitando o contrato específico da modalidade. A autorização de IMAGE\_READY segue o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); estados e interface seguem o Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## CORREÇÃO CANÔNICA P03 — DIFERENCIAÇÃO COMERCIAL DOS PACOTES A/B/C (15/10/2026)

Decisão aprovada preservada. A composição e diferenciação comercial/audiovisual dos pacotes A/B/C estão na seção P03 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). A emissão, escolha humana e derivação dos estados seguem o Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md); evidências e locks seguem o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md).

## CORREÇÃO CANÔNICA P02 — DESEJO E BENEFÍCIO PERCEBIDO (15/10/2026)

Decisão aprovada preservada. Aplicar a análise factual de desejo e benefício percebido da seção P02 no Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md). Sua tradução audiovisual segue os contratos P03–P05 e MOV V2 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); estados e escolhas pertencem ao Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## CORREÇÃO CANÔNICA P01 — EXCLUSIVIDADE DO PACOTE CRIATIVO (15/10/2026)

A exclusividade de <code>CREATIVE_PACKAGE_GATE</code> e os estados derivados são definidos no Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Não redefinir estados nesta cópia.

## RÓTULOS OFICIAIS DO MODALITY\_GATE

Consultar os rótulos oficiais do MODALITY\_GATE na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## INTERFACE LIMPA — REGRA CANÔNICA DE SAÍDA

Consultar o contrato de interface limpa e a exposição das informações necessárias à decisão na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## PADRÃO VISUAL ATUAL — ESCOLHA DA MODALIDADE

Consultar a apresentação da escolha de modalidade e suas preferências visuais na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## AUTOAUDITORIA OBRIGATÓRIA DE BOTÕES

Consultar a autoauditoria dos controles funcionais na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## REGRA CANÔNICA — CONTROLES COLORIDOS UNIVERSAIS (14/10/2026)

Consultar as cores obrigatórias dos botões e a alternativa textual autorizada e os critérios de validade dos controles na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## REGRA CANÔNICA — GATE CRIATIVO UNIFICADO

Aplicar o GATE CRIATIVO UNIFICADO e o CONTRATO DE STATE MACHINE ATIVA do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). A construção dos pacotes segue P03 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); <code>IMAGE_READY</code> segue o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md).

## REGRA CANÔNICA — MECANISMO CRIATIVO AUTOMÁTICO

Os estados automáticos do mecanismo pertencem ao Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Os critérios de seleção e a tradução audiovisual estão no Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); evidências e locks seguem o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md).

## REGRA CANÔNICA — SAC ENXUTO / AIDA + DESCOBERTA

O diagnóstico/AIDA flexível, NEXT\_ADVANCE interno, objetivo DESCOBERTA automático, estados derivados, rastreabilidade humana e sequência vigente pertencem ao Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Aplicar os critérios factuais do Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md) e os contratos audiovisuais do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). A descrição AIDA do QWE e os três itens MOV seguem o Text Engine [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md).

## ARQUITETURA SAC

SAC é o sistema-mãe; QWE e MOV são modalidades irmãs. Aplicar os contratos vigentes: audiovisual no Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); Elementos de Texto e capa no Text Engine [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); evidências e locks no Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); estados e loop no Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). MOV permanece sem fala.

# STATUS

<b>V2 — FLUXO OPERACIONAL: ELEMENTOS DE TEXTO → CAPA → APROVAÇÃO DA CAPA.</b>

A V1 não é runtime desta versão e não possui autoridade operacional aqui.

# PRINCÍPIO DE MANUTENÇÃO OPERACIONAL

A V2 possui fluxo operacional completo. Desvios observados são tratados sem remendo pela sequência:

<b>EVIDÊNCIA → CAMADA RESPONSÁVEL → CAUSA COMPROVADA → CORREÇÃO ESTRUTURAL → CONFERÊNCIA DA ALTERAÇÃO.</b>

As regras abaixo orientam a execução ativa; os gates do Runtime controlam as aprovações de cada artefato.

# SISTEMA E LEI FUNDAMENTAL

<b>SAC — Sistema de Avanço de Compra</b>

> “O SAC não presume que a mulher já quer comprar. Ele identifica o que ela precisa perceber, desejar, entender ou confirmar sobre o produto e cria um vídeo para fazê-la avançar um passo em direção à compra.”

Tudo que for criado nesta versão deve nascer desta lei.

## ARQUITETURA CANÔNICA APROVADA — SAC / QWE / MOV (12/10/2026)

<b>SAC é o sistema-mãe. QWE e MOV são duas MODALIDADES/TIPOS DE VÍDEO IRMÃOS, não hierarquizados entre si.</b> O MOV não é subtipo, derivado nem variante do QWE. QWE designa a modalidade tradicional com seu contrato audiovisual e textual próprio; MOV designa a modalidade de observação visual silenciosa com contrato audiovisual e textual próprio.

O núcleo comum SAC possui leitura de audiência baseada em evidência, NEXT\_ADVANCE, objetivo, mecanismo, mensagem central, abertura, conceito, gates humanos, fidelidade à variante anunciada (PRODUCT\_LISTING\_MATCH), Product Lock, Influencer Lock, segurança e rastreabilidade. A modalidade selecionada define como esses objetivos são executados em imagem, roteiro, áudio, ações, Elementos de Texto e capa, respeitando as regras comuns.

<b>ROTEAMENTO CANÔNICO:</b> <code>SAC → MODALITY_GATE → QWE | MOV → materiais → DURATION_GATE → influencer → CREATIVE_PREP</code>. Registrar somente <code>VIDEO_FORMAT=QWE</code> ou <code>VIDEO_FORMAT=MOV</code>, sem presumir escolha. A ativação canônica é <code>SAC</code>, conforme Bootstrap/Runtime.

<b>Contratos exclusivos:</b> o audiovisual de cada modalidade segue o Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); as peças de publicação e a capa seguem o CONTRATO ATIVO POR MODALIDADE do Text Engine [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md). QWE e MOV mantêm contratos próprios; a visão geral não replica seus limites e formatos.

QWE e MOV são modalidades independentes sob o sistema-mãe SAC.

## REGRA OPERACIONAL DO SAC — UM CRIATIVO, UM AVANÇO PRINCIPAL

Cada criativo deve provocar apenas um avanço principal. Antes dos gates humanos, o SAC executa uma leitura interna obrigatória: <code>AUDIENCE_BASE = Mulher + Brasil + TikTok Shop</code> → <code>AUDIENCE_CONTEXT</code> baseado somente em evidência → <code>CONTEXT_READING</code> com O QUE SABEMOS / O QUE FALTA / BARREIRA OU DESEJO RELEVANTE → <code>NEED_DIAGNOSIS</code> entre PERCEBER / DESEJAR / ENTENDER / CONFIRMAR. Essa leitura não cria persona e não toma decisão pelo usuário.

Depois dessa leitura, aplicar a preparação estratégica automática do Runtime: AIDA/NEXT\_ADVANCE internos, objetivo DESCOBERTA e mecanismo automático. O único gate humano estratégico é CREATIVE\_PACKAGE\_GATE; mensagem central, abertura e conceito são derivados da mesma opção aprovada. Não solicitar decisões humanas separadas para esses componentes.

O SAC propõe e justifica três Pacotes Criativos completos; o usuário escolhe um em <code>CREATIVE_PACKAGE_GATE</code>. Mensagem, abertura e conceito derivam dessa mesma opção; diagnóstico, objetivo e mecanismo permanecem automáticos.

A <b>MENSAGEM\_CENTRAL</b> é a referência obrigatória de toda a execução. <b>Abertura, conceito, imagem, roteiro, ELEMENTOS DE TEXTO e capa</b> devem expressar o mesmo avanço principal, sem introduzir novo ângulo, nova promessa ou nova decisão.

A nomenclatura canônica desta versão é <b>ELEMENTOS DE TEXTO</b>.

# FASE 0 — ATIVAÇÃO

Entrada vigente: SAC → Bootstrap [00 — BOOTSTRAP / ATIVAÇÃO — FASE 0](./00-BOOTSTRAP-ATIVACAO.md) → núcleo de entrada do Runtime [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md). A SAC MÃE não integra a cadeia de leitura obrigatória antes da escolha de modalidade. O Registro Ativo guarda checkpoints; não substitui regras.

# FASE 1 — CONTRATO MÍNIMO

Consultar a Fase 1 [01 — FLUXO OPERACIONAL — FASE 1](./01-FLUXO-OPERACIONAL.md) e os handlers MATERIALS\_WAIT\_PRODUCT, MATERIALS\_CONFIRM\_INFLUENCER e MATERIALS\_WAIT\_INFLUENCER do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). O Runtime define ordem, duração, decisão da influencer, pendências e bloqueio de geração; o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md) define critérios de materiais, evidência e locks. Não manter um contrato de coleta paralelo nesta visão geral.

# INVARIANTE DE SEGURANÇA DA FASE 1

Consultar a Fase 1 [01 — FLUXO OPERACIONAL — FASE 1](./01-FLUXO-OPERACIONAL.md) e os handlers MATERIALS\_WAIT\_PRODUCT, MATERIALS\_CONFIRM\_INFLUENCER e MATERIALS\_WAIT\_INFLUENCER do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). O Runtime define ordem, duração, decisão da influencer, pendências e bloqueio de geração; o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md) define critérios de materiais, evidência e locks. Não manter um contrato de coleta paralelo nesta visão geral.

# SAÍDA OBRIGATÓRIA APÓS MATERIAIS INICIAIS

Consultar a Fase 1 [01 — FLUXO OPERACIONAL — FASE 1](./01-FLUXO-OPERACIONAL.md) e os handlers MATERIALS\_WAIT\_PRODUCT, MATERIALS\_CONFIRM\_INFLUENCER e MATERIALS\_WAIT\_INFLUENCER do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). O Runtime define ordem, duração, decisão da influencer, pendências e bloqueio de geração; o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md) define critérios de materiais, evidência e locks. Não manter um contrato de coleta paralelo nesta visão geral.

# REGRA OPERACIONAL DA FASE 1

Consultar a Fase 1 [01 — FLUXO OPERACIONAL — FASE 1](./01-FLUXO-OPERACIONAL.md) e os handlers MATERIALS\_WAIT\_PRODUCT, MATERIALS\_CONFIRM\_INFLUENCER e MATERIALS\_WAIT\_INFLUENCER do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). O Runtime define ordem, duração, decisão da influencer, pendências e bloqueio de geração; o Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md) define critérios de materiais, evidência e locks. Não manter um contrato de coleta paralelo nesta visão geral.

# FASE 2 — CREATIVE READINESS / TOOL GATE

As condições de geração da imagem-base pertencem ao CONTRATO IMAGE\_READY e P06 do Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); sua aplicação, checkpoint pré-ferramenta e transição para aprovação pertencem ao Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). A capa tem rota própria posterior à aprovação dos Elementos de Texto da modalidade vigente, conforme o Text Engine [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md) e os handlers de capa do Runtime. Esta visão geral não redefine quantidade de peças, condições técnicas ou transições.

- 📄 [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md)

- 📄 [01 — FLUXO OPERACIONAL — FASE 1](./01-FLUXO-OPERACIONAL.md)

- 📄 [00 — BOOTSTRAP / ATIVAÇÃO — FASE 0](./00-BOOTSTRAP-ATIVACAO.md)

- 📄 [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md)

- 📄 [03 — ORIENTAÇÕES OPERACIONAIS — FASE 2](./03-ORIENTACOES-OPERACIONAIS.md)

- 📄 [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md)

- 📄 [05 — PADRÃO OPERACIONAL DO ROTEIRO — FASE 3](./05-PADRAO-OPERACIONAL-ROTEIRO.md)

# FASE 3 — ROTEIRO / SCRIPT GATE

Fonte responsável: [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). Consultar o contrato vigente de roteiro da modalidade e duração escolhidas, incluindo entrada, naturalidade, continuidade, fala ou silêncio, limites, formato e checagens. Estados, escolha de duração e controles de aprovação pertencem ao [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Esta visão geral não redefine os contratos.

- 📄 [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md)

- 📄 [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md)

- 📄 [08 — FLUXO OPERACIONAL INTEGRADO — V2](./08-FLUXO-OPERACIONAL-INTEGRADO.md)

- 📄 [ZZ — DESATIVADO — SEM AUTORIDADE OPERACIONAL](./ZZ-DESATIVADO.md)

- 📄 [09 — ARQUIVO PASSIVO DE EXECUÇÕES — SEM AUTORIDADE OPERACIONAL](./09-ARQUIVO-PASSIVO.md)

- 🗂️ [10 — REGISTRO ATIVO DE EXECUÇÕES — QWE](./10-REGISTRO-ATIVO-QWE.md)

## FORMATO 15s — REFERÊNCIA À FONTE RESPONSÁVEL

Aplicar a seção “FORMATO 15s EM 5s + 10s” do [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md).

## BIBLIOTECA TRANSVERSAL DE GANCHOS — REFERÊNCIA

Consultar “BIBLIOTECA TRANSVERSAL DE GANCHOS — FONTE RESPONSÁVEL” no [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). A biblioteca foi transferida integralmente, com abertura derivada do Pacote Criativo aprovado, sem seleção independente.

## REGRA UNIVERSAL DE INTERAÇÃO — RESPOSTAS CLICÁVEIS (09/10/2026)

Consultar o contrato de interação e respostas clicáveis na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## CONTROLE DE CONSISTÊNCIA DO LOOP — 09/10/2026

Os contadores, marcadores idempotentes, tentativa única de escrita final e conclusão não bloqueante seguem exclusivamente o Lifecycle [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md), seções CONTADORES DE RASTREABILIDADE e ARCHIVE\_WRITE → EXECUTION\_DONE. As transições e a decisão de nova versão seguem o Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Preservar aprovações e materiais confiáveis conforme essas fontes; não recalcular nem gravar o fechamento por esta cópia.

## REGRA ATIVA — AUTOAUDITORIA DE IMAGENS (09/10/2026)

Após toda geração ou refação da imagem-base e da capa, executar e registrar autoauditoria visual obrigatória <b>antes de apresentar o gate e avançar</b>. Conferir produto, influencer, detalhes, formato e conceito. Divergência = informar e recomendar refazer; nunca avançar automaticamente. O Runtime / State Machine V2 é a autoridade da rotina detalhada. Em todo gate de imagem/capa, apresentar REFAZER/APROVAR pelo ADAPTADOR\_DE\_INTERFACE do Runtime, com cores obrigatórias em NATIVE ou degradação TEXT autorizada; a resposta válida envia o evento 0/1 correspondente, mantendo aprovação exclusivamente humana.

## ESCLARECIMENTO DA REGRA DE BOTÕES APÓS IMAGENS — 09/10/2026

Consultar a apresentação dos controles de decisão após imagens na fonte responsável: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

## GATILHO TRANSVERSAL DE AUTOANÁLISE — 09/10/2026

Em toda resposta a opção do usuário e antes de oferecer qualquer novo conjunto de escolhas, aplicar obrigatoriamente o <b>GATILHO UNIVERSAL DE AUTOANÁLISE POR RESPOSTA / GATE</b>, definido no <code>00 — RUNTIME / STATE MACHINE — V2</code>. Esta página apenas estabelece sua obrigatoriedade universal; checklist, lógica de transição, checkpoint, ferramenta e travas pertencem exclusivamente ao Runtime. É proibido terminar com anúncio de geração sem executar a ferramenta ou sem declarar o bloqueio real. O gatilho não cria gate adicional nem autoriza avançar sem aprovação humana.

## ROTEIRO MOV — SILÊNCIO E DEMONSTRAÇÃO VISUAL

Aplicar o contrato MOV vigente do [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md), incluindo silêncio absoluto, gestos, enquadramento, duração e formato do roteiro. Os Elementos de Texto e a capa pertencem ao [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); não redefinir essas regras nesta cópia.

## REGRA MOV — TRADUÇÃO ESTRATÉGICA EM LINGUAGEM VISUAL

REGRA ATUAL MOV: OBJETIVO=A/DESCOBERTA fixo, NEXT\_ADVANCE e mecanismo integrados automaticamente ao diagnóstico. MOV traduz o mecanismo visualmente e utiliza <code>CREATIVE_PACKAGE_GATE</code> como única seleção estratégica humana.

REGRA OBRIGATÓRIA PARA VIDEO\_FORMAT=MOV: cada Pacote Criativo A/B/C precisa ter efeito observável distinto nos enquadramentos, gestos, ritmo, sequência e ênfase audiovisual, sustentado pelo produto e evidências, sem depender de narração, fala, texto na tela ou CTA falada. Não existe escolha separada em <code>OPENING_STYLE_GATE</code> ou <code>CONCEPT_GATE</code>.

<b>EXEMPLOS VISUAIS ADAPTÁVEIS:</b> os exemplos seguintes não atribuem objetivos às letras A/B/C; o objetivo vigente permanece DESCOBERTA e os três pacotes são diferenciados dinamicamente conforme P03.

Reconhecimento e curiosidade: priorizar reconhecimento e curiosidade visual inicial; entrada visual marcante e legibilidade geral do produto, sem alegar desempenho.

Inspeção e entendimento: priorizar inspeção visual e entendimento dos atributos verificáveis; planos próximos com tempo para observar detalhes pertinentes.

Visão para decisão informada: priorizar visão que favoreça decisão informada do produto em uso, diferentes ângulos úteis e fechamento visual natural; não presume intenção prévia de compra, nem usa urgência/preço/promessa não comprovada.

Estas são DIREÇÕES AUDIOVISUAIS GERAIS para diferenciar o gate, NÃO conceitos/roteiros fechados: o mecanismo é automático; mensagem, abertura e conceito integram a mesma opção aprovada em <code>CREATIVE_PACKAGE_GATE</code> e determinam a execução concreta, sem escolhas humanas separadas. O sistema NÃO fixa uma tomada, gesto ou cronograma idêntico para categorias diferentes. Adaptação universal a moda, acessórios, bolsas, beleza e qualquer produto por seus atributos reais. No MOV com celular, selfie no espelho e aparelho na altura do rosto, sem exigir cobertura integral da face; no MOV sem celular, câmera externa abaixo do pescoço; rosto fora do enquadramento e produto em destaque nas duas composições; para todo MOV, SILÊNCIO ABSOLUTO sem fala/narração/CTA falada, vídeo-base sem overlays ou música. Na FASE 3, validar se as ações e planos efetivamente cumprem o objetivo DESCOBERTA e o pacote escolhido e diferem logicamente dos outros dois, sem reabrir gates aprovados.

Ranking A/B/C e seleção aplicam-se ao <code>CREATIVE_PACKAGE_GATE</code>.

## MOV V2 — REFERÊNCIA AO CONTRATO DO ROTEIRO

A fonte responsável é a seção “MOV V2 — CONTRATO OPERACIONAL DO ROTEIRO” do [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). O conteúdo transferido preserva núcleo, composição com/sem celular, coreografia, retenção opcional, silêncio, duração, algoritmo, autoauditoria e precedência vigente. Esta página não mantém contrato concorrente.
