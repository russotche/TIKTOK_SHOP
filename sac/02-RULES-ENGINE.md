# 02 — RULES ENGINE / CREATIVE READINESS — FASE 2

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-10-17. Fonte: https://app.notion.com/p/8a9fafd5013b82de861281127ea3ba3f

---

## P06 — IMAGE\_READY: COERÊNCIA VISUAL ANTES DA GERAÇÃO (15/10/2026)

Correção operacional do SAC, complementar a P01–P05, sem novo gate humano. IMAGE\_READY continua dependendo de todas as evidências, dos materiais, da escolha efetivamente aprovada do Pacote Criativo A/B/C, das validações derivadas, Product Lock, Influencer Lock e demais pré-requisitos já vigentes. Além de verificar sua presença, a autoauditoria interna de IMAGE\_READY deve confirmar que a direção visual aprovada foi traduzida em instruções concretas para a imagem-base: zoom, corte, produto em destaque, composição, pose inicial e espaço para movimentos previstos. A imagem projetada deve ser compatível com o roteiro visual e com a duração da modalidade escolhida.

Se houver inconsistência entre a direção selecionada e a imagem proposta, IMAGE\_READY permanece FALSE e IMAGE\_GEN não é autorizado até correção interna consistente com o pacote aprovado. Não inferir aprovação humana, não gerar imagem prematuramente, não alterar a estratégia aprovada silenciosamente e não inventar detalhes do produto. Uma mudança material na proposta aprovada requer o gate humano pertinente já existente; simples ajustes técnicos fiéis à opção podem ser feitos internamente.

Preservar QWE com fala, MOV sem fala, fidelidade à oferta e à variante, Interface Limpa e <code>IMAGE_GATE</code>, <code>SCRIPT_GATE</code>, <code>TEXT_ELEMENTS_GATE</code> e <code>COVER_GATE</code>.

## CORREÇÃO CANÔNICA P02 — DESEJO E BENEFÍCIO PERCEBIDO (15/10/2026)

Após resolver materiais, produto/variante, evidências e locks, e ANTES de <code>CREATIVE_PACKAGE_PREP</code>, identificar internamente: (1) característica real sustentada pela evidência; (2) necessidade ou desejo plausível do público, como hipótese quando não comprovado; (3) benefício funcional ou emocional percebido que essa característica pode comunicar; (4) como representar esse benefício de modo honesto no criativo.

<b>FINALIDADE:</b> cada Pacote Criativo A/B/C comunica não apenas o que o produto tem, mas por que isso pode importar ao comprador. Integrar a leitura a AIDA/NEXT\_ADVANCE internos, OBJETIVO=DESCOBERTA e mecanismo criativo automático; jamais substituir a identificação factual do produto por apelos emocionais. Os três pacotes continuam distintos e unidos em mensagem, abertura e conceito, sem aprovações separadas.

<b>MODALIDADES:</b> QWE pode comunicar benefício por fala e demonstração, dentro das evidências e duração. MOV deve comunicá-lo exclusivamente por enquadramento, gestos, movimento, interação com o produto e composição visual, sem fala ou locução. Não exigir uma transformação visual artificial para todo produto.

<b>FIDELIDADE:</b> não inventar dor específica, perfil do público, resultado, elogios de terceiros, transformação corporal, atributos, preço, descontos ou garantias. Não alegar que alguém ficará mais bonita, desejada, elogiada ou curada como consequência comprovada sem evidência; quando necessário, usar proposta estética subjetiva, sem promessa. Se não houver evidência suficiente para um benefício específico, limitar a comunicação ao que é observável e verdadeiro.

<b>EXECUÇÃO E INTERFACE:</b> esta etapa é análise interna automática. <code>CREATIVE_PACKAGE_GATE</code> A/B/C permanece a única escolha humana estratégica. Manter INTERFACE LIMPA: exibir somente propostas comparáveis e controles necessários, sem relatórios de diagnóstico. Preservar <code>IMAGE_READY</code>, <code>PRODUCT_LOCK</code>, <code>INFLUENCER_LOCK</code> e gates posteriores.

