# 00 — RUNTIME / STATE MACHINE — V2

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-11-04T01:26:18.949Z:. Fonte: https://app.notion.com/p/9eafafd5013b8241b69181e1ec34ca5f

---

## APLICAÇÃO DA DECISÃO CANÔNICA — PERSISTÊNCIA SOMENTE NA CONVERSA (19/10/2026)

<b>Prevalência:</b> esta regra aplica a decisão explícita do usuário de 19/10/2026 e prevalece sobre qualquer instrução legada desta página que determine criar, consultar, atualizar ou sincronizar linhas do Registro Ativo, checkpoints, snapshots, logs ou registros individuais por vídeo. Nenhuma execução SAC/QWE/MOV deve ser registrada individualmente no Notion.

<b>Estado e continuidade:</b> manter STATE, eventos confirmados, materiais, evidências, locks, decisões humanas, aprovações e artefatos necessários ao fluxo no contexto da conversa. Não exigir persistência no Notion para iniciar, avançar, pausar, retomar ou concluir uma execução. Não criar nem consultar registros individuais para recuperar estado. Não anunciar sincronização pendente por ausência de registro.

<b>Escopo preservado:</b> o Notion permanece fonte canônica das regras. Esta decisão não altera a ordem dos estados, os gates, as evidências, os locks, os requisitos de aprovação humana, as autoridades dos Engines, o adaptador de interface nem o contrato de conclusão. O Lifecycle continua autoridade dos contadores, mas seus valores e marcadores são mantidos no estado da conversa, sem gravação por execução.

<b>Leitura de legado:</b> instruções posteriores nesta página que mencionem Registro Ativo, criação de linha, checkpoint, snapshot ou sincronização devem ser interpretadas como legado documental sem efeito operacional, na extensão em que contrariem esta regra.

---

## DECISÃO DO USUÁRIO: SEM CONTROLE OPERACIONAL OU CHECKPOINTS (19/10/2026)

<b>Regra vigente:</b> o usuário não precisa nem deseja controle de execução no Notion. Não criar linhas de Registro Ativo, checkpoints, snapshots, logs de execução ou registros de sincronização para acompanhar cada vídeo. Não exigir gravação antes de pedir materiais, antes de uma transição ou para continuar o fluxo. Não anunciar “sincronização pendente” por ausência desse registro, nem transformar persistência operacional em etapa visível ou bloqueio. Conduzir o trabalho nesta conversa pelos eventos e materiais efetivamente recebidos, preservando todos os gates criativos e aprovações humanas reais. O Notion continua sendo fonte canônica das regras do SAC, mas não deve ser usado para rastrear cada execução individual. Só alterar documentação/regras no Notion quando o usuário solicitar explicitamente.

## CONTRATO DE ESTADO, SAÍDA E RECUPERAÇÃO

<b>A CADA ENTRADA:</b> determinar STATE confirmado e evento efetivamente recebido. Executar exclusivamente handler autorizado; conferir pré-condições, evidência, locks e decisão humana. Nenhum comentário, silêncio, material ou valor ambiguamente digitado aprova gate. Uma transição só se considera executada após resultado observável da ferramenta ou confirmação válida do usuário. Se escrita no Notion falhar, aplicar persistência não bloqueante vigente sem fingir sucesso.

<b>PRÉ-SAÍDA OBRIGATÓRIA:</b> toda interação finita deve ser emitida exclusivamente pelo <code>ADAPTADOR_DE_INTERFACE</code> do núcleo de entrada. O handler define apenas o significado das opções e a transição; não define texto literal como substituto de controle.

# ADAPTADOR\_DE\_INTERFACE — AUTORIDADE ÚNICA PARA GATES FINITOS

Fonte única desta seção transferida para o núcleo de entrada [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md), seção com o mesmo nome. Carregar e aplicar o contrato vigente ali; este ponteiro não mantém outra definição.

## INTERFACE LIMPA CONSOLIDADA

Regra operacional vigente no SAC, QWE e MOV.

<b>PRINCÍPIO:</b> aplicar “INTERFACE LIMPA — REGRA CANÔNICA DE SAÍDA” e o ADAPTADOR\_DE\_INTERFACE; não acrescentar confirmação separada.

<b>MODALIDADE:</b> aplicar os rótulos completos e as cores obrigatórias definidos em “RÓTULOS OFICIAIS DO MODALITY\_GATE”.

<b>CRIAÇÃO:</b> aplicar a composição dos pacotes da seção P03 do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md) e a exclusividade da escolha/derivação definida em P01 e GATE CRIATIVO UNIFICADO do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

<b>FLUXO PRESERVADO:</b> não acrescentar gate e não pular seleção de modalidade, materiais, duração, aprovação criativa, IMAGE\_READY, IMAGE\_GATE, SCRIPT\_GATE, TEXT\_ELEMENTS\_GATE, COVER\_GATE nem demais gates reais previstos. PRODUCT\_LOCK, INFLUENCER\_LOCK e evidências permanecem obrigatórios. QWE pode utilizar fala; MOV permanece sem fala. Confirmar efetivamente cada ação antes de anunciar conclusão.

<b>AUDITORIA:</b> validar a interface conforme os contratos vigentes e manter os testes de ponta a ponta como verificação prática separada.

## EXCLUSIVIDADE DO PACOTE CRIATIVO

O único gate humano de seleção estratégica criativa é <b>CREATIVE\_PACKAGE\_GATE</b>, com exatamente três pacotes integrados A/B/C e seleção explícita pelo ADAPTADOR\_DE\_INTERFACE e seu nível vigente. Cada pacote integra mensagem central, abertura dos primeiros três segundos e conceito audiovisual (inclusive direcionamento visual); esses elementos são derivados da mesma opção selecionada, sem decisões humanas individuais.

Aplicar o CONTRATO DE STATE MACHINE ATIVA. <code>CREATIVE_PACKAGE_GATE</code> permanece a única escolha estratégica humana.

<b>ESTADOS DERIVADOS:</b> após aprovação real de CREATIVE\_PACKAGE\_GATE, definir CREATIVE\_PACKAGE\_APPROVED=TRUE e derivar MESSAGE\_CENTRAL\_APPROVED, OPENING\_STYLE\_OK, CONCEPT\_APPROVED e CONCEPT\_OK da mesma opção, sem solicitar cliques adicionais. IMAGE\_READY exige pacote aprovado e os demais locks/evidências/prontidões já vigentes; nunca exige aprovação humana separada desses componentes.

<b>PRESERVAR:</b> escolha de modalidade QWE/MOV, duração, materiais, PRODUCT\_LOCK, INFLUENCER\_LOCK, AIDA/descoberta/mecanismo automáticos, IMAGE\_GATE, SCRIPT\_GATE, TEXT\_ELEMENTS\_GATE, COVER\_GATE, INTERFACE LIMPA, MOV sem fala e proibição de inventar atributos. Em retomadas, respeitar aprovações humanas válidas já realizadas; alterações materiais em artefatos aprovados voltam somente ao gate pertinente.

<b>AUTOAUDITORIA SILENCIOSA:</b> antes de emitir o próximo gate, verificar que não foi oferecida aprovação separada de mensagem, abertura ou conceito. Se a execução estiver inconsistente, bloquear avanço até resolver o estado internamente.

## RÓTULOS OFICIAIS DO MODALITY\_GATE

Fonte única desta seção transferida para o núcleo de entrada [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md), seção com o mesmo nome. Carregar e aplicar o contrato vigente ali; este ponteiro não mantém outra definição.

## INTERFACE LIMPA — REGRA CANÔNICA DE SAÍDA

Em SAC (QWE/MOV), apresentar ao usuário SOMENTE conteúdo que exija interação ou seja o artefato da etapa: pergunta ou decisão atual, opções pelo nível disponível do adaptador e instrução estritamente necessária. Realizar leitura de Bootstrap/Runtime/Notion, diagnósticos, persistência, estados, checkpoints, rastreabilidade técnica e autoauditorias internamente, sem narrar, anunciar sucesso, exibir nomes internos de gates ou publicar relatórios de rotina. A autoauditoria dos botões continua obrigatória, porém silenciosa. <b>CONTRATO DE DECISÃO FINITA:</b> aplicar exclusivamente o ADAPTADOR\_DE\_INTERFACE, que define ação única e recuperação. MODALITY\_GATE: exibir “SAC — Escolha a modalidade” e os rótulos completos da seção “RÓTULOS OFICIAIS DO MODALITY\_GATE”. Os demais gates devem ser igualmente concisos. Preservar integralmente escolhas humanas, validação factual, Product Lock, Influencer Lock e aprovações de imagem/roteiro/textos/capa. Só exibir detalhe operacional se houver falha real, informação faltante ou solicitação explícita de auditoria/explicação; nunca alegar que ação de ferramenta foi realizada sem confirmação. Se ferramentas exibirem atividade automática fora do conteúdo controlável da resposta, não repetir essa atividade no texto ao usuário. Prioridade: a decisão humana deve ser o foco visual exclusivo da resposta.

A pista \{\[n\]\} do CREATIVE\_PACKAGE\_GATE permanece visível por decisão do usuário: é informação de uso da alternativa para ajudar a escolha, não exposição do checkpoint técnico. Em TEXT, mostrar somente os códigos/rótulos necessários à resposta, sem relatório repetido da falha.

## PADRÃO VISUAL ATUAL — ESCOLHA DA MODALIDADE

Aplicar os rótulos completos e as cores obrigatórias da seção “RÓTULOS OFICIAIS DO MODALITY\_GATE”, com os controles definidos no ADAPTADOR\_DE\_INTERFACE. A validade é conferida no checklist “AUTOAUDITORIA 100% DOS CONTROLES CLICÁVEIS”.

## GATE UNIVERSAL DE AUTOAUDITORIA DOS BOTÕES — REGRA OBRIGATÓRIA

Executar o checklist AUTOAUDITORIA 100% DOS CONTROLES CLICÁVEIS em toda decisão finita. Em NATIVE, exigir controles funcionais e cores obrigatórias. Em TEXT, validar a degradação autorizada e as opções exatas do gate. UI\_BUTTONS\_READY=FALSE não bloqueia a alternativa textual; evidências, locks e aprovação humana permanecem obrigatórios.

## CONTROLES COLORIDOS UNIVERSAIS

Aplicar o ADAPTADOR\_DE\_INTERFACE e a paleta obrigatória de RÓTULOS OFICIAIS DO MODALITY\_GATE. A alternativa textual é degradação explícita por limitação/falha, não torna as cores opcionais nos botões.