# AUTORIDADE

Fonte canônica única da Fase 2 para condições de prontidão criativa e autorização técnica pré-<code>image_gen</code>. Não controla a ordem do fluxo e não redefine o Bootstrap ou os handlers de materiais.

Fontes relacionadas: entrada e interface [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md); estados [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md); evidências/locks [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); audiovisual [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); textos/capa [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); fechamento [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).

# PRINCÍPIO INVIOLÁVEL

<b>MATERIAL RESOLVIDO ≠ PRONTIDÃO CRIATIVA ≠ IMAGE\_READY ≠ IMAGEM APROVADA.</b>

Nenhum evento de material, confirmação, reutilização, comentário, silêncio ou inferência pode autorizar geração.

# CONTRATO IMAGE\_READY

<code>IMAGE_READY = MATERIALS_OK + EVIDENCE_OK + AUDIENCE_CONTEXT_READY + CONTEXT_READING_READY + NEED_DIAGNOSIS_READY + AIDA_READY + OBJECTIVE_READY_DESCOBERTA + MECHANISM_READY + CREATIVE_PACKAGE_APPROVED + MESSAGE_CENTRAL_APPROVED + OPENING_STYLE_OK + CONCEPT_APPROVED + CONCEPT_OK + PRODUCT_LOCK_OK + INFLUENCER_LOCK_OK</code>

Todos os termos do contrato devem estar explicitamente <code>TRUE</code> no estado atual. Nenhum diagnóstico interno pode ser inventado e nenhum gate humano pode ser inferido ou resolvido silenciosamente.

Se qualquer termo estiver <code>FALSE</code>, <code>PENDING</code>, <code>UNKNOWN</code> ou não existir:

<code>IMAGE_READY = FALSE</code>

<code>image_gen = BLOCKED</code>

<b>ÚNICA ENTRADA AUTORIZADA PARA </b><b><code>image_gen</code></b><b> NA GERAÇÃO DA IMAGEM-BASE:</b>

<code>IMAGE_READY = TRUE → IMAGE_GEN</code>

Nenhum outro estado, evento ou handler da Fase 2 possui aresta para geração da imagem-base. A rota <code>COVER_READY → COVER_GEN</code>, definida exclusivamente na Fase 4, é uma edição posterior da imagem já aprovada para aplicar o texto da capa e não substitui, contorna nem enfraquece este contrato.

# MATERIALS\_OK

TRUE somente quando link/referência do produto, imagem(ns) utilizável(is) do produto e referência utilizável da influencer exigida pela execução estiverem resolvidos. Resolver materiais não altera nenhum outro termo de IMAGE\_READY.

# EVIDENCE\_OK

TRUE somente quando existe evidência real nos materiais ou informação explícita do usuário sustentando exatamente o elemento usado pela estratégia atual.

Possibilidade, aparência, plausibilidade, inferência, “parece”, “talvez” ou conhecimento genérico da categoria não contam como evidência.

Sem sustentação: <code>EVIDENCE_OK = FALSE</code>; pedir somente a evidência/informação faltante.

# AUDIENCE\_CONTEXT\_READY

A base fixa da execução é <code>Mulher + Brasil + TikTok Shop</code>. A partir dela, construir um contexto específico da audiência usando somente produto, evidências e situação real da execução. Pode registrar situação de uso relevante, necessidade/interesse sustentado e grau de familiaridade necessário para compreender o criativo. É proibido inventar persona, idade, renda, profissão, estilo de vida, dor ou desejo não sustentado. <code>AUDIENCE_CONTEXT_READY=TRUE</code> somente quando o contexto estiver sustentado ou corretamente limitado ao que de fato se sabe.

# CONTEXT\_READING\_READY

Registrar internamente três campos: <b>O QUE SABEMOS / O QUE FALTA / BARREIRA OU DESEJO RELEVANTE</b>. O campo O QUE FALTA não autoriza inferência: se a ausência impedir a estratégia, bloquear e pedir somente o dado necessário. <code>CONTEXT_READING_READY=TRUE</code> somente quando essa leitura estiver coerente com a evidência disponível.

# NEED\_DIAGNOSIS\_READY

Depois da leitura de contexto, registrar internamente qual necessidade parece dominante entre PERCEBER / DESEJAR / ENTENDER / CONFIRMAR. Este diagnóstico é hipótese interna, não cria gate humano e alimenta a preparação dos Pacotes Criativos. <code>NEED_DIAGNOSIS_READY=TRUE</code> somente quando houver base suficiente para construir propostas factuais.

# OPENING\_STYLE\_OK — VALIDAÇÃO DERIVADA DO PACOTE

Aplicável a toda execução SAC e sempre subordinado a NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO, MENSAGEM\_CENTRAL e evidência. A preparação interna define a abertura dos primeiros três segundos dentro de cada Pacote Criativo; não há gate separado.

Depois de <code>EVIDENCE_OK=TRUE</code>, usar os estilos abaixo como referências internas para preparar a abertura de cada Pacote Criativo; não apresentar uma seleção separada nem equiparar a letra do estilo à letra do pacote:

A) IMAGINAÇÃO — abrir pela visualização de uma cena concreta de uso. A função dominante é fazer a pessoa imaginar uma experiência específica com o produto, sustentada pelos materiais. A cena pode ocorrer no presente ou no futuro; a simples menção ao futuro não transforma a abertura em B.

B) FUTURO — abrir pela projeção temporal da decisão: destacar a passagem entre uma escolha considerada agora e uma possibilidade posterior. A função dominante é a relação entre agora e depois, não a visualização detalhada de uma cena. Não prometer resultado, criar urgência falsa nem alegar benefício não comprovado.

C) JUSTIFICATIVA DA ESCOLHA / VALOR PERCEBIDO — abrir pelo motivo que torna o produto, uso ou escolha relevante para a pessoa no estágio aprovado da execução. A função dominante é explicar por que aquilo faz sentido, com base no NEXT\_ADVANCE, no objetivo, no mecanismo, na MENSAGEM\_CENTRAL e em evidências. “Por quê”, “justo” e uma percepção comparativa de preço são formas possíveis de expressão, não opções separadas; a percepção de preço só pode ser usada com evidência específica. Não informar preço numérico nem inventar comparação, desconto, economia ou percepção coletiva.

REGRA DE CLASSIFICAÇÃO A–C: classificar pela função dominante da abertura nos primeiros três segundos, não por uma palavra isolada. Se a abertura puder ser lida em mais de uma opção, reformular até o efeito principal ficar inequívoco. Exemplo: “imagina” pode aparecer em A ou B; será A se cria uma cena concreta e B se enfatiza a passagem de agora para depois.

As três opções são estilos de abertura e não substituem NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO ou MENSAGEM\_CENTRAL, nem exigem palavras obrigatórias. O estilo derivado do pacote aprovado deve ficar reconhecível nos primeiros três segundos audiovisuais pelo conjunto de ação, expressão, reação, enquadramento e fala quando houver; não depende de um trecho falado obrigatório. O restante do roteiro e todos os ELEMENTOS DE TEXTO continuam subordinados às decisões estratégicas aprovadas, à evidência, à MENSAGEM\_CENTRAL e à lei fundamental do SAC.

Abertura é componente interno de cada Pacote Criativo A/B/C. Não existe <code>OPENING_STYLE_GATE</code> operacional. A abertura selecionada deriva exclusivamente do pacote aprovado no <code>CREATIVE_PACKAGE_GATE</code>.

<code>OPENING_STYLE_SELECTED</code> e <code>OPENING_STYLE_OK</code> são estados derivados do Pacote Criativo aprovado. Não recebem escolha humana independente e não liberam outro gate. A autorização visual depende do pacote aprovado, evidências e locks.

# CONCEPT\_APPROVED / CONCEPT\_OK — VALIDAÇÕES DERIVADAS DO PACOTE