## GATE CRIATIVO UNIFICADO

Mensagem Central, Abertura e Conceito integram o mesmo Pacote Criativo. AIDA, NEXT\_ADVANCE, objetivo DESCOBERTA e mecanismo criativo são automáticos.

<b>CREATIVE\_PACKAGE\_PREP (automático):</b> após evidências e locks válidos, formular internamente a MENSAGEM\_CENTRAL e criar exatamente três propostas integradas A/B/C. Cada uma contém: (1) mensagem central única, clara e factual; (2) estilo e execução dos primeiros 3 segundos; (3) conceito audiovisual com cena, enquadramento, gesto, dinâmica e execução coerentes com o produto e a modalidade. Não exigir que as três propostas tenham a mesma mensagem, mas cada uma deve ser coerente com a estratégia fixa e com a evidência. Ranking por estrelas e diferenças audiovisuais reais entre A/B/C. Não presumir características não verificadas.

<b>CREATIVE\_PACKAGE\_GATE (único gate humano):</b> mostrar A, B e C de modo comparável, com conteúdo específico e nota contextual; seleção humana explícita pelo ADAPTADOR\_DE\_INTERFACE e seu nível vigente; nenhuma opção vem pré-selecionada. Se houver reprovação/solicitação de refazer, regenerar propostas sem avançar. Quando aprovado, registrar CREATIVE\_PACKAGE\_SELECTED=\<A\|B\|C>, CREATIVE\_PACKAGE\_APPROVED=TRUE, MENSAGEM\_CENTRAL da opção escolhida, OPENING\_STYLE\_SELECTED e CONCEPT\_SELECTED derivados da MESMA opção, sem solicitar três aprovações. Marcar MESSAGE\_CENTRAL\_APPROVED, OPENING\_STYLE\_OK, CONCEPT\_APPROVED e CONCEPT\_OK como validações derivadas do pacote, NÃO como gates ou cliques independentes.

<b>CONTRATO DE STATE MACHINE ATIVA:</b> a modalidade é resolvida em <code>MODALITY_GATE</code>; duração em <code>DURATION_GATE</code>; diagnóstico/NEXT\_ADVANCE, objetivo DESCOBERTA e mecanismo são internos; mensagem, abertura e conceito derivam do pacote aprovado em <code>CREATIVE_PACKAGE_GATE</code>, única escolha estratégica humana. Depois seguem <code>IMAGE_GATE → SCRIPT_GATE → TEXT_ELEMENTS_GATE → COVER_GATE → ARCHIVE_WRITE → EXECUTION_DONE</code>. Rastreabilidade humana registra somente a seleção do pacote.

<b>IMAGE\_READY:</b> requer CREATIVE\_PACKAGE\_APPROVED=TRUE, conteúdo do pacote coerente e seus estados derivados, mais todos os demais requisitos de MATERIALS\_OK, EVIDENCE\_OK, PRODUCT\_LOCK\_OK, INFLUENCER\_LOCK\_OK e diagnóstico/estratégia automáticos. Não bloquear imagem aguardando 0/1 de mensagem ou A/B/C de abertura/conceito.

<b>FLUXO CANÔNICO:</b> SAC → MODALITY\_GATE QWE/MOV → materiais + duração + influencer → diagnóstico/AIDA + DESCOBERTA + mecanismo automáticos → CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE A/B/C → autoauditoria IMAGE\_READY → IMAGE\_GEN → IMAGE\_GATE 0/1 → SCRIPT\_GATE 0/1 → TEXT\_ELEMENTS\_GATE 0/1 → COVER\_GATE 0/1 → ARCHIVE\_WRITE → EXECUTION\_DONE → loop do mesmo produto com nova escolha de modalidade/duração e novo pacote. Preservar IMAGE\_GATE, SCRIPT\_GATE, TEXT\_ELEMENTS\_GATE, COVER\_GATE, fidelidade estrita ao produto e variante, Influencer Lock e MOV sem fala.

## MECANISMO CRIATIVO AUTOMÁTICO

Diagnóstico AIDA e NEXT\_ADVANCE são internos; OBJETIVO=DESCOBERTA é automático; o mecanismo criativo é automático.

<b>MECANISMO:</b> aplicar os critérios de seleção e tradução audiovisual da seção MECANISMO CRIATIVO AUTOMÁTICO no Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md).

<b>ESTADOS:</b> MECHANISM\_GATE desativado, não emitir alternativas A/B/C nem botão de confirmação, nem solicitar aprovação humana. Registrar internamente MECHANISM\_SELECTED e MECHANISM\_READY=TRUE com justificativa curta e evidências. Não exigir aprovação humana de mecanismo nem somar letra ou clique desse mecanismo à rastreabilidade humana.

<b>SEQUÊNCIA VIGENTE:</b> SAC → MODALITY\_GATE → materiais/duração/Influencer Lock → AIDA, DESCOBERTA e mecanismo automáticos → CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE A/B/C → IMAGE\_READY/IMAGE\_GEN/IMAGE\_GATE → SCRIPT\_GATE → TEXT\_ELEMENTS\_GATE → COVER\_GATE → ARCHIVE\_WRITE → EXECUTION\_DONE → novo vídeo do mesmo produto com modalidade e duração novamente definidas.

<b>CONDIÇÃO DA IMAGEM:</b> <code>MECHANISM_READY=TRUE</code> é interno. Produto, evidências, locks e Pacote Criativo aprovado permanecem pré-requisitos. O primeiro e único gate estratégico humano é <code>CREATIVE_PACKAGE_GATE</code>; mensagem, abertura e conceito são derivados do pacote aprovado.

<p>
<b>QWE/MOV:</b> QWE permite fala de acordo com suas regras; MOV permanece absolutamente sem fala. Na modalidade MOV, mecanismo deve ser traduzido por movimentos, gestos, enquadramentos e interação visual. 
</p>

<b>Preservar:</b> gates humanos vigentes; Fidelity/PRODUCT\_LISTING\_MATCH; sincronização semântica; não reabrir decisões já aprovadas.

## SAC ENXUTO / AIDA + DESCOBERTA

Aplicar esta estrutura em todas as execuções SAC, preservando modalidade, materiais, duração, influencer, imagem, roteiro, Elementos de Texto e capa.

<b>Mudança 1 — AIDA integrado ao diagnóstico automático:</b> aplicar Atenção, Interesse, Desejo e Ação como lógica flexível da preparação do criativo para o feed TikTok, não como quatro blocos obrigatórios, nem uma sequência rígida ou gate. Diagnosticar necessidades e evidências sem inventar perfil, interesse ou conhecimento de audiência.

<b>NEXT\_ADVANCE:</b> calcular internamente como direção de trabalho integrada ao diagnóstico/AIDA, sem gate ou escolha humana.

<b>Mudança 3 — OBJETIVO CRIATIVO fixo:</b> registrar automaticamente OBJECTIVE\_SELECTED=A, OBJECTIVE=DESCOBERTA, OBJECTIVE\_READY=TRUE, sem OBJECTIVE\_GATE e sem opções A/B/C. Significa desenvolver qualquer vídeo para ser compreensível e atrativo ao público frio durante o scroll, sem afirmar que toda espectadora é fria ou impedir desejo, ação e decisão de compra dentro do mesmo vídeo. A descoberta é porta de entrada, não proibição de conversão.

<b>Fluxo estratégico vigente:</b> SAC → MODALITY\_GATE → materiais, duração e influencer → AIDA/NEXT\_ADVANCE + objetivo DESCOBERTA + mecanismo automáticos → CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE A/B/C → IMAGE\_READY + autoauditoria → IMAGE\_GATE → SCRIPT\_GATE → TEXT\_ELEMENTS\_GATE → COVER\_GATE → ARCHIVE\_WRITE → EXECUTION\_DONE.

<b>IMAGE\_READY:</b> aplicar integralmente a lista única CONTRATO IMAGE\_READY do Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md). Os handlers não executam gates estratégicos aposentados; estados automáticos e derivados não são aprovações humanas independentes.

<b>Rastreabilidade:</b> a única escolha estratégica humana contabilizada é a seleção A/B/C em <code>CREATIVE_PACKAGE_GATE</code>. <code>TRACE_SEQUENCE=[PACOTE:<letra>]</code>. OBJECTIVE, MECHANISM, MENSAGEM\_CENTRAL, ABERTURA e CONCEITO são automáticos ou derivados do pacote e não geram contadores humanos.

<b>Loop:</b> ao começar nova versão do mesmo produto, escolher modalidade e duração conforme BOOT SAC vigente, reconstruir diagnóstico/AIDA, atribuir DESCOBERTA e calcular mecanismo internamente; seguir para <code>CREATIVE_PACKAGE_PREP → CREATIVE_PACKAGE_GATE</code>, conforme o CONTRATO DE STATE MACHINE ATIVA.

<b>Preservações críticas:</b> MOV sem fala, QWE com fala; PRODUCT\_LISTING\_MATCH, fidelidade máxima de imagem, Influencer Lock, gates humanos vigentes, interface conforme o adaptador, registro honesto de sincronização e verificação externa do vídeo pelo usuário. Falta de evidência relevante bloqueia só a parte dependente, sem inventar atributos.

## MATRIZ DE EXECUÇÃO POR MODALIDADE — REFERÊNCIAS

SAC é o sistema-mãe; QWE e MOV são modalidades irmãs, resolvidas exclusivamente por <code>MODALITY_GATE</code> em nova execução e nova versão. Registrar somente <code>VIDEO_FORMAT=QWE</code> ou <code>VIDEO_FORMAT=MOV</code>.

Contratos audiovisuais, incluindo fala QWE e ausência de fala MOV, composição e duração: Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). Peças textuais, limites e capa: Engine de Elementos de Texto [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md). Evidências, fidelidade comercial e locks: Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md). Contadores e fechamento: Lifecycle [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).

O Runtime aplica esses contratos aos handlers vigentes; não cria contrato criativo concorrente. Preservar aprovações humanas, condições de IMAGE\_READY e da capa, recuperação de interface e persistência não bloqueante. No loop do mesmo produto, seguir <code>MODALITY_GATE → DURATION_GATE → CREATIVE_PREP → CREATIVE_PACKAGE_PREP → CREATIVE_PACKAGE_GATE</code>.

# AUTORIDADE

Esta página é o runtime executável da V2 inteira do SAC, com duas modalidades irmãs: QWE e MOV. Controla estado, eventos e transições de cada execução SAC. Não redefine as regras criativas pertencentes aos Engines; referencia suas autoridades e impõe a ordem de execução.