Em <code>CREATIVE_PACKAGE_PREP</code>, formular um conceito audiovisual integrado para cada uma das três propostas A/B/C. Cada conceito deve ser coerente com a mensagem e a abertura do próprio pacote, diagnóstico, objetivo, mecanismo e evidências. Não exigir <code>OPENING_STYLE_OK</code> de aprovação prévia nem abrir seleção de conceito separada.

Nenhuma variante pode introduzir novo público, novo avanço, nova promessa, nova objeção ou nova necessidade. O sistema deve aplicar o ranking contextual por estrelas definido nesta Fase, sem escolher a opção pelo usuário.

Antes da aprovação do pacote, <code>CONCEPT_APPROVED=FALSE</code> e <code>CONCEPT_OK=FALSE</code>. Após escolha explícita em <code>CREATIVE_PACKAGE_GATE</code>, derivar <code>CONCEPT_SELECTED</code>, <code>CONCEPT_APPROVED</code> e <code>CONCEPT_OK</code> da mesma opção aprovada. <code>CONCEPT_OK=TRUE</code> exige evidência, Product Lock, Influencer Lock e SAC SAFE. Não solicitar aprovação independente de conceito; incompatibilidade exige corrigir o pacote e reapresentá-lo no gate vigente.

# PRODUCT\_LOCK\_OK

A referência real do produto é a âncora. Preservar atributos observáveis aplicáveis: cor, forma, silhueta, estrutura, proporções, componentes, acabamento, inscrições/textos físicos, símbolos, encaixes e microdetalhes.

É proibido substituir, redesenhar, reinterpretar, completar ou inventar produto, marca, texto ou componente.

Nova cena, pose, enquadramento ou interação não autorizam alteração do produto.

Quanto maior a fidelidade exigida, menor a liberdade de reconstrução do produto.

Se a cena exigir transformação incompatível com a referência: <code>PRODUCT_LOCK_OK = FALSE</code>.

## PROTOCOLO OPERACIONAL — FIDELIDADE MÁXIMA DE IMAGEM (APROVADO EM 14/10/2026)

<b>Escopo:</b> regra comum obrigatória do SAC, tanto QWE quanto MOV, aplicada à imagem-base antes de apresentá-la no IMAGE\_GATE. A imagem é fonte para geração posterior do vídeo no FLOW. Prioridade: fidelidade comercial antes da estética.

1. <b>LER:</b> examinar minuciosamente todas as fotografias originais utilizáveis, separando produto e variante anunciada.
2. <b>MAPEAR:</b> conferir cor, estampa, forma, proporções, botões, presilhas, costuras, alças, decotes, mangas, elásticos, inscrições, acabamentos, posição, quantidade e orientação de cada detalhe aplicável. Registrar mentalmente o que está visível e o que não é comprovável.
3. <b>PRESERVAR:</b> não inventar, retirar, multiplicar, deslocar, espelhar, reformular ou embelezar elementos físicos do produto; manter a variante exata e os locks vigentes.
4. <b>GERAR:</b> montar a cena autenticamente, usando as referências reais como âncora. Se a montagem exigir adivinhar componentes importantes, não gerar como se fossem verificados.
5. <b>AUTOAUDITAR:</b> comparar a imagem resultante com as referências disponíveis antes do IMAGE\_GATE, conferindo individualmente todos os detalhes críticos e eventuais divergências novas.
6. <b>BLOQUEAR E CORRIGIR:</b> discrepância identificada exige correção e nova conferência. Característica relevante incerta exige declaração explícita da limitação e, quando indispensável para a fidelidade comercial, referência complementar; jamais declarar fidelidade comprovada por suposição.

<b>Condição de saída:</b> somente apresentar ao IMAGE\_GATE uma imagem autoconsistente com o produto e as referências verificáveis, identificando qualquer detalhe que permaneça não verificável. A aprovação humana é obrigatória e não substitui a autoauditoria.