Fontes relacionadas: entrada e interface [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md); estados [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md); evidências/locks [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); audiovisual [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); textos/capa [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); fechamento [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).

# PERSISTÊNCIA DO ESTADO ATIVO

O registro operacional durável é [10 — REGISTRO ATIVO DE EXECUÇÕES — QWE](./10-REGISTRO-ATIVO-QWE.md). Ele armazena checkpoints da execução atual; não é fonte de regras. A página-mãe e os Engines continuam sendo a autoridade canônica das regras. O <code>09 — ARQUIVO PASSIVO</code> continua sem autoridade operacional.

Criar uma linha por execução antes de responder ao primeiro pedido de material: <code>Execução=QWE — <produto ou aguardando materiais></code>, <code>Status=Ativa</code>, <code>STATE=MATERIALS_WAIT_PRODUCT</code>, duração ainda não definida e próxima ação pendente. Guardar o URL/ID da linha durante a execução. Cada nova versão do mesmo produto recebe nova linha.

Preencher as propriedades existentes da linha: <code>Execução</code>, <code>Status</code>, <code>STATE</code>, <code>Duração</code>, <code>Produto</code>, <code>Link do produto</code>, <code>Último gate resolvido</code> e <code>Próxima ação esperada</code>; <code>ID da execução</code> e <code>Última atualização</code> são gerados pelo Notion. No corpo da linha, manter um único snapshot vigente com: CHECKPOINT ATUAL (estado, última transição confirmada, pendência exata, pausa/retorno), MATERIAIS E EVIDÊNCIAS, CONTEXTO E DIAGNÓSTICO, DECISÕES/GATES E APROVAÇÕES, ARTEFATOS E STATUS (imagem, roteiro, ELEMENTOS DE TEXTO e capa). Substituir o snapshot atual a cada gravação; manter apenas o estado vigente.

Atualizar os campos e o corpo do registro <b>antes de confirmar qualquer transição ao usuário</b> e imediatamente após cada resposta válida de gate, pausa/retomada, alteração de estado, resultado de ferramenta ou aprovação/reprovação. O checkpoint deve registrar, no mínimo: identificador e Status; <code>STATE</code>; produto, link e referências dos materiais, incluindo <code>INFLUENCER_REFERENCE_USABLE</code> e <code>INFLUENCER_LOCK_OK</code>; <code>SCRIPT_DURATION</code>; evidências/contexto/diagnóstico; escolhas e aprovações de NEXT\_ADVANCE, OBJETIVO, MECANISMO, MENSAGEM\_CENTRAL (incluindo revisão), ABERTURA e CONCEITO; contadores de rastreabilidade vigentes por produto, gate e letra, e <code>COUNTERS_COMMITTED</code> e <code>ARCHIVE_WRITE_ATTEMPTED</code> para impedir incrementos e gravações duplicadas; imagem candidata/aprovada; roteiro e gate; ELEMENTOS DE TEXTO e gate; imagem-base da capa, texto da capa e gate; <code>PAUSED</code> e estado de retorno; último gate realmente resolvido; e a próxima ação exata esperada do usuário ou do sistema. Registrar somente decisões e fatos realmente ocorridos; nunca converter comentário, silêncio ou inferência em aprovação. No fechamento após <code>COVER_GATE=1</code>, agrupar aprovação final, contadores e estado terminal na única tentativa prevista no Lifecycle; não emitir checkpoints terminais adicionais.

Antes de qualquer chamada de ferramenta, tentar gravar checkpoint pré-ferramenta com estado, pré-condições e saída esperada. Após o retorno, tentar registrar resultado e novo estado. Se a gravação do estado ativo falhar, preservar a última versão confirmada do checkpoint, marcar sincronização pendente e seguir somente pelo próximo handler legítimo já sustentado por evidências, locks, resultados reais e decisões humanas válidas, conforme a persistência não bloqueante. A falha de escrita nunca cria aprovação, nunca autoriza salto de gate e nunca permite afirmar que uma mudança de estado foi salva sem confirmação do Notion.

<b>AUTORIDADE DE ATIVAÇÃO:</b> <code>SAC</code> é o comando canônico de início/reinício. <code>QWE</code> e <code>MOV</code> são valores de modalidade resolvidos em <code>MODALITY_GATE</code>. Ao receber <code>SAC</code> para iniciar/reiniciar, marcar a linha anterior ainda não terminal como <code>Resetada</code>, registrar o motivo <code>novo SAC</code>, criar uma nova linha e aplicar o reset completo. No loop de nova versão do mesmo produto, criar nova linha após a conclusão da anterior e antes de <code>MODALITY_GATE</code>; o loop é iniciado pelo evento válido NOVA VERSÃO DO MESMO PRODUTO no nível vigente do adaptador.

Em retomada explicitamente solicitada, recuperar somente a linha identificada como <code>Ativa</code>, <code>Pausada</code> ou <code>Bloqueada</code>, revalidá-la contra as regras canônicas vigentes e restaurar apenas o último checkpoint confirmado. Retomar do primeiro estado pendente; não aprovar gates. Se houver mais de uma linha elegível ou checkpoint incompleto/conflitante, bloquear e pedir a identificação ou o dado faltante. Linhas <code>Concluída</code> ou <code>Resetada</code> são terminais: nunca usá-las para orientar outra execução. O registro não gera aprendizado nem recomendações.

No snapshot vigente registrar também INTERFACE\_MODE, UI\_ATTEMPTED\_FOR, UI\_BUTTONS\_READY, motivo da degradação e INPUT\_SOURCE, vinculados à execução/gate/revisão. Seguir a mesma política de escrita não bloqueante e tentativa terminal única; esses campos não criam gravações adicionais.

Campo de acompanhamento: Sincronização = Não verificada, Confirmada ou Pendente; vazio significa Não verificada. Incluir o valor planejado na mesma atualização de checkpoint, sem chamada adicional. Só afirmar Confirmada após retorno de sucesso. Se a escrita falhar, manter Pendente no estado da conversa e informar uma vez “Sincronização pendente”; uma falha não pode ser considerada registrada no Notion sem retorno verificável. Reconciliar na próxima escrita legítima; não repetir a tentativa final nem reinterpretar Status da execução como status de sincronização. Registros retrospectivos permanecem identificados e nunca são prova de checkpoint em tempo real.

# ESTADOS DO RUNTIME IMPLEMENTADO

<code>IDLE → MODALITY_GATE → MATERIALS_WAIT_PRODUCT → MATERIALS_CONFIRM_INFLUENCER / MATERIALS_WAIT_INFLUENCER → CREATIVE_PREP (diagnóstico AIDA, OBJETIVO=DESCOBERTA e MECANISMO automáticos) → CREATIVE_PACKAGE_PREP → CREATIVE_PACKAGE_GATE → IMAGE_READY → IMAGE_GEN → IMAGE_GATE → SCRIPT_PREP → SCRIPT_OUTPUT_CHECK → SCRIPT_GATE → TEXT_ELEMENTS_PREP → TEXT_ELEMENTS_OUTPUT_CHECK → TEXT_ELEMENTS_GATE → COVER_WAIT_ANCHOR_IMAGE → COVER_READY → COVER_GEN → COVER_GATE → ARCHIVE_WRITE → EXECUTION_DONE → MODALITY_GATE → DURATION_GATE → CREATIVE_PREP (AIDA/DESCOBERTA/mecanismo automáticos) → CREATIVE_PACKAGE_PREP → CREATIVE_PACKAGE_GATE</code>

<code>IMAGE_READY</code> é um estado derivado: só existe quando o Rules Engine da Fase 2 retornar todas as condições obrigatórias como TRUE. Nenhuma das validações derivadas de mensagem, abertura e conceito exige aprovações humanas independentes; todas decorrem da escolha efetivamente confirmada em CREATIVE\_PACKAGE\_GATE.

## MATRIZ DE TESTES POR GATE — GRUPO 7 (16/10/2026)

<b>FINALIDADE:</b> especificação de teste dos handlers vigentes. Não cria estado, gate, botão ou confirmação. Governança, limites e registro consolidado: [SAC MÃE](./00-SAC-MAE.md), seção GRUPO 7 — GOVERNANÇA DA ARQUITETURA.

<b>COMO AVALIAR:</b> cada caso tem PASS quando a execução observada cumpre o esperado, inclusive quando o resultado correto é bloquear ou manter o gate. Divergência observada é FAIL; caso sem execução é PENDENTE. PASS do teste é separado da aprovação humana do artefato e do resultado técnico do check.

<b>FONTES DOS CRITÉRIOS:</b> evidências/locks em [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); audiovisual em [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); textos/capa em [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); contagem/fechamento em [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md). A matriz verifica a aplicação dos contratos, não redefine seus critérios.

<b>COBERTURA:</b> percursos QWE 10s, QWE 15s, MOV 10s e MOV 15s; no MOV, incluir composição com celular e sem celular nos casos visuais. Exercitar aprovação, rejeição e entradas inválidas pelos handlers atuais, com os gates humanos existentes. Esta manutenção não inicia esses percursos e não presume suas aprovações.