<b>Meta aspiracional:</b> buscar erro inferior a 1%; não afirmar que a taxa foi medida nem garantir precisão matemática ou equivalência pixel a pixel.

<b>Cadeia de segurança:</b> produto real → imagem fiel → vídeo. A checagem preventiva da imagem cabe ao SAC; a verificação final do vídeo será realizada pelo usuário na ferramenta do TikTok. <b>Não</b> exigir auditoria do arquivo final do FLOW pelo ChatGPT nem criar novo gate de vídeo.

<b>Precedência:</b> esta regra complementa PRODUCT\_LOCK\_OK e IMAGE\_READY, sem substituir a ordem do Runtime, a estratégia aprovada ou os gates existentes.

# INFLUENCER\_LOCK\_OK

A referência oficial governa a identidade visual da influencer. Em toda execução SAC, a imagem-base, o roteiro visual e qualquer artefato visual derivado devem usar sempre a nossa influencer oficial enviada ou explicitamente designada como referência para a execução, podendo ser reutilizada quando acessível, confiável e validada pelos critérios de <code>INFLUENCER_LOCK_OK</code>. É proibido substituir por outra pessoa, trocar por outra mulher, variar a identidade, gerar apenas alguém parecido ou reinterpretar sua identidade.

Uma referência só é utilizável quando: (a) foi enviada ou explicitamente designada pelo usuário como referência oficial desta execução; (b) está acessível e tem nitidez/detalhe suficiente para identificar traços visuais estáveis da influencer; (c) não está tão obstruída, cortada ou degradada que preservar a identidade exigiria adivinhação; e (d) não há conflito não resolvido entre referências. Se várias imagens forem compatíveis, podem ser usadas em conjunto; se divergirem, pedir ao usuário que indique a referência oficial antes de avançar.

A escolha válida da referência pelo ADAPTADOR\_DE\_INTERFACE do Runtime confirma sua identificação, por retorno estruturado ou alternativa textual autorizada; não comprova acesso, nitidez, ausência de conflito ou fidelidade de geração. Antes de CREATIVE\_PREP validar esses critérios. Falha define INFLUENCER\_REFERENCE\_USABLE=FALSE e INFLUENCER\_LOCK\_OK=FALSE; pedir somente a correção necessária.

Roupa, pose, cenário e direção artística podem mudar quando compatíveis com o conceito; identidade observável não.

Check universal obrigatório: <code>INFLUENCER_OFFICIAL_ONLY = TRUE</code>.

Se a geração ou edição apresentar outra pessoa, <code>INFLUENCER_LOCK_OK = FALSE</code> e o artefato é inválido.

<code>INFLUENCER_LOCK_OK=TRUE</code> exige referência utilizável conforme os critérios acima e identidade preservada na proposta visual.

<b>PRESERVAÇÃO INTEGRAL DA REFERÊNCIA ENVIADA:</b> manter 100% da identidade e dos detalhes observáveis da influenciadora enviada para a execução: rosto, olhos, boca, maquiagem, cabelo, pele, proporções, marcas e tatuagem com lado anatômico correto quando visíveis. Não embelezar, afinar, trocar traços, recriar tatuagem ou substituir por pessoa parecida sem pedido específico do usuário. Roupa, pose e cenário só mudam conforme a direção aprovada, sem alterar a pessoa. Fidelidade integral é requisito, não garantia automática da ferramenta: conferir o resultado real, indicar divergência ou impossibilidade de verificar e corrigir antes de alegar atendimento. Referência inacessível não pode ser completada por memória; solicitar a imagem necessária. Esta regra não pressupõe referência padrão armazenada no Notion.

# SAC SAFE PRÉ-GERAÇÃO

Mesmo com todos os termos candidatos a TRUE, bloquear conceito que dependa de preço, desconto, cupom, estoque, urgência, escassez, prova social, avaliação, compradores, popularidade, função, benefício, certificação, resultado ou condição comercial não sustentados.

# FAIL-CLOSED

Ausência de informação nunca vira TRUE por inferência.