| Gate ou ponto de controle | Resultado esperado para PASS | Variações mínimas |
| --- | --- | --- |
| Entrada / MODALITY\_GATE | SAC carrega Bootstrap e núcleo de entrada; modalidade não é presumida. Evento válido do adaptador escolhe a modalidade e o handler registra somente a escolha efetiva. | QWE e MOV, nova execução e nova versão; verificar ordem e rótulos oficiais. |
| Duração | Somente a escolha válida pelo handler vigente registra duração; modalidade já está resolvida. Pendência mantém o estado e não libera criação. | 10s e 15s; escolha ausente/inválida; rota inicial e loop. |
| Influencer | Gate e referência são tratados pelo Runtime; o Rules Engine confirma utilizabilidade. Referência enviada e acessível pode ser reutilizada; ausência ou inadequação exige imagem clara, sem promessa de padrão armazenado. | Imagem enviada nesta execução; nova imagem; falta de acesso, nitidez ou conflito. |
| CREATIVE\_PACKAGE\_GATE | Três pacotes são apresentados pelo adaptador; somente a escolha humana válida aprova o pacote e seus estados derivados. Nenhum gate estratégico aposentado reaparece. | A, B e C; ausência de escolha; mudança de pacote sem aprovação presumida. |
| IMAGE\_READY / pré-ferramenta | Todos os termos do CONTRATO IMAGE\_READY do Rules Engine e o checkpoint vigente são verificados. Condição ausente impede IMAGE\_GEN; material recebido não é autorização. | Caso válido e caso com material, evidência, lock ou aprovação realmente ausente. |
| IMAGE\_GATE | Resultado real e autoauditoria visual antecedem a decisão humana. Aprovar segue o handler; refazer regressa ao menor ponto. Falha de ferramenta não produz gate de imagem inexistente. | Aprovar e refazer; erro de ferramenta; divergência factual; controles após imagem. |
| SCRIPT\_OUTPUT\_CHECK / SCRIPT\_GATE | Somente roteiro que atende ao Creative Engine da modalidade/duração chega ao gate. Aprovar libera textos, não execução ou upload de vídeo; refazer mantém a revisão no fluxo pertinente. | QWE 10s/15s; MOV 10s/15s sem voz; composição MOV com e sem celular. |
| TEXT\_ELEMENTS\_OUTPUT\_CHECK / TEXT\_ELEMENTS\_GATE | Somente peças do contrato da modalidade passam ao usuário. Check interno não é aprovação; aprovação válida encaminha à âncora da capa conforme o handler. | QWE e MOV; conjunto válido; peça inválida; refação parcial e do conjunto. |
| COVER\_WAIT\_ANCHOR\_IMAGE / COVER\_READY | A capa só começa após textos aprovados, recebe a imagem exata exigida e valida texto e condições do Text Engine antes da ferramenta. | Âncora correta, ausente ou divergente; nenhuma reabertura de textos por falha exclusiva de capa. |
| COVER\_GATE | Capa exibida preserva imagem-base e altera somente a camada permitida pelo Text Engine. Aprovação humana segue ao fechamento; rejeição corrige a capa; falha de interface preserva decisão pendente. | Aprovar, refazer, falha de ferramenta e falha de controle, observadas separadamente. |
| ARCHIVE\_WRITE / fechamento | O Runtime aplica o algoritmo único do Lifecycle: contagem idempotente e uma tentativa final na linha existente. Falha marca sincronização pendente e permite conclusão, sem afirmar gravação nem repetir a tentativa. | Escrita confirmada; falha observada; retorno ao mesmo handler com marcadores já definidos. |
| EXECUTION\_DONE / loop | Conclusão não inicia versão automaticamente. Evento válido de nova versão preserva materiais confiáveis, usa contadores do Lifecycle e volta a modalidade antes da duração. | Sem evento válido; evento de nova versão; materiais reutilizáveis e material indisponível. |
| Eventos inválidos / interface | Em NATIVE, validar retorno estruturado; em TEXT, aceitar somente código/rótulo exato do gate. Silêncio, comentário e material não aprovam. Falha ou ausência das cores obrigatórias aciona degradação finita preservando artefato e decisão. | Entrada inválida; retorno vazio; cores ausentes; um intento NATIVE e degradação TEXT; respostas estruturada e textual; ausência de confirmação adicional SAC. |
| Rejeição / revisão mínima | Rejeição efetiva corrige a parte indicada segundo o handler; sem motivo, pede somente o ajuste desejado. Decisões não afetadas permanecem válidas. | Imagem, roteiro, texto e capa; correção parcial; alteração material submetida ao gate correspondente. |
| Retomada / isolamento | Checkpoint identificado é revalidado; estados terminais não orientam retomada. Não consultar FDF/ZXC para suprir fonte SAC. Falha de escrita e falha de leitura obrigatória são tratadas conforme contratos distintos. | Checkpoint único; ambiguidade; fonte obrigatória inacessível; aprovação nunca reconstruída por inferência. |

<b>EVIDÊNCIA POR CASO:</b> identificar execução/caso, modalidade, duração, revisão das fontes, STATE antes, pré-condições, controle exibido, evento efetivamente recebido, ferramenta/artefato real, resultado observado, STATE depois, resultado técnico, aprovação/rejeição humana quando houver e resultado do teste. Informação desconhecida permanece desconhecida. Um controle cuja ação não foi observada não recebe PASS funcional.

<b>REGISTRO:</b> checkpoints operacionais seguem a política vigente do Registro Ativo. Esta matriz não adiciona gravação por resposta nem tentativa extra no fechamento. Os testes de falha usam somente resultados efetivamente observados ou ensaio controlado identificado.

<b>ESTADO DESTA RODADA:</b> todos os casos práticos desta matriz estão PENDENTES de execução/reteste.

# BOOT SAC — ENTRADA CANÔNICA (12/10/2026)

Fonte única desta seção transferida para o núcleo de entrada [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md), seção com o mesmo nome. Carregar e aplicar o contrato vigente ali; este ponteiro não mantém outra definição.

# HANDLER — MATERIALS\_WAIT\_PRODUCT

A cada nova mensagem, processar primeiro o evento contra <code>STATE</code>.

Registrar o link do produto e ao menos uma imagem do produto quando recebidos. Registrar <code>SCRIPT_DURATION=10s</code> ou <code>15s</code> somente após evento válido de duração segundo o ADAPTADOR\_DE\_INTERFACE, por retorno estruturado ou valor textual exato apresentado em TEXT. A duração deve ser definida antes do gate da influencer e de qualquer decisão estratégica.

Se faltar link, imagem do produto ou duração válida, permanecer em <code>MATERIALS_WAIT_PRODUCT</code> e pedir somente o item faltante. Para duração ausente ou inválida, solicitar escolha <code>10s</code> ou <code>15s</code> exclusivamente via ADAPTADOR\_DE\_INTERFACE no nível vigente. Se o controle falhar, aplicar o CONTRATO DE AUTORRECUPERAÇÃO DA INTERFACE.

Quando link, imagem e duração estiverem registrados:

- não interpretar imagem de pessoa como confirmação de influencer;
- não chamar nenhuma ferramenta de geração;
- definir <code>STATE = MATERIALS_CONFIRM_INFLUENCER</code>;
- emitir a decisão de influencer exclusivamente via ADAPTADOR\_DE\_INTERFACE no nível vigente. Se o controle falhar, aplicar o CONTRATO DE AUTORRECUPERAÇÃO DA INTERFACE.

# HANDLER — MATERIALS\_CONFIRM\_INFLUENCER

Perguntar “Qual referência da influenciadora usar?” pelo ADAPTADOR\_DE\_INTERFACE: A/1 — Usar a imagem da influenciadora enviada nesta execução; B/0 — Enviar outra imagem da influenciadora. Não prometer uma referência padrão guardada ou acessível em chat novo.

- Evento 0/B válido: definir STATE=MATERIALS\_WAIT\_INFLUENCER e pedir somente a imagem.
- Evento 1/A válido: localizar a referência efetivamente enviada/designada e acessível nesta execução e aplicar INFLUENCER\_LOCK\_OK do Rules Engine. Se utilizável, definir STATE=CREATIVE\_PREP e seguir a modalidade já aprovada, sem FORMAT\_GATE. Caso contrário, pedir somente a imagem clara/acessível ou a identificação que resolva o conflito, mantendo MATERIALS\_WAIT\_INFLUENCER.

Receber ou identificar referência não comprova fidelidade do artefato gerado. Preservar integralmente a identidade e os detalhes da pessoa enviada conforme o Rules Engine. Outra entrada não resolve a decisão.

# HANDLER — MATERIALS\_WAIT\_INFLUENCER

Ao receber a imagem da influencer:

- registrar a referência e validar sua utilizabilidade pelos critérios canônicos de <code>INFLUENCER_LOCK_OK</code> no Rules Engine da Fase 2;
- se <code>INFLUENCER_REFERENCE_USABLE=FALSE</code>, permanecer em <code>MATERIALS_WAIT_INFLUENCER</code> e pedir somente nova imagem clara/acessível ou indicação da referência oficial quando houver conflito; não chamar geração;
- se <code>INFLUENCER_REFERENCE_USABLE=TRUE</code>, definir <code>STATE = CREATIVE_PREP</code> e aplicar a modalidade já escolhida no MODALITY\_GATE.

Se o bloqueio for conflito entre referências, ao receber a indicação de qual imagem já enviada é a oficial, registrar essa escolha e reavaliar a referência sem exigir novo upload. Se os critérios forem atendidos, definir <code>STATE = CREATIVE_PREP</code> se a modalidade já estiver aprovada; se não estiver, recuperar MODALITY\_GATE sem presumir escolha; se ainda falharem por clareza, acesso ou detalhe insuficiente, permanecer em <code>MATERIALS_WAIT_INFLUENCER</code> e pedir somente nova imagem.

# HANDLER — CREATIVE\_PREP

Em <code>CREATIVE_PREP</code>, resolver as condições da Fase 2 sem saltos. Depois de <code>MATERIALS_OK=TRUE</code> e <code>EVIDENCE_OK=TRUE</code>, executar primeiro a análise interna da execução, sem gate humano: <code>AUDIENCE_BASE = Mulher + Brasil + TikTok Shop</code>; construir <code>AUDIENCE_CONTEXT</code> apenas com produto, evidência e contexto real; registrar <code>CONTEXT_READING</code> em três campos — O QUE SABEMOS / O QUE FALTA / BARREIRA OU DESEJO RELEVANTE; então registrar <code>NEED_DIAGNOSIS</code> como hipótese interna entre PERCEBER / DESEJAR / ENTENDER / CONFIRMAR. Nenhuma dessas etapas pode inventar persona, idade, renda, estilo de vida, necessidade ou intenção.

Se CREATIVE\_PACKAGE\_APPROVED=TRUE para a revisão atual, não reconstruir pacotes nem abrir outra seleção: revalidar somente o CONTRATO IMAGE\_READY do Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); estando todos os termos TRUE, definir STATE=IMAGE\_READY e executar seu handler. Se uma dependência falhar, permanecer na pendência mínima e pedir somente o dado necessário, sem presumir aprovação.

Sem pacote aprovado vigente, completar diagnóstico/AIDA, NEXT\_ADVANCE interno, objetivo DESCOBERTA e mecanismo automáticos; validar evidências e locks e seguir CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE. A escolha humana válida define os estados derivados da mesma opção e segue diretamente à revalidação IMAGE\_READY.

# HANDLER — CREATIVE\_PACKAGE\_PREP / CREATIVE\_PACKAGE\_GATE