Conflito entre evidências = PENDING/BLOCKED.

Falha em determinar o estado = BLOCKED.

A IA pode verificar condições técnicas, mas não substituir gates humanos posteriores.

# NÃO DUPLICAÇÃO

Esta página define as condições. O Runtime define ordem/transições. O Creative Engine executa a criação específica da execução SAC. Uma regra universal criada aqui não deve ser copiada operacionalmente para outras páginas.

# SISTEMA UNIVERSAL DE RANKING POR ESTRELAS — PRÉ-ROTEIRO

Aplicável ao <code>CREATIVE_PACKAGE_GATE</code> e a outros gates humanos realmente vigentes que apresentem alternativas ao usuário. Gates aposentados não participam.

Cada alternativa deve receber uma avaliação contextual por estrelas com justificativa curta, baseada somente no alinhamento com produto, evidência, AUDIENCE\_CONTEXT, NEED\_DIAGNOSIS, NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO e MENSAGEM\_CENTRAL já vigentes naquele ponto.

Escala padrão:

- <code>⭐⭐⭐⭐⭐</code> = mais indicada para a execução atual;
- <code>⭐⭐⭐</code> = opção intermediária, válida porém menos forte;
- <code>⭐</code> = menos indicada entre as opções apresentadas.

A classificação não é fixa por categoria e deve ser recalculada em cada execução. <code>⭐⭐⭐⭐⭐</code> significa recomendação contextual do agente, nunca aprovação automática. O agente deve explicar em uma frase curta por que cada opção recebeu aquela classificação, pode indicar qual é a mais alinhada, mas jamais escolher, pré-selecionar, aprovar ou resolver o gate pelo usuário.

Gates de aprovação sem alternativas, como <code>IMAGE_GATE</code> e <code>SCRIPT_GATE</code>, usam seus próprios formatos.

# RASTREABILIDADE — REFERÊNCIAS DE AUTORIDADE

O Runtime é a fonte operacional para registrar a escolha humana do <code>CREATIVE_PACKAGE_GATE</code> e qualquer rastreabilidade vigente. Não existe etapa operacional após <code>CONCEPT_GATE</code>, pois esse gate está aposentado.

O Lifecycle é a única fonte para definir quais versões contam e para incrementar, preservar ou zerar contadores por produto, gate e letra. Aplicar exclusivamente a seção <code>CONTADORES DE RASTREABILIDADE — REGRA CANÔNICA</code> do Lifecycle.

Esta página não recalcula, incrementa, preserva, zera nem persiste contadores de rastreabilidade. Os valores são informativos: não alteram estrelas, não bloqueiam repetição, não pré-selecionam alternativas nem substituem a escolha humana.

## MOV — TRADUÇÃO ESTRATÉGICA EM LINGUAGEM VISUAL

REGRA ATUAL MOV: OBJETIVO=A/DESCOBERTA fixo, NEXT\_ADVANCE e mecanismo integrados automaticamente ao diagnóstico. <code>OBJECTIVE_GATE</code>, <code>MECHANISM_GATE</code>, <code>MESSAGE_CENTRAL_GATE</code>, <code>OPENING_STYLE_GATE</code> e <code>CONCEPT_GATE</code> estão aposentados. MOV segue <code>CREATIVE_PACKAGE_PREP → CREATIVE_PACKAGE_GATE</code> como única seleção estratégica humana.

REGRA OBRIGATÓRIA PARA VIDEO\_FORMAT=MOV: cada Pacote Criativo A/B/C precisa vir acompanhado de efeito observável distinto nos enquadramentos, gestos, ritmo, sequência e ênfase audiovisual, sustentado pelo produto e evidências, sem depender de narração, fala, texto na tela ou CTA falada. Não basta reescrever três versões do mesmo plano.

<b>EXEMPLOS VISUAIS ADAPTÁVEIS:</b> os exemplos seguintes não atribuem objetivos às letras A/B/C; o objetivo vigente permanece DESCOBERTA e os três pacotes são diferenciados dinamicamente conforme P03.