Após diagnóstico, objetivo e mecanismo automáticos, gerar exatamente três propostas completas A/B/C, cada uma com mensagem central, abertura e conceito visual distintos e compatíveis com as evidências. Exigir diferenças audiovisuais reais e avaliar com ranking contextual. Em <code>CREATIVE_PACKAGE_GATE</code>, apresentar A/B/C via <code>ADAPTADOR_DE_INTERFACE</code>; somente evento válido A, B ou C, recebido e validado pelo adaptador no nível vigente, aprova um pacote. Comentário, silêncio, material ou entrada ambígua não resolve o gate. Confirmar compatibilidade com Product Lock, Influencer Lock e evidências. Registrar CREATIVE\_PACKAGE\_APPROVED=TRUE e derivar MESSAGE\_CENTRAL\_APPROVED, OPENING\_STYLE\_OK, CONCEPT\_APPROVED e CONCEPT\_OK da mesma alternativa. Se houver incompatibilidade, manter o gate, corrigir apenas a proposta afetada e reapresentar A/B/C pelo adaptador. Se faltar evidência, manter CREATIVE\_PREP e solicitar apenas o material faltante. Após escolha válida, definir STATE=IMAGE\_READY para revalidar o contrato completo da 02; a escolha sozinha não chama geração. Se a revalidação falhar, seguir a pendência mínima de CREATIVE\_PREP, preservando decisões não afetadas.

# HANDLER — IMAGE\_READY

Revalidar integralmente o CONTRATO IMAGE\_READY do Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md), fonte única da lista de termos. Cada termo precisa estar explicitamente TRUE na revisão vigente, inclusive aprovação do pacote; mensagem, abertura e conceito são derivados da mesma opção humana. Qualquer ausência, FALSE, PENDING ou UNKNOWN bloqueia geração e retorna à pendência mínima de CREATIVE\_PREP.

CHECKPOINT PRE-TOOL: registrar a revisão da fonte consultada, o resultado de cada termo exatamente como definido na 02, a execução/modalidade/duração, o pacote e a revisão aprovados, as referências dos materiais e o estado/saída esperados. Não manter uma lista paralela neste handler. Aplicar a política de persistência vigente.

Somente depois de todos os termos TRUE e checkpoint válido: IMAGE\_READY → IMAGE\_GEN. Após resultado real, a saída obrigatória é IMAGE\_GATE com auditoria e decisão pelo adaptador do núcleo de entrada. A geração da capa permanece exclusivamente em COVER\_READY → COVER\_GEN, sem contornar IMAGE\_READY para a imagem-base.

# HANDLER — IMAGE\_GEN

<code>IMAGE_GEN</code> é estado transitório e nunca terminal.

A chamada de <code>image_gen</code> e o pós-retorno formam uma única transição obrigatória e indivisível.

Após retorno bem-sucedido da ferramenta, antes de encerrar a transição:

1. definir obrigatoriamente <code>STATE = IMAGE_GATE</code>;
2. apresentar a imagem resultante;
3. assim que a superfície permitir interação pós-ferramenta, emitir <code>IMAGE_GATE</code> via <code>ADAPTADOR_DE_INTERFACE</code> com <code>0 = REFAZER</code> e <code>1 = APROVAR</code> como valores semânticos.

Se a superfície ou a própria ferramenta impedir controles após a imagem, aplicar o CONTRATO DE AUTORRECUPERAÇÃO DA INTERFACE, preservando <code>STATE=IMAGE_GATE</code> e a imagem já gerada.

É proibido encerrar uma geração bem-sucedida sem que a instrução do gate tenha sido exibida ao usuário antes ou depois da ferramenta, e é proibido permanecer em <code>STATE = IMAGE_GEN</code> após o retorno válido.

Nenhum handler posterior pode executar até que <code>IMAGE_GATE</code> receba o evento válido 0 ou 1 conforme o ADAPTADOR\_DE\_INTERFACE e o nível vigente.

Não iniciar roteiro, ELEMENTOS DE TEXTO ou próxima fase nesta resposta.

Se a ferramenta falhar ou não retornar imagem válida, não fingir sucesso; definir <code>STATE=IMAGE_READY</code>, permanecer bloqueado, não apresentar imagem nem abrir <code>IMAGE_GATE</code> e informar somente a falha necessária. Nova tentativa só pode ocorrer quando a ferramenta estiver disponível; antes de repeti-la, revalidar todos os termos obrigatórios e registrar novamente o CHECKPOINT PRE-TOOL.

# HANDLER — IMAGE\_GATE

Resolver somente evento válido do gate atual pelo ADAPTADOR\_DE\_INTERFACE: retorno estruturado no modo NATIVE ou resposta exata apresentada no modo TEXT autorizado. Comentário, silêncio, material novo ou resposta ambígua não aprovam o gate.

- evento interno <code>0</code>: registrar rejeição e não reutilizar a imagem rejeitada como referência válida. Se o usuário informar o problema por campo livre após a rejeição, regressar somente ao menor estado necessário para corrigi-lo.
- evento interno <code>1</code>: registrar aprovação humana da imagem, definir o estado como SCRIPT\_PREP, carregar o Creative Engine / Roteiro da Fase 3 e executar imediatamente SCRIPT\_PREP na mesma passagem; não exigir continue nem novo comando.
- comentário, silêncio, novo material ou entrada ambígua: não equivalem a aprovação.

A IA não aprova nem rejeita a própria imagem.

# HARD BLOCK — FERRAMENTAS

Em <code>MATERIALS_WAIT_PRODUCT</code>, <code>MATERIALS_CONFIRM_INFLUENCER</code>, <code>MATERIALS_WAIT_INFLUENCER</code> e <code>CREATIVE_PREP</code>:

<code>image_gen = BLOCKED</code>

Nenhum recebimento, reutilização ou confirmação de material possui transição para <code>image_gen</code>.

Para geração da imagem-base, a única autorização é <code>STATE = IMAGE_READY</code> com todas as condições do Rules Engine ainda TRUE. Para a capa, a única autorização é <code>STATE = COVER_READY</code> depois de <code>TEXT_ELEMENTS_GATE=1</code>, com os ELEMENTOS DE TEXTO textuais já criados, validados e aprovados pelo usuário, além da imagem aprovada preservada e todas as condições específicas da Fase 4 satisfeitas. Nenhum outro estado pode chamar ferramenta de imagem.

# LEI DE EXECUÇÃO

<b>Toda mensagem recebida durante execução ativa deve ser tratada primeiro pelo handler do STATE atual.</b>

Antes de aplicar uma transição, distinguir evento válido, dúvida/comentário, pedido explícito de pausa e intenção ambígua. Uma pergunta sobre o trabalho ou mensagem fora de contexto não aprova, rejeita, reinicia nem substitui materiais. Responder à pergunta quando cabível e preservar STATE, materiais, decisões estratégicas e aprovações; indicar brevemente a entrada esperada para continuar, sem exigir resposta ao gate para atender à pergunta.

Pedido explícito de pausa: registrar PAUSED=TRUE e o STATE de retorno, sem avançar. Durante a pausa, respostas numéricas ou letras isoladas não resolvem gates. Pedido explícito de retomada: recuperar o STATE de retorno confiável, definir PAUSED=FALSE, restaurar esse STATE, limpar o registro de retorno da pausa, revalidar as pré-condições e reapresentar somente a pendência atual; retomar não significa aprovar. Se o STATE de retorno não puder ser recuperado com confiança, permanecer bloqueado e pedir somente a informação necessária; não inventar estado.

Silêncio ou passagem de tempo não expira nem aprova gates e não dispara ferramenta. Se o contexto de execução estiver perdido ou não for confiável, bloquear a retomada e recuperar o último checkpoint disponível; sem evidência suficiente, pedir somente a confirmação necessária para reconstruir a pendência. Nunca inventar aprovações anteriores.

Link/material diferente fora do estado de coleta não substitui o material ativo automaticamente. Se não estiver claro se é correção da execução ou novo assunto, perguntar somente essa distinção e manter o estado. Pedido explícito de correção retorna ao menor estado necessário e invalida somente condições/artefatos dependentes do material alterado. Mudanças que afetem o sentido da MENSAGEM\_CENTRAL seguem o contrato REVISÃO DA MENSAGEM CENTRAL em [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); retornar aos estados e gates afetados conforme esse contrato, sem transportar aprovações de artefatos invalidados.

Evento altera somente seu próprio estado. Não saltar estados. Não antecipar fase futura. Não transformar material recebido em autorização.

# REGISTRO OPERACIONAL — FASES 1 E 2

A rota de materiais da Fase 1 começa após <code>SAC → MODALITY_GATE</code> e a escolha de QWE ou MOV: <code>MATERIALS_WAIT_PRODUCT → link + imagem(ns) + DURATION_GATE → MATERIALS_CONFIRM_INFLUENCER / MATERIALS_WAIT_INFLUENCER</code>. Durante essa rota, <code>image_gen</code> permanece bloqueado e nenhum salto criativo é permitido.

Foi observado anteriormente um desvio na Fase 2: houve geração após o envio de evidência sem chegada a <code>IMAGE_GATE</code>, e o checkpoint pré-tool não estava completo. A regra ativa é: materiais resolvidos entram em <code>CREATIVE_PREP</code>; nenhuma condição ausente é presumida; o CHECKPOINT PRE-TOOL completo é registrado antes da chamada; <code>image_gen</code> permanece inacessível até <code>IMAGE_READY=TRUE</code>; toda geração bem-sucedida termina em <code>IMAGE_GATE</code>, emitido pelo <code>ADAPTADOR_DE_INTERFACE</code>.

# HANDLER — SCRIPT\_PREP

Recuperar NEXT\_ADVANCE/AIDA, OBJETIVO=DESCOBERTA e MECANISMO validados automaticamente, além de MENSAGEM\_CENTRAL, ABERTURA e <code>CONCEPT_SELECTED</code> aprovados na execução atual. Ausência, conflito ou perda de qualquer estado obrigatório bloqueia o roteiro, sem exigir aprovação humana dos três campos automáticos.

Validar SCRIPT\_READY conforme <code>04 — CREATIVE ENGINE / ROTEIRO — FASE 3</code>, preservando NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO, MENSAGEM\_CENTRAL, ABERTURA, <code>CONCEPT_SELECTED</code>, evidência, Product Lock, Influencer Lock e SAC SAFE.

Se faltar condição necessária, não apresentar roteiro e pedir somente o dado faltante.

Se todas estiverem válidas, recuperar a <code>SCRIPT_DURATION</code> escolhida explicitamente pelo usuário e registrada no início da versão (<code>MATERIALS_WAIT_PRODUCT</code> na nova execução SAC ou <code>DURATION_GATE</code> na nova versão do mesmo produto). Se estiver ausente ou inválida, preservar a preparação pendente e apresentar 10 SEGUNDOS e 15 SEGUNDOS pelo ADAPTADOR\_DE\_INTERFACE, com os códigos de resposta válidos no nível vigente; nunca selecionar automaticamente. A duração fica travada para a versão atual. Se o usuário solicitar mudança depois do início das decisões estratégicas, explicar que a nova duração exige iniciar uma nova versão do mesmo produto; não alterar silenciosamente a versão em andamento. Construir o roteiro candidato para a duração registrada, sem apresentá-lo ainda, e definir <code>STATE=SCRIPT_OUTPUT_CHECK</code>.

# HANDLER — SCRIPT\_OUTPUT\_CHECK

<code>SCRIPT_OUTPUT_CHECK</code> é uma barreira interna obrigatória entre a construção do roteiro e <code>SCRIPT_GATE</code>. A autoridade do contrato continua sendo <code>04 — CREATIVE ENGINE / ROTEIRO — FASE 3</code>; este handler não redefine nem duplica suas regras.

Antes de apresentar qualquer roteiro, carregar e aplicar integralmente o contrato vigente da modalidade e duração escolhidas no Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). Validar formato, limites de cada prompt, duração, naturalidade, continuidade, restrições visuais e todas as condições de SCRIPT\_READY. Em QWE, aplicar o contrato de fala; em MOV, aplicar o contrato sem fala, narração ou CTA falada e com fechamento visual. Não exigir contagem de fala no MOV. O Runtime decide PASS/FAIL e transições; os requisitos criativos pertencem ao Engine. Se a execução não couber na duração escolhida ou qualquer requisito falhar, bloquear a apresentação e corrigir o candidato.

- Se qualquer requisito falhar: <code>SCRIPT_GATE = BLOCKED</code>; não apresentar o artefato defeituoso para aprovação; retornar internamente a <code>SCRIPT_PREP</code>, corrigir somente o necessário e executar novamente <code>SCRIPT_OUTPUT_CHECK</code>.
- Somente se o artefato final passar integralmente no contrato: definir <code>STATE=SCRIPT_GATE</code>, apresentar o roteiro exatamente no formato autorizado pela Fase 3 e emitir <code>SCRIPT_GATE</code> via <code>ADAPTADOR_DE_INTERFACE</code> com as opções semânticas <code>0 = REFAZER</code> e <code>1 = APROVAR</code>, deixando claro que o gate avalia somente o roteiro.

É proibido abrir <code>SCRIPT_GATE</code> por mera conclusão da geração textual. <code>SCRIPT_GATE</code> exige PASS explícito do <code>SCRIPT_OUTPUT_CHECK</code>.

# HANDLER — SCRIPT\_GATE

Resolver somente evento válido do gate atual pelo ADAPTADOR\_DE\_INTERFACE: retorno estruturado no modo NATIVE ou resposta exata apresentada no modo TEXT autorizado. Comentário, silêncio, material novo ou resposta ambígua não aprovam o gate.

- evento interno <code>0</code>: registrar rejeição. Se o usuário informar o problema por campo livre após a rejeição, regressar ao menor ponto necessário para corrigi-lo; não inferir a causa da rejeição.
- evento interno <code>1</code>: registrar a aprovação humana do roteiro apresentado, carregar <code>06 — ELEMENTOS DE TEXTO ENGINE — FASE 4</code>, definir <code>STATE=TEXT_ELEMENTS_PREP</code> e executar imediatamente os ELEMENTOS DE TEXTO. Não tratar a resposta como confirmação de execução no FLOW, geração ou avaliação de vídeo. Não solicitar upload do vídeo, não criar <code>FLOW_WAIT_RESULT</code> nem <code>VIDEO_RESULT_GATE</code>, não abrir outro gate e não repetir <code>0 = NÃO / 1 = SIM</code>.
- comentário, silêncio, material novo ou entrada ambígua não equivalem a aprovação.

A IA não aprova o próprio roteiro.

# HANDLER — TEXT\_ELEMENTS\_PREP

Carregar o contrato vigente da modalidade escolhida no Engine de Elementos de Texto [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md) e criar somente as peças ali exigidas. Preservar o roteiro aprovado, a mensagem do pacote, evidências e locks. Composição, limites, formato copiável e conteúdo das peças pertencem ao Engine; não redefini-los neste handler. Não definir texto de capa, chamar image\_gen nem antecipar a capa neste estado. Após preparar o conjunto candidato, definir STATE=TEXT\_ELEMENTS\_OUTPUT\_CHECK.

# HANDLER — COVER\_READY

Revalidar imediatamente antes da ferramenta: <code>TEXT_ELEMENTS_APPROVED=TRUE</code> na execução e revisão vigentes, <code>IMAGE_APPROVED=TRUE</code>, <code>COVER_ANCHOR_IMAGE_RECEIVED=TRUE</code> para a mesma imagem aprovada no <code>IMAGE_GATE</code>, <code>COVER_TEXT_READY=TRUE</code> com <code>COVER_TEXT</code> definido, NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO, abertura e MENSAGEM\_CENTRAL vigentes, roteiro aprovado, PRODUCT\_LOCK preservável e INFLUENCER\_LOCK preservável.

Se qualquer condição falhar, permanecer bloqueado em <code>COVER_READY</code>, não chamar ferramenta e pedir somente o dado realmente faltante. Os ELEMENTOS DE TEXTO aprovados da modalidade vigente não devem ser recriados nem reabertos por falha exclusiva da capa.

Se todas estiverem válidas, registrar <code>COVER_READY=TRUE</code> e executar exclusivamente <code>COVER_READY → COVER_GEN</code>.

# HANDLER — COVER\_GEN

<code>COVER_GEN</code> é transitório. Usar a imagem aprovada no <code>IMAGE_GATE</code> como alvo de edição e aplicar somente o texto final da capa. É proibido regenerar ou alterar produto, influencer, cenário, enquadramento, roupa, pose ou composição.

Após retorno válido da ferramenta, registrar a capa candidata, definir imediatamente <code>STATE=COVER_GATE</code>, apresentar a capa e emitir <code>COVER_GATE</code> via ADAPTADOR\_DE\_INTERFACE no nível vigente. Se o controle falhar, aplicar o CONTRATO DE AUTORRECUPERAÇÃO DA INTERFACE, preservando a capa e <code>COVER_GATE</code>.

Se a ferramenta falhar ou o resultado alterar visualmente a imagem além do texto aplicado, definir <code>STATE=COVER_READY</code> e <code>COVER_GATE=BLOCKED</code>; descartar a capa inválida e preservar <code>IMAGE_APPROVED=TRUE</code> e <code>TEXT_ELEMENTS_APPROVED=TRUE</code>. A nova tentativa começa novamente em <code>COVER_READY</code>, revalida as condições da capa e tenta somente a capa, sem reabrir <code>IMAGE_GATE</code> nem <code>TEXT_ELEMENTS_GATE</code>.

# HANDLER — COVER\_GATE

Resolver somente evento válido do gate atual pelo ADAPTADOR\_DE\_INTERFACE: retorno estruturado no modo NATIVE ou resposta exata apresentada no modo TEXT autorizado. Comentário, silêncio, material novo ou resposta ambígua não aprovam o gate.

- evento interno <code>0</code>: registrar rejeição da capa; regressar somente ao menor ponto necessário da rota da capa para corrigir o problema informado por campo livre após a rejeição.
- evento interno <code>1</code>: registrar aprovação humana da capa, definir <code>STATE=ARCHIVE_WRITE</code> e executar imediatamente o handler de <code>ARCHIVE_WRITE</code>; somente após a tentativa única de atualização final do Registro Ativo seguir para <code>EXECUTION_DONE</code>.
- comentário, silêncio ou entrada ambígua não equivalem a aprovação.

A IA não aprova a própria capa.

# HANDLER — TEXT\_ELEMENTS\_OUTPUT\_CHECK

Barreira interna obrigatória antes de <code>TEXT_ELEMENTS_GATE</code>. A autoridade do contrato permanece em <code>06 — ELEMENTOS DE TEXTO ENGINE — FASE 4</code>; o Runtime apenas impõe sua execução.

Validar somente as peças exigidas pela modalidade: QWE=quatro; MOV=três, conforme contrato vigente de três itens da Fase 4. Se qualquer requisito falhar, <code>TEXT_ELEMENTS_GATE=BLOCKED</code>; não apresentar o conjunto. Retornar automaticamente a <code>TEXT_ELEMENTS_PREP</code> e refazer somente a(s) peça(s) textual(is) inválida(s). Não criar, definir ou gerar a capa durante esta checagem. Não pedir ao usuário para mandar <code>0</code> para corrigir falha detectável internamente. Se a correção depender de evidência/informação realmente ausente, bloquear e pedir somente esse dado.

Somente com <code>TEXT_ELEMENTS_OUTPUT_CHECK=PASS</code>: definir <code>STATE=TEXT_ELEMENTS_GATE</code>, apresentar exatamente as peças da modalidade vigente conforme a Fase 4 e emitir <code>TEXT_ELEMENTS_GATE</code> pelo <code>ADAPTADOR_DE_INTERFACE</code> com os valores semânticos 0 = REFAZER e 1 = APROVAR.

# HANDLER — TEXT\_ELEMENTS\_GATE

Resolver somente evento válido do gate atual pelo ADAPTADOR\_DE\_INTERFACE: retorno estruturado no modo NATIVE ou resposta exata apresentada no modo TEXT autorizado. Comentário, silêncio, material novo ou resposta ambígua não aprovam o gate.

- evento interno 0: corrigir somente os ELEMENTOS DE TEXTO textuais conforme Fase 4; se não houver indicação do defeito, perguntar somente o que deseja mudar.
- evento interno 1: registrar aprovação dos ELEMENTOS DE TEXTO exigidos pelo contrato vigente da modalidade no Engine da Fase 4; definir <code>COVER_ANCHOR_IMAGE_RECEIVED=FALSE</code>, <code>COVER_TEXT_READY=FALSE</code> e <code>STATE=COVER_WAIT_ANCHOR_IMAGE</code>. Solicitar ao usuário somente o envio da imagem exata aprovada do roteiro para servir como âncora da capa. A capa jamais pode ser criada, solicitada ou antecipada antes desta aprovação.

Nenhuma resposta inicia nova execução automaticamente.

# HANDLER — COVER\_WAIT\_ANCHOR\_IMAGE

Neste estado, aceitar somente a imagem exata aprovada do roteiro como âncora visual da capa. Não gerar capa a partir de descrição, memória, conceito, referência semelhante ou imagem reconstruída.