Reconhecimento e curiosidade: priorizar reconhecimento e curiosidade visual inicial; entrada visual marcante e legibilidade geral do produto, sem alegar desempenho.

Inspeção e entendimento: priorizar inspeção visual e entendimento dos atributos verificáveis; planos próximos com tempo para observar detalhes pertinentes.

Visão para decisão informada: priorizar visão que favoreça decisão informada do produto em uso, diferentes ângulos úteis e fechamento visual natural; não presume intenção prévia de compra, nem usa urgência/preço/promessa não comprovada.

Estas são DIREÇÕES AUDIOVISUAIS GERAIS para diferenciar o gate, NÃO conceitos/roteiros fechados: o mecanismo é automático; mensagem, abertura e conceito integram a mesma opção aprovada em <code>CREATIVE_PACKAGE_GATE</code> e determinam a execução concreta, sem escolhas humanas separadas. O sistema NÃO fixa uma tomada, gesto ou cronograma idêntico para categorias diferentes. Adaptação universal a moda, acessórios, bolsas, beleza e qualquer produto por seus atributos reais. No MOV com celular, selfie no espelho e aparelho na altura do rosto, sem exigir cobertura integral da face; no MOV sem celular, câmera externa abaixo do pescoço; rosto fora do enquadramento e produto em destaque nas duas composições; para todo MOV, SILÊNCIO ABSOLUTO sem fala/narração/CTA falada, vídeo-base sem overlays ou música. Na FASE 3, validar se as ações e planos efetivamente cumprem o objetivo DESCOBERTA e o pacote escolhido e diferem logicamente dos outros dois, sem reabrir gates aprovados.

Ranking A/B/C e seleção aplicam-se ao <code>CREATIVE_PACKAGE_GATE</code>.

## PADRÃO CANÔNICO MOV — PRODUTO PROTAGONISTA (correção universal aprovada em QWE-12, 11/10/2026)

<b>REGRA ABSOLUTA: O PRODUTO É O PROTAGONISTA, INDEPENDENTEMENTE DA CATEGORIA.</b> Pode ser vestido, sutiã, relógio, meia, sapato, bolsa, acessório ou qualquer outro produto. Nunca substituir essa regra por “roupa protagonista” nem por enquadramento corporal fixo. A imagem e os movimentos devem privilegiar a leitura imediata das características reais do produto, sua escala, formato e detalhes importantes.

<b>ENQUADRAMENTO ADAPTATIVO POR PRODUTO:</b> vídeo 9:16. Vestido: pescoço para baixo e peça visível; relógio: punho e relógio em destaque; meia ou sapato: pé/perna pertinente; sutiã: região do produto com enquadramento apropriado; demais categorias: close e planos úteis ao objeto. Manter rosto fora do enquadramento no MOV, conforme a composição aprovada com ou sem celular; isso não torna “pescoço para baixo” um plano corporal obrigatório para todo produto. Não cortar atributos essenciais; mostrar contexto apenas quando ajudar o produto.

<b>MOV:</b> imagem-base já preparada para os movimentos e aproximações do vídeo, gestos naturais expressivos e ênfase no objeto. Sem fala, narração, CTA falada, música ou texto/overlay no vídeo-base.

<b>LOCKS:</b> preservar produto real e influencer oficial nas cenas com pessoa; jamais espelhar marcas corporais. A tatuagem identificadora da influencer permanece na perna direita anatômica quando visível, nunca na esquerda. Não adicionar, deslocar ou espelhar.

<b>AUTOAUDITORIA OBRIGATÓRIA ANTES DE IMAGE\_GATE:</b> (1) produto domina a atenção visual; (2) enquadramento é adequado à categoria e dimensões do produto; (3) detalhes e identidade respeitam referências; (4) 9:16 e movimentos MOV factíveis; (5) rosto fora do enquadramento e cenário sem competir com o produto; (6) silêncio e vídeo-base limpo. Reprovar e corrigir qualquer violação antes da apresentação. A aprovação humana da imagem permanece necessária. O corte do pescoço para baixo aprovado em QWE-12 é EXEMPLO de vestido, não imposição a outras categorias.