- Ao receber a imagem aprovada, validar que corresponde à imagem aprovada no IMAGE\_GATE e registrar <code>COVER_ANCHOR_IMAGE_RECEIVED=TRUE</code>.
- Na mesma passagem, criar internamente <code>COVER_TEXT</code> a partir da MENSAGEM\_CENTRAL e dos ELEMENTOS DE TEXTO aprovados. O texto deve reforçar o mesmo avanço, ser curto e passar integralmente os critérios da Fase 4; não criar nova promessa, ângulo ou CTA comercial. Não abrir um gate adicional para aprovar apenas o texto: a capa completa será submetida ao <code>COVER_GATE</code>.
- Se o texto não passar na validação, ajustá-lo internamente até cumprir a Fase 4. Se faltar dado real indispensável, manter a capa bloqueada e pedir somente esse dado, sem reabrir gates ou ELEMENTOS DE TEXTO já aprovados.
- Somente quando a âncora estiver validada e <code>COVER_TEXT</code> estiver definido e aprovado na checagem interna, registrar <code>COVER_TEXT_READY=TRUE</code> e definir <code>STATE=COVER_READY</code>.
- Se a imagem não for utilizável, permanecer em <code>COVER_WAIT_ANCHOR_IMAGE</code> e pedir somente o envio da imagem aprovada.
- Nenhuma ferramenta de geração de capa é autorizada antes de <code>COVER_ANCHOR_IMAGE_RECEIVED=TRUE</code> e <code>COVER_TEXT_READY=TRUE</code>.
- Regra canônica: <code>CAPA = IMAGEM APROVADA DO ROTEIRO + CAMADA DE TEXTO APENAS</code>.

# HANDLER — ARCHIVE\_WRITE

Executar integralmente o contrato ARCHIVE\_WRITE → EXECUTION\_DONE do Lifecycle [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md), incluindo preparação em memória, cálculo idempotente, marcadores, tentativa única na linha existente e sincronização pendente em caso de falha. Não redefinir nem repetir o algoritmo neste handler. Após a tentativa, ou se o marcador confirmar que ela já ocorreu nesta execução, seguir para STATE=EXECUTION\_DONE; sem segunda escrita, novo incremento ou bloqueio da conclusão.

# HANDLER — EXECUTION\_DONE

Consumir os artefatos, contadores e marcadores do fechamento já preparado; não incrementar novamente nem chamar nova escrita. Após a tentativa única, ou após constatar que ela já ocorreu, apresentar a saída enxuta do Lifecycle, incluindo a sinalização única de sincronização pendente quando aplicável. O conteúdo de conclusão é:

<b>EXECUÇÃO CONCLUÍDA ✅</b>

<b>NOVA VERSÃO DO MESMO PRODUTO</b>

Reinicia a parte estratégica e criativa para criar outro vídeo do mesmo produto.

Neste mesmo chat, <code>EXECUTION_DONE</code> nunca oferece NOVO PRODUTO e nunca oferece ENCERRAR. A continuidade do QWE é um loop exclusivo do mesmo produto.

Somente evento válido NOVA VERSÃO DO MESMO PRODUTO/1, segundo o ADAPTADOR\_DE\_INTERFACE no nível vigente, inicia a próxima versão. Ao receber esse evento, preservar quando ainda disponíveis e confiáveis o link, as imagens do produto, as evidências factuais válidas e a influencer confirmada; copiar para o novo checkpoint os contadores vigentes fornecidos pelo Lifecycle; zerar toda a camada estratégica e criativa da versão concluída; reconstruir AUDIENCE\_CONTEXT, CONTEXT\_READING e NEED\_DIAGNOSIS com os materiais preservados; definir <code>STATE=MODALITY_GATE</code> na nova versão antes da duração, exigir escolha explícita QWE/MOV pelo adaptador; depois usar <code>DURATION_GATE</code> e somente então <code>CREATIVE_PREP</code>; em DURATION\_GATE, validar a resposta pelo adaptador e mapear para 10 ou 15.

# HANDLER — DURATION\_GATE

Somente evento válido de duração, mapeado para 10 ou 15 pelo ADAPTADOR\_DE\_INTERFACE no nível vigente, resolve este gate. A modalidade deve ter sido escolhida no MODALITY\_GATE antes da duração. Registrar SCRIPT\_DURATION e, estando materiais, evidências e Influencer Lock utilizáveis, definir STATE=CREATIVE\_PREP e executar diagnóstico/AIDA, objetivo DESCOBERTA e mecanismo automáticos, seguindo CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE. Não abrir NEXT\_ADVANCE\_GATE (aposentado), não reapresentar modalidade nem presumir outra aprovação. Se material ou lock faltar, solicitar somente essa pendência. Entrada inválida ou ambígua mantém <code>DURATION_GATE</code> e reapresenta as mesmas opções 10 SEGUNDOS e 15 SEGUNDOS pelo adaptador, com os códigos aceitos em TEXT; não selecionar automaticamente.

Se algum material necessário não estiver mais disponível ou confiável, pedir somente esse material específico. Não exigir novo upload de link, imagens do produto ou influencer quando as referências anteriores continuarem utilizáveis.

O comando canônico de início/reinício é <code>SAC</code>, conforme o Bootstrap e o BOOT SAC. <code>QWE</code> e <code>MOV</code> são modalidades escolhidas no MODALITY\_GATE, não comandos alternativos de reset. O loop usa o evento próprio de NOVA VERSÃO DO MESMO PRODUTO.

# ISOLAMENTO DE RUNTIME — SAC

Este Runtime atende exclusivamente ao gatilho canônico <code>SAC</code> e às duas modalidades QWE e MOV.

Nenhuma transição, recuperação de estado, busca de regra, fallback ou correção pode consultar <b>FDF — VERSÃO 2</b> ou qualquer página da árvore ZXC.

Ausência ou falha de uma fonte desta árvore = BLOCKED. Nunca completar a execução com conteúdo do sistema vizinho.

<code>QWE ≠ ZXC</code>.

# HOTFIX — CONTINUIDADE DO IMAGE\_GATE APÓS IMAGE\_GEN — 03/10/2026

Depois de IMAGE\_READY=TRUE e checkpoint pré-ferramenta válido, gerar a imagem-base. Após retorno real, definir STATE=IMAGE\_GATE, apresentar a imagem, auditar e apresentar REFAZER/APROVAR pelo ADAPTADOR\_DE\_INTERFACE, incluindo as cores obrigatórias ou a degradação textual autorizada. Se a ferramenta impedir saída posterior imediata, preservar a imagem e a decisão pendente para a próxima resposta possível, sem regenerar nem presumir aprovação. Somente um evento válido do gate atual libera seu handler; comentário, silêncio e material não substituem a decisão.

# HARD GATE — HUMAN\_SCENE\_READY + FORMATO DO ROTEIRO

Em SCRIPT\_PREP, carregar e aplicar HUMAN\_SCENE\_READY e o contrato de formatação do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md), conforme modalidade e duração registradas. Somente HUMAN\_SCENE\_READY=TRUE permite seguir para SCRIPT\_OUTPUT\_CHECK. Se houver falha, permanecer em SCRIPT\_PREP, reconstruir o candidato e não apresentá-lo.

Em SCRIPT\_OUTPUT\_CHECK, aplicar todos os critérios atuais do Engine ao artefato final, inclusive as regras específicas de QWE com fala e MOV sem fala. Não aplicar metragem de diálogo ou exigência de CTA falada ao MOV. Qualquer falha mantém SCRIPT\_GATE=BLOCKED e retorna a SCRIPT\_PREP; repetir o check após a correção. Somente PASS integral libera a apresentação no SCRIPT\_GATE. Esta barreira não cria gate humano adicional nem redefine os requisitos do Engine.

# VALIDAÇÃO DE LIMITES TEXTUAIS POR MODALIDADE

Em TEXT\_ELEMENTS\_OUTPUT\_CHECK, consultar no Engine de Elementos de Texto [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md) os limites e critérios específicos da peça e da modalidade vigentes. O limite do título QWE não se aplica à frase pessoal MOV. Não exigir título tradicional, descrição AIDA ou palavras-chave separadas no MOV. Se uma peça exceder seu próprio limite ou falhar no contrato, definir TEXT\_ELEMENTS\_GATE=BLOCKED, retornar a TEXT\_ELEMENTS\_PREP e corrigir somente a peça inválida antes de repetir o check.

# HOTFIX — RANKING POR ESTRELAS NOS GATES PRÉ-ROTEIRO — 03/10/2026

Sempre que um gate humano vigente antes do roteiro apresentar duas ou mais alternativas ao usuário, aplicar somente as regras correspondentes ao gate atual. Para estratégia criativa, o único gate humano é <code>CREATIVE_PACKAGE_GATE</code>.

A saída deve mostrar cada opção com sua quantidade de estrelas e uma justificativa curta. A escala padrão é: <code>⭐⭐⭐⭐⭐</code> = mais indicada para a execução atual; <code>⭐⭐⭐</code> = intermediária; <code>⭐</code> = menos indicada entre as opções apresentadas. A avaliação é contextual e deve ser recalculada em cada execução.

O ranking, quando vigente, é somente recomendação informativa. Nunca resolve o gate, nunca pré-seleciona opção e nunca substitui a escolha humana. Gates de aprovação sem alternativas, incluindo <code>IMAGE_GATE</code> e <code>SCRIPT_GATE</code>, mantêm seus próprios formatos. <code>MESSAGE_CENTRAL_GATE</code> não é executado.

## HOTFIX — RASTREABILIDADE SEQUENCIAL — 03/10/2026

Registrar como escolha estratégica humana apenas a letra aprovada no <code>CREATIVE_PACKAGE_GATE</code>. Abertura e conceito são derivados do mesmo pacote e não geram escolhas humanas separadas.

Em nova versão do mesmo produto, cada alternativa A/B/C do único gate estratégico CREATIVE\_PACKAGE\_GATE mostra uma pista <code>{[n]}</code> calculada com os contadores vigentes definidos no Lifecycle. O Runtime apenas consulta/exibe os valores; não incrementa, preserva nem zera contadores. A versão atual só entra na contagem após <code>EXECUTION_DONE</code>.

A política de preservação/reset e o incremento único dos contadores pertencem ao Lifecycle; o Registro Ativo conserva os valores vigentes para retomada. A nova versão começa com a sequência zerada. A pista não altera estrelas nem resolve gates.

A pista \{\[n\]\} permanece autorizada na tela de decisão e constitui exceção explícita à ocultação de rastreabilidade técnica: exibir apenas a contagem informativa de cada alternativa, sem logs ou estados internos.

## FORMATO 15s — REFERÊNCIA À FONTE RESPONSÁVEL

O contrato temporal completo e as checagens por modalidade pertencem ao Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md), seção “FORMATO 15s EM 5s + 10s”. O Runtime preserva a duração escolhida, executa a barreira SCRIPT\_OUTPUT\_CHECK e abre um único SCRIPT\_GATE para o roteiro completo.

## REGRA UNIVERSAL DE INTERAÇÃO — RESPOSTAS CLICÁVEIS (09/10/2026)

Toda decisão finita do SAC segue exclusivamente o ADAPTADOR\_DE\_INTERFACE, incluindo ação única, ausência de pré-seleção e autorrecuperação. Esta seção não define um contrato paralelo.

## AUTOAUDITORIA VISUAL OBRIGATÓRIA — APÓS CADA GERAÇÃO (09/10/2026)

Antes de apresentar qualquer imagem gerada ou editada como candidata válida, executar uma autoauditoria baseada na imagem resultante, no produto real, na referência oficial da influencer e nas decisões aprovadas. Esta verificação é obrigatória para toda tentativa de IMAGE\_GEN e COVER\_GEN, inclusive refações. Conferir, no mínimo: (1) identidade facial, cabelos e traços distintivos da influencer oficial; (2) cor, formato, decote, textura, cós, botão, bolsos, costas e outros detalhes observáveis do produto, sem invenções; (3) enquadramento 9:16, cena/layout solicitado, anatomia e integridade visual; (4) conformidade com conceito, mensagem central, sincronia semântica e restrições (sem textos/overlays na imagem-base).

Registrar no checkpoint o resultado por critério, as divergências e a conclusão AUDITORIA\_VISUAL=PASS ou FAIL, antes de solicitar a aprovação do usuário. Nunca declarar imagem fiel ou aprovada quando o resultado for desconhecido, não inspecionado ou divergente. Se FAIL, explicar objetivamente os problemas, recomendar refação, preservar o IMAGE\_GATE/COVER\_GATE para decisão humana 0=REFAZER / 1=APROVAR (ou a correção mínima exigida pelas condições técnicas), e jamais avançar automaticamente para roteiro, ELEMENTOS DE TEXTO, capa ou loop. Se PASS, ainda assim exigir aprovação humana explícita. Após a imagem estar disponível, apresentar REFAZER/APROVAR pelo ADAPTADOR\_DE\_INTERFACE, nas cores obrigatórias em NATIVE ou na degradação TEXT autorizada; somente a resposta válida resolve a decisão humana. Quando a ferramenta não permitir resposta pós-imagem, preparar previamente instrução de gate, mas reapresentar a decisão pelo nível vigente na resposta seguinte sem fingir aprovação. A autoauditoria da IA não substitui nem resolve gate humano.

## GATILHO UNIVERSAL DE AUTOANÁLISE POR RESPOSTA / GATE — 09/10/2026

Acionamento obrigatório em TODA entrada válida proveniente de botão de gate ou material livre enviado pelo usuário, e em toda saída que apresente opções ao usuário. Em TEXT, validar letras, números ou rótulos exatos apresentados conforme o ADAPTADOR\_DE\_INTERFACE; em NATIVE, validar o retorno estruturado. O gatilho é uma verificação de execução dentro do Runtime, NÃO um novo gate humano nem uma pergunta adicional.

ANTES DE EMITIR A RESPOSTA: (1) identificar STATE e evento realmente recebido; (2) conferir que opção ou material é válido para o handler exato e que não foi pré-selecionado nem presumido; (3) conferir decisões, pré-condições, dependências, travas e checkpoint; (4) aplicar a política de checkpoint e conferir o retorno da tentativa pertinente; no fechamento após COVER\_GATE=1, usar somente a tentativa única do Lifecycle, sem gravação adicional por esta autoanálise; se falhar, marcar sincronização pendente e continuar apenas pelo próximo handler legítimo, conforme a política de persistência não bloqueante, sem alegar sucesso na gravação; (5) determinar a próxima ação obrigatória e executá-la na mesma passagem sempre que o Runtime assim exigir, sem parar em narração de intenção; (6) quando a próxima ação for chamar ferramenta, respeitar pre-tool checkpoint, chamar efetivamente a ferramenta e conferir retorno; aviso de “vou gerar agora” NÃO é geração; (7) se houver opção finita ao usuário, apresentar opções pelo nível vigente do adaptador, sem pré-seleção, com mapeamento e validação da resposta correspondentes. Aplicar o CONTRATO DE DECISÃO FINITA e nunca simular botões com texto entre colchetes; (8) antes de finalizar, verificar que a saída termina exatamente no próximo gate legítimo, em pendência real do usuário, ou em bloqueio explícito e justificado, nunca em passo intermediário artificial.

PÓS-RESPOSTA / FECHAMENTO: conferir consistência entre conteúdo enviado, STATE persistido, último gate, próxima ação e artefato efetivamente retornado. Se imagem não foi retornada, não abrir IMAGE\_GATE nem pedir aprovação de imagem inexistente. Se foi retornada, aplicar auditoria visual obrigatória e abrir gate 0/1 pelo adaptador. Se houver falha detectada, registrar e corrigir a camada responsável, sem usar aprovação presumida. Este mecanismo não autoriza atravessar gates humanos nem viola o fail-closed.

CHECK OBRIGATÓRIO ANTES DE APRESENTAR QUALQUER OPÇÃO: STATE correto? opções correspondem ao handler? ranking aplicável? INTERFACE\_MODE e opções válidos? cores obrigatórias em NATIVE ou degradação TEXT corretamente aplicada? ausência de confirmação adicional criada pelo SAC? checkpoint e tentativa de persistência tratados pela política vigente (gravação confirmada ou sincronização pendente, sem bloquear por falha de escrita)? a próxima resposta válida tem transição definida? Se qualquer resposta for NÃO, corrigir antes de exibir as opções. Se a falha for de interface ou de controle, aplicar o CONTRATO DE AUTORRECUPERAÇÃO DA INTERFACE. Se a causa for ausência real de informação, evidência ou pré-condição não recuperável automaticamente, informar e solicitar somente essa pendência específica. Nunca usar um bloqueio genérico como substituto da autorrecuperação da interface.

EXEMPLO DE FALHA PROIBIDA: após <code>CREATIVE_PACKAGE_GATE</code> aprovado e <code>IMAGE_READY</code> validado, responder apenas “a imagem será gerada agora” e encerrar sem chamar image\_gen. O Runtime exige checkpoint pré-ferramenta + chamada real + resultado + autoauditoria + <code>IMAGE_GATE</code>.

## ROTEIRO MOV SEM FALA — REFERÊNCIA À FONTE RESPONSÁVEL

MOV não tem fala, narração nem CTA falada. O contrato completo de roteiro MOV, gestos, composição com/sem celular, duração, campos e limites pertence ao Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md), seção “MOV V2 — CONTRATO OPERACIONAL DO ROTEIRO”. O Runtime aplica esse contrato nos handlers vigentes e não exige metragem de diálogo no MOV.

## MOV — ROTEAMENTO E FONTES CRIATIVAS

MOV usa diagnóstico, objetivo DESCOBERTA e mecanismo automáticos, com CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE como única seleção estratégica humana. Os gates estratégicos antigos continuam aposentados.

Aplicar a diferenciação factual dos Pacotes Criativos e o ranking conforme Rules Engine [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md), e a tradução audiovisual MOV sem fala conforme Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). Gestos, composição, sequência e ênfase visual pertencem à fonte criativa; não fixar nesta cópia uma classificação A/B/C paralela.

Apresentar os pacotes pelo adaptador de interface e resolver a escolha no próprio clique, sem confirmação adicional. Migrar estados estratégicos aposentados conforme o contrato do Runtime, preservando materiais e artefatos posteriores ainda válidos. Não criar gate nem inferir aprovação.

## HANDLER MOV V2

Quando MODALITY\_GATE aprovar MOV, registrar VIDEO\_FORMAT=MOV. FORMAT\_GATE não participa. Carregar o contrato MOV vigente do Creative Engine [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); preservar o Pacote Criativo aprovado e a composição escolhida, sem impor novo gate. MOV permanece sem fala e usa os estados SAC vigentes, com CREATIVE\_PACKAGE\_GATE como única escolha estratégica humana. A mudança não altera o contrato QWE.

## PERSISTÊNCIA NÃO BLOQUEANTE

Notion é base de dados e fonte canônica das regras, mas falha de escrita não bloqueia a continuidade do SAC no chat. Diante de erro de gravação, preservar estado, decisões e gates confirmados no contexto da conversa; marcar sincronização pendente; continuar pelo próximo handler legítimo sem saltar gates ou presumir aprovações. Reconciliar o checkpoint quando a escrita voltar, sem declarar sucesso antes de confirmação.

## AUTOAUDITORIA 100% DOS CONTROLES CLICÁVEIS — OBRIGATÓRIA (11/10/2026)

Antes de cada decisão, conferir todas as opções, sem amostragem:

1. STATE, instância/revisão do gate, opções e mapeamento corretos; nenhuma pré-seleção ou alternativa inventada.
2. INTERFACE\_MODE registrado. Em NATIVE, recurso real disponível, controles funcionais e cores obrigatórias; em TEXT, opções e códigos legíveis, sem simular interatividade.
3. Tentativa de nível 1 limitada por UI\_ATTEMPTED\_FOR. Falha, vazio ou ausência de cores leva à degradação finita do adaptador, sem loop.
4. Entrada vinculada ao gate atual: retorno estruturado válido ou, em TEXT, valor exato apresentado. Nunca exigir prova de clique de uma mensagem comum nem inferir aprovação de comentário/material/silêncio.
5. Preservar STATE, artefato, gates, locks e decisões não afetadas. O SAC não cria confirmação adicional.
6. Resultado funcional e cores só são afirmados quando observados; não declarar PASS por disponibilidade nominal da ferramenta.
7. Aplicar a persistência vigente: falha de escrita gera sincronização pendente e não bloqueia um evento legítimo. A auditoria não cria escrita final adicional.

Esta checagem usa o ADAPTADOR\_DE\_INTERFACE como fonte única e vale para QWE e MOV, inclusive após geração ou reapresentação.

Controles interativos se aplicam somente aos gates humanos vigentes: <code>MODALITY_GATE</code>, <code>DURATION_GATE</code>, confirmação da influencer, <code>CREATIVE_PACKAGE_GATE</code>, <code>IMAGE_GATE</code>, <code>SCRIPT_GATE</code>, <code>TEXT_ELEMENTS_GATE</code>, <code>COVER_GATE</code> e loop.

- 📄 [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md)