## BLOQUEIO GLOBAL DE CONFORMIDADE COM PRODUTO — TODOS OS FORMATOS (11/10/2026)

ORDEM EXPRESSA DO USUÁRIO: aplicar imediatamente a TODAS as modalidades QWE/SAC (MOV, QWE, vídeo de 10s e 15s, novas variantes e qualquer formato futuro). A fidelidade comercial ao produto é condição obrigatória e não se limita à qualidade estética.

PRODUCT\_LISTING\_MATCH: comparar artefato visual com a(s) imagem(ns) de referência do produto efetivamente vinculado ao anúncio no TikTok Shop, incluindo VARIANTE selecionada (cor, estampa, forma, decote, mangas, fenda, posição da fenda, acabamento, marca, texto físico e quaisquer atributos pertinentes). Variantes distintas de um mesmo anúncio NÃO podem ser fundidas, inventadas nem apresentadas como sendo a variante escolhida. Se a variante não estiver inequívoca, obter confirmação antes de gerar.

GATE TÉCNICO BLOQUEANTE: PRODUCT\_LISTING\_MATCH somente TRUE após conferência de identidade visual e evidência; FALSE/PENDING/UNKNOWN implica REJEITAR internamente a imagem ou vídeo como apto para publicação; não liberar roteiro derivado, capa, publicação ou alegação de prontidão comercial enquanto a divergência persistir. Aprovação anterior da imagem NÃO elimina uma divergência factual descoberta posteriormente. Invalidar somente artefatos dependentes e retornar à menor etapa necessária para refazer com a referência correta, preservando decisões não afetadas.

Antes de gerar e antes de oferecer qualquer artefato para aprovação, executar auditoria sistemática de correspondência comercial item a item; em caso de falha, dizer quais elementos divergem, corrigir e reaudar. A aprovação humana permanece necessária, mas não substitui a correspondência ao anúncio. Não alegar que verificou o catálogo/listing se somente imagens de chat estiverem disponíveis; nessa hipótese indicar validação pendente de conferência com a listagem real.

PROTEÇÃO DA CONTA: jamais recomendar a publicação de conteúdo visual sabidamente divergente, não confirmado ou de outra variante. A regra vale independentemente de plataforma/gerador e do grau de beleza da imagem. Notion é registro canônico das regras, não trava de execução; falha de persistência não autoriza liberar conteúdo inseguro.

## PROTEÇÃO EM TRÊS MOMENTOS

Regra obrigatória do SAC para ambas as modalidades irmãs, QWE e MOV, e qualquer produto.

1. ANTES DA GERAÇÃO: verificar fidelidade ao produto real e à variante anunciada, além de conformidade com as políticas aplicáveis do TikTok Shop.
2. DEPOIS DA GERAÇÃO: executar autoauditoria da imagem-base SAC contra o produto e a variante anunciada antes do IMAGE\_GATE. A checagem do vídeo final exportado ocorrerá externamente pelo usuário com os recursos de verificação do TikTok; não exigir auditoria do vídeo final pelo ChatGPT como gate adicional, nem presumir que essa verificação garante ausência de violações.
3. ANTES DA PUBLICAÇÃO: não recomendar liberação enquanto existirem divergências, dúvidas materiais ou verificações pendentes. A aprovação humana permanece obrigatória.

Esta regra complementa o PRODUCT\_LISTING\_MATCH e não altera a sequência dos gates criativos, nem cria gate de produção após roteiro. A verificação do arquivo final é condição para recomendação de publicação. Não prometer ausência de penalidades nem atribuir causas às violações sem suas justificativas oficiais.

Referência oficial fornecida pelo usuário: [https://seller-br.tiktok.com/university/essay?knowledge\_id=148058718537493&lang=pt-BR](https://seller-br.tiktok.com/university/essay?knowledge_id=148058718537493&lang=pt-BR)
