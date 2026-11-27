# 06 — ELEMENTOS DE TEXTO ENGINE — FASE 4

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-10-23. Fonte: https://app.notion.com/p/6c4fafd5013b82dfaea5017079a0dc0c

---

## DIRETRIZ PRIORITÁRIA — HASHTAGS SAC (23/10/2026)

<b>REGRA VIGENTE PARA QWE E MOV:</b> usar exatamente 5 hashtags por publicação, nesta composição fixa: 3 hashtags obrigatórias de campanha, 1 hashtag relacionada ao nicho e 1 hashtag relacionada especificamente ao produto.

<b>HASHTAGS OBRIGATÓRIAS, COM GRAFIA EXATA:</b> #TiktokShopBR1111 #TiktokShopBRBlackFriday #TiktokShopBR1212.

<b>HASHTAGS COMPLEMENTARES:</b> escolher 1 hashtag do nicho e 1 hashtag do produto, ambas diretamente relacionadas à evidência e à mensagem aprovada. Usar letras minúsculas nas duas complementares. Não duplicar hashtags ou preencher com termos irrelevantes.

<b>QWE E MOV:</b> a mesma regra das 5 hashtags vale para ambas as modalidades. A composição textual específica de cada modalidade permanece inalterada. Esta regra substitui integralmente a exigência anterior de 1 a 3 hashtags.

<b>VERIFICAÇÃO OBRIGATÓRIA:</b> conferir presença, grafia e quantidade exata das 3 hashtags de campanha e das 2 hashtags complementares, sem alterar a grafia das hashtags obrigatórias fornecidas pelo usuário.

## CONTRATO ATIVO POR MODALIDADE — SAC (12/10/2026)

<b>FONTE ÚNICA DA COMPOSIÇÃO TEXTUAL POR MODALIDADE.</b> SAC é sistema-mãe; QWE e MOV são modalidades irmãs. As peças seguem a mesma revisão da MENSAGEM\_CENTRAL, as evidências e o roteiro aprovado.

<b>QWE:</b> exatamente quatro peças: TEXTO/TÍTULO NA TELA; MICRO-CTA / CTA DO LINK; DESCRIÇÃO + HASHTAGS; PALAVRAS-CHAVE. Aplicar as seções específicas QWE desta página.

<b>MOV:</b> exatamente três itens, cada um em bloco Markdown copiável separado:

1. <b>Frase pessoal curta provocando o lead:</b> primeira pessoa, natural, espontânea e com emoção concreta, coerente com o produto e a mensagem aprovados. Preferir aproximadamente 30–75 caracteres; máximo 90, incluindo espaços e pontuação. Pode ter quebra natural de linha; não exigir caixa alta. Não inventar experiência de uso, atributo, promessa, escassez ou reação de terceiros.
2. <b>CTA para o campo nome do produto:</b> MAIÚSCULAS; sinais <code><</code>, <code>></code> e <code>-</code> opcionais. Máximo 30 caracteres incluindo espaços e símbolos, ideal próximo de 20; validar a contagem e a coerência factual. Não substituir a identificação oficial do catálogo quando exigida.
3. <b>Chamada provocativa + hashtags:</b> começar com emoji relacionado e conter o nome factual do produto. Usar conversa natural, provocação leve e elegante, preferencialmente em pergunta, para despertar curiosidade e identificação sem enganar. Adaptar ao produto, à imagem, à mensagem e ao roteiro; não reutilizar mecanicamente a mesma chamada. Após linha em branco, incluir as hashtags selecionadas exclusivamente pela DIRETRIZ PRIORITÁRIA — HASHTAGS SAC.

Não criar descrição AIDA, palavras-chave separadas ou micro-CTA adicional no MOV. Evitar texto genérico, tecnicismo, exagero, sexualização, insinuação inadequada, pressão, falsa escassez, preço/desconto não confirmado e benefícios ou características sem evidência; preservar o valor simbólico quando aplicável.

<b>Exemplo ilustrativo do item 3:</b> <code>🌸 Vai dizer que você não se imaginou nesse conjunto cropped e short?</code>, seguido de linha em branco e das hashtags pertinentes. Adaptar emoji e nome ao produto real.

<b>APLICAÇÃO:</b> a frase MOV pode ser usada como overlay na edição posterior; nenhum destes itens integra o prompt de geração do vídeo-base MOV, que permanece sem fala, música, texto ou overlays. Os demais textos são externos ao vídeo-base. QWE e MOV exigem validação interna das respectivas peças e aprovação humana; a capa permanece posterior à aprovação do conjunto. Esta seção incorpora as decisões MOV de 11/10 e 14/10 e suas atualizações aprovadas, sem mudar o contrato audiovisual.

# AUTORIDADE

Fonte canônica da V2 para criação, validação e aprovação dos ELEMENTOS DE TEXTO após <code>SCRIPT_GATE=1</code>. Não redefine decisões estratégicas, materiais, a geração da imagem-base nem o processo de criação do vídeo no FLOW. Define os critérios textuais, a âncora imutável e o contrato visual da capa. Seus estados, transições e recuperação são definidos exclusivamente no Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

Fontes relacionadas: entrada e interface [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md); estados [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md); evidências/locks [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); audiovisual [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); textos/capa [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); fechamento [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).

# ENTRADA

Somente <code>SCRIPT_GATE=1</code> entra diretamente em <code>TEXT_ELEMENTS_PREP</code>. Nesse gate, <code>1</code> aprova somente o roteiro apresentado e libera a criação dos ELEMENTOS DE TEXTO; não confirma execução no FLOW nem geração ou avaliação de vídeo.

# FLOW / VÍDEO

O roteiro aprovado pode ser usado pelo usuário no FLOW, mas essa execução é independente do <code>SCRIPT_GATE</code>. <code>SCRIPT_GATE=1</code> aprova somente o roteiro apresentado e libera diretamente os ELEMENTOS DE TEXTO. Não exigir execução, geração, avaliação ou upload de vídeo; não criar segundo gate.

# TEXT\_ELEMENTS\_PREP

Antes de criar as peças, recuperar a MENSAGEM\_CENTRAL definida antes da escrita do roteiro, conforme a diretriz canônica de coerência semântica em [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md). Usar a mensagem e a revisão vigente da mesma execução e do roteiro aprovado; não criar um novo ângulo na etapa de ELEMENTOS DE TEXTO. Se houver pedido de mudança de sentido, aplicar o contrato REVISÃO DA MENSAGEM CENTRAL da Fase 3 antes de continuar. Roteiro invalidado não autoriza ELEMENTOS DE TEXTO. Se o registro estiver ausente, recuperar a definição a partir do contexto confiável da execução; se isso não for possível, bloquear e pedir somente o esclarecimento necessário, sem inventar outra mensagem.

Criar somente as peças definidas no CONTRATO ATIVO POR MODALIDADE desta página, subordinadas à direção interna fundamentada, objetivo, mecanismo, MENSAGEM\_CENTRAL vigente, evidência e roteiro aprovado. A abertura derivada do pacote rege os primeiros três segundos; os textos preservam a mensagem sem repetição literal.

A CAPA DO VÍDEO é um artefato final separado e obrigatório. Ela só pode ser solicitada e criada depois que os ELEMENTOS DE TEXTO exigidos pela modalidade (QWE: quatro; MOV: três) forem criados, passarem no <code>TEXT_ELEMENTS_OUTPUT_CHECK</code> e forem aprovados pelo usuário em <code>TEXT_ELEMENTS_GATE=1</code>. A CAPA é sempre a última coisa a ser criada na execução.

## REGRA DE VALOR SIMBÓLICO, AFETIVO OU RELIGIOSO

Quando o produto carregar significado simbólico, afetivo, religioso, devocional ou memorial comprovado pelos materiais, os ELEMENTOS DE TEXTO devem refletir esse valor humano real e não reduzi-lo a linguagem genérica de produto. Termos vagos como “detalhe”, “item”, “peça bonita” ou equivalentes devem ser evitados quando apagam o significado principal do objeto.

A escrita deve reconhecer, quando sustentado pela evidência, conceitos como fé, devoção, representação, símbolo, lembrança, pertencimento ou significado afetivo. Isso deve acontecer sem inventar crenças da pessoa, sem presumir intensidade emocional e sem criar promessa espiritual, milagre, proteção sobrenatural, cura, bênção garantida ou qualquer efeito não demonstrável.

Regra operacional: <code>SYMBOLIC_VALUE_PRESERVED=TRUE</code> somente quando as peças exigidas pela modalidade e a futura capa respeitam o significado real do produto sem banalizá-lo e sem extrapolar a evidência. Se um produto de forte valor simbólico puder ser trocado por qualquer outro objeto sem quase alterar o texto, a peça é genérica e deve ser refeita antes do <code>TEXT_ELEMENTS_GATE</code>.

# TEXTO/TÍTULO — REGRA UNIVERSAL SAC

<b>ESCOPO: QWE.</b> No MOV, aplicar exclusivamente o CONTRATO ATIVO POR MODALIDADE.

O TEXTO/TÍTULO NA TELA é a frase exibida sobre o vídeo como uma legenda editorial, criada depois da aprovação do roteiro e entregue separadamente do bloco copiável para o FLOW. Deve completar a conversa do vídeo com uma frase afirmativa, completa e compreensível sozinha, unindo uma informação real e relevante do produto ao desejo concreto de quem assiste. Não entregar apenas um fragmento, nome de produto ou slogan sem desenvolver a ideia.

Antes de escrever, identificar: <code>Qual NEXT_ADVANCE foi aprovado e qual detalhe verdadeiro deste produto ajuda a provocar exatamente esse avanço?</code> Ligar esse detalhe ao desejo em linguagem natural, simples, específica e compreensível de primeira por uma criança de 10 anos. Escrever para o lead/espectador, preservando NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO e a MENSAGEM\_CENTRAL e a mesma história da fala/cena, descrição e micro-CTA. Não criar necessidade, ocasião, benefício ou promessa sem sustentação.

Características observáveis ou documentadas podem e devem entrar quando cumprem essa ligação; não transformar a frase em ficha técnica, lista de atributos ou explicação isolada. Esta regra substitui a proibição anterior de mencionar características no texto/título na tela. Manter concisão e leitura fácil, sem encurtar a ponto de perder o sentido. Entregar em MAIÚSCULAS. Regra de tamanho: alvo preferencial de até 50 caracteres; limite absoluto de 60 caracteres, contando letras, números, espaços e pontuação. Se exceder 60, a peça é inválida e deve ser reescrita antes do TEXT\_ELEMENTS\_GATE.

Exemplo de formato dentro do limite: “ESSA PANTALONA TEM CORES PARA COMBINAR COM SUA BLUSA”. Usar a afirmação de variedade somente quando comprovada. O exemplo demonstra ligação entre informação real e desejo, sem servir de fórmula fixa para todo produto.

Esta regra se aplica ao TEXTO/TÍTULO NA TELA da modalidade QWE. A DESCRIÇÃO + HASHTAGS continua sendo uma peça distinta com seu contrato AIDA. O texto na tela é aplicado na edição/publicação; não orienta inserir legendas ou overlays no prompt de geração do vídeo-base e não substitui o contrato da capa.

# MICRO-CTA

<b>ESCOPO: QWE.</b> No MOV, aplicar exclusivamente o CONTRATO ATIVO POR MODALIDADE.

Máximo 30 caracteres, em MAIÚSCULAS. Contar letras, espaços e pontuação. Os primeiros 20 caracteres — ou a micro-CTA inteira, se tiver menos de 20 — devem comunicar sozinhos a ação ou o destino do link, sem depender dos caracteres seguintes para fazer sentido. Validar lendo apenas esse trecho inicial; se a ação ou destino não ficar claro, reescrever. O texto completo deve continuar verdadeiro e coerente com o produto/destino.

# DESCRIÇÃO + HASHTAGS — REGRA UNIVERSAL SAC

<b>ESCOPO: QWE.</b> No MOV, aplicar exclusivamente o CONTRATO ATIVO POR MODALIDADE.

A DESCRIÇÃO deve materializar a DOR ou o DESEJO real da pessoa e provocar reconhecimento imediato: <code>caramba... isso é sobre mim; isso foi pra mim.</code> Antes de escrever, identificar o motivo real pelo qual aquela pessoa ainda está olhando o produto. A descrição não repete o título nem vira explicação ou ficha técnica do produto; ela expressa esse motivo em linguagem simples, concreta e compreensível por uma criança de 10 anos, incorporando naturalmente palavras-chave reais do produto. Deve continuar diretamente a conversa aberta pelo TEXTO/TÍTULO NA TELA. Se puder servir quase igual para qualquer produto, reescrever.

Descrição: máximo 400 caracteres, contando espaços, pontuação e quebras de parágrafo, sem contar as hashtags. Deve ter exatamente quatro parágrafos AIDA; a primeira letra de cada palavra em cada parágrafo deve estar em maiúscula. Cada um dos quatro parágrafos AIDA deve começar obrigatoriamente com um emoji semanticamente coerente com o produto, o contexto, a emoção ou a situação descrita. O emoji vem antes de qualquer letra ou palavra. Os emojis devem reforçar significado, não decorar. É proibido usar emoji genérico, aleatório, repetitivo, infantilizado ou sem conexão semântica com a mensagem. Emojis não substituem palavras, evidência, clareza nem etapa AIDA.

Aplicar sempre AIDA em exatamente quatro parágrafos, nesta ordem, sem títulos ou rótulos: 1) Atenção — abre a conversa compatível com o NEXT\_ADVANCE aprovado; 2) Interesse — conecta essa direção à situação do roteiro; 3) Desejo — reforça o valor sustentado pela evidência e pela MENSAGEM\_CENTRAL quando aplicável; 4) Ação — conduz ao próximo avanço aprovado com naturalidade, clareza e sem pressão comercial. Cada parágrafo cumpre sua etapa própria; não juntar etapas no mesmo parágrafo nem omitir uma delas.

O AIDA organiza a descrição e permanece subordinado à lei fundamental do SAC, à MENSAGEM\_CENTRAL vigente, ao NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO, ao título e ao roteiro aprovado. Não cria necessidade, benefício, promessa ou ângulo sem sustentação, não presume estágio de consciência e não usa linguagem de venda explícita. A ação não pode ser vaga nem depender de subentendido.

Inserir palavras-chave do produto dentro da própria descrição, de forma natural: nome ou tipo do produto e termos específicos sustentados pelos materiais, quando pertinentes à mensagem. Não basta colocá-las somente nas hashtags ou na peça separada de palavras-chave. Não inventar atributos, não acumular termos de busca artificialmente e não desviar do ângulo apenas para incluir palavras-chave. Condensar cada parágrafo sem fundir as quatro etapas; preservar quatro parágrafos legíveis e o limite total.

Selecionar e validar as hashtags exclusivamente pela DIRETRIZ PRIORITÁRIA — HASHTAGS SAC desta página. Não criar outra quantidade ou hierarquia de seleção nesta seção.

Descrição e hashtags formam uma única peça.

# PALAVRAS-CHAVE

<b>ESCOPO: QWE.</b> No MOV, aplicar exclusivamente o CONTRATO ATIVO POR MODALIDADE.

Exatamente 3, capitalização natural. Selecionar somente as três frases-chave mais fortes, específicas e relevantes do produto e da MENSAGEM\_CENTRAL vigente. Cada uma deve representar busca, produto, tipo, variação, desejo ou contexto real sustentado pelos materiais; não inventar função, efeito, promessa ou termo genérico apenas para completar quantidade.

Na entrega dos ELEMENTOS DE TEXTO, cada uma das 3 frases-chave deve ficar em seu próprio bloco Markdown copiável, separada das demais. É proibido colocar as três juntas no mesmo bloco.

# CAPA DO VÍDEO

A CAPA DO VÍDEO é obrigatória em toda execução, mas não faz parte do pacote inicial de ELEMENTOS DE TEXTO. Ela é sempre o último artefato a ser criado. É proibido solicitar, definir, gerar ou apresentar a capa antes de <code>TEXT_ELEMENTS_GATE=1</code>.

## OBJETIVO PRINCIPAL DA CAPA — REGRA CANÔNICA

A função principal da capa é fazer o lead certo escolher aquele vídeo para assistir antes mesmo de consumir o conteúdo. A capa deve funcionar como a porta de entrada da conversa mental do vídeo: em leitura imediata, o lead precisa reconhecer que aquele conteúdo fala com a situação, desejo, dúvida, interesse ou avanço definido pela MENSAGEM\_CENTRAL.

A capa não existe para vender o produto, explicar características, resumir ficha técnica, inserir CTA comercial, mandar comprar, clicar, escolher variação ou repetir o nome do produto sem função. Ela deve transformar a MENSAGEM\_CENTRAL do vídeo em uma frase visual de impacto que faça o lead se reconhecer e querer abrir/assistir o vídeo.

Regra operacional: <code>COVER_PRIMARY_OBJECTIVE = LEAD_RECOGNITION_TO_WATCH</code>.

Antes de definir o texto da capa, perguntar internamente: <code>Ao olhar esta capa por 1 segundo, o lead certo pensa “isso é pra mim / isso é exatamente o que eu estava pensando” e sente vontade de assistir?</code> Se a resposta não for inequivocamente SIM, <code>COVER_TEXT_READY=FALSE</code> e o texto deve ser refeito.

A imagem base da capa deve ser exatamente a mesma imagem aprovada no <code>IMAGE_GATE</code> e usada como base do roteiro. Não substituir a imagem aprovada por outra composição, produto, influencer ou cenário.

## ÂNCORA OBRIGATÓRIA DA CAPA — IMAGEM APROVADA DO ROTEIRO

Antes de qualquer <code>COVER_READY</code> ou <code>COVER_GEN</code>, o agente deve solicitar ao usuário o envio da <b>imagem exata aprovada do roteiro</b> que será usada como âncora da capa. É proibido criar, regenerar, reconstruir, reinterpretar ou inferir essa imagem apenas a partir do contexto anterior, descrição textual, memória, referências antigas ou conceito do roteiro.

Regra operacional: <code>COVER_ANCHOR_IMAGE_RECEIVED=TRUE</code> somente quando o usuário tiver enviado na etapa da capa a própria imagem aprovada do roteiro. Sem essa imagem recebida explicitamente nesta etapa, <code>COVER_READY=FALSE</code> e a capa não pode ser gerada.

A geração da capa deve tratar a imagem recebida como base visual imutável. É permitido editar somente a camada de texto e seus elementos gráficos de suporte. É proibido alterar influencer, rosto, cabelo, corpo, produto, roupa, pose, expressão, cenário, iluminação, enquadramento, proporções, composição ou qualquer detalhe visual da imagem-base.

Equação operacional canônica: <code>CAPA = IMAGEM APROVADA DO ROTEIRO + CAMADA DE TEXTO APENAS</code>.

A capa deve conter texto curto na própria imagem, pensado para reforçar o mesmo assunto semântico do vídeo e ajudar a manter alinhados: capa, vídeo, descrição, hashtags, palavras-chave e mensagem central da execução.

O texto da capa deve ser simples, concreto, específico e compreensível por uma criança de 10 anos; deve conversar diretamente com o pensamento da pessoa que já está olhando o produto. Não pode ser genérico, abrir outro ângulo, mudar promessa ou desejo, criar outro público, sugerir outro produto ou contradizer o roteiro aprovado.

A CAPA permanece subordinada ao NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO e à MENSAGEM\_CENTRAL vigente, ao roteiro aprovado, às peças textuais aprovadas da modalidade e à lei fundamental do SAC.

## DIRETRIZ VISUAL CANÔNICA DA CAPA

Antes de qualquer <code>COVER_GEN</code>, estas regras devem ser lidas e aplicadas integralmente. Falha em qualquer item mantém <code>COVER_READY=FALSE</code>.

<b>PROPORÇÃO / FORMATO</b>

- Toda CAPA DO VÍDEO deve ser criada obrigatoriamente no formato vertical de vídeo TikTok: <b>9:16</b>.
- É proibido gerar capa quadrada, horizontal ou em qualquer proporção diferente de 9:16.
- A capa deve preservar a composição da imagem aprovada, adaptada ao canvas vertical sem cortar produto, influencer ou elementos essenciais da cena.
- Check obrigatório: <code>COVER_ASPECT_RATIO = 9:16</code>.
- Se a geração retornar proporção diferente, a capa é inválida e <code>COVER_READY=FALSE</code> até nova tentativa correta.

<b>POSICIONAMENTO</b>

- O bloco completo de texto deve ficar no <b>centro geométrico da imagem</b>, centralizado horizontal e verticalmente na composição.
- Não basta estar centralizado apenas na horizontal.
- É proibido deixar o texto concentrado na faixa inferior, “caído” sobre o busto ou deslocado para baixo.
- O conjunto tipográfico deve ocupar a faixa central da capa de forma visualmente equilibrada.

<b>TIPOGRAFIA / ESTILO</b>

- Texto sempre em <b>CAIXA ALTA</b>.
- Usar tipografia <b>muito grossa, forte, condensada ou de alto impacto</b>, típica de thumbnail/capa de vídeo de resposta imediata.
- Priorizar máxima legibilidade em tela pequena. Texto fino, elegante demais, manuscrito ou de baixo contraste = bloqueado.
- O bloco deve ter aparência de <b>camadas de impacto</b>, não de texto simples corrido.

<b>CORES E CONTRASTE</b>

- Base padrão: <b>branco</b> nas linhas secundárias.
- Palavra ou linha principal: <b>amarelo/dourado</b> para maior destaque.
- Aplicar <b>contorno preto forte</b> em todo o texto.
- Aplicar <b>sombra pesada / drop shadow</b> para separação clara do fundo.
- Pode usar <b>faixa/pincelada amarela</b> atrás da palavra ou linha principal e <b>glow/brilho amarelo</b> ou elementos gráficos curtos de ênfase quando melhorarem a leitura.
- É proibido usar cores que reduzam contraste ou façam o texto competir visualmente com o produto.

<b>HIERARQUIA</b>

- A palavra ou linha que contém o núcleo da mensagem deve ser a mais chamativa do bloco.
- As demais linhas devem sustentar a leitura em hierarquia visual claramente inferior.
- O destaque principal deve permanecer subordinado à MENSAGEM\_CENTRAL; não pode criar outra promessa, desejo, ângulo ou público.

<b>PRESERVAÇÃO DA IMAGEM</b>

- <code>COVER_GEN</code> deve editar exclusivamente o texto e seus elementos gráficos de suporte.
- A capa deve usar obrigatoriamente a mesma influencer oficial da imagem aprovada no <code>IMAGE_GATE</code>; é proibido substituir, trocar, reinterpretar ou gerar outra mulher.
- Não alterar influencer, produto, cenário, enquadramento, roupa, pose, iluminação, proporção, expressão ou composição da imagem-base.
- Check obrigatório da capa: <code>INFLUENCER_OFFICIAL_ONLY = TRUE</code>.
- Qualquer modificação visual fora da camada textual, inclusive troca de identidade da influencer, invalida a capa.

<b>CHECK OBRIGATÓRIO ANTES DA GERAÇÃO</b>

Confirmar internamente:

<code>SAME_IMAGE=TRUE | CENTER_GEOMETRIC=TRUE | UPPERCASE=TRUE | TYPOGRAPHY_IMPACT=TRUE | WHITE_YELLOW=TRUE | BLACK_OUTLINE=TRUE | HEAVY_SHADOW=TRUE | HIERARCHY_OK=TRUE | MESSAGE_CONTINUITY=TRUE</code>

Se qualquer termo não for TRUE: <code>COVER_READY=FALSE</code> e não gerar a capa.

## ROTA TÉCNICA DA CAPA

Os estados, as pré-condições operacionais e as transições da capa pertencem ao Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md): HANDLER — TEXT\_ELEMENTS\_GATE, COVER\_WAIT\_ANCHOR\_IMAGE, COVER\_READY, COVER\_GEN e COVER\_GATE. Aplicar esses handlers, incluindo preservação dos artefatos aprovados, regressão mínima, tratamento de falha da ferramenta e recuperação da interface. A aprovação da capa encaminha ao fechamento do Lifecycle, conforme o Runtime.

Esta página mantém os critérios próprios: OBJETIVO PRINCIPAL DA CAPA, ÂNCORA OBRIGATÓRIA e DIRETRIZ VISUAL CANÔNICA. A rota operacional não é redefinida aqui.

# FORMATAÇÃO

QWE: entregar juntas as quatro peças definidas no CONTRATO ATIVO POR MODALIDADE. TEXTO/TÍTULO, MICRO-CTA e DESCRIÇÃO + HASHTAGS ficam cada um em bloco Markdown copiável próprio, contendo somente o conteúdo final. PALAVRAS-CHAVE segue seu contrato de três frases-chave em blocos individuais.

MOV: entregar os três itens nos blocos separados definidos no CONTRATO ATIVO POR MODALIDADE, sem transplantar a composição QWE. Identificações e gates ficam fora dos blocos.

Depois da aprovação do conjunto exigido pela modalidade, seguir a rota de capa do Runtime. A capa é o último artefato e usa a imagem aprovada, conforme seu contrato nesta página.

# COERÊNCIA

Regra comum SAC: vídeo, peças exigidas pela modalidade e capa do vídeo devem pertencer ao mesmo avanço principal e respeitar as decisões estratégicas aprovadas da execução. A abertura derivada do Pacote Criativo aprovado orienta apenas os primeiros três segundos do roteiro; todas as peças preservam a mesma MENSAGEM\_CENTRAL, sem migrar para outro ângulo, diluir a decisão ou introduzir nova interpretação criativa.

<b>ESCOPO QWE PARA O TÍTULO:</b> o título verbaliza a conversa mental já em curso; a descrição materializa a dor/desejo e o motivo real que mantém a pessoa olhando o produto. <b>REGRA DE PONTO DE VISTA DO TÍTULO:</b> no QWE, a influencer estará com o produto — usando, segurando, vestindo, aplicando ou mostrando conforme a categoria. Por isso, o TEXTO/TÍTULO NA TELA deve ser sempre escrito para o lead/espectador, nunca como pensamento em primeira pessoa da influencer sobre ela mesma. O título deve fazer quem assiste se projetar na cena, imaginar-se com o produto ou reconhecer a própria decisão. Evitar construções como “EU JÁ ME VEJO USANDO...”. Preferir formulações dirigidas ao espectador, como “VOCÊ JÁ SE IMAGINOU USANDO...”, quando compatíveis com a MENSAGEM\_CENTRAL, as decisões estratégicas aprovadas, a evidência e o roteiro aprovado. Antes do TEXT\_ELEMENTS\_GATE, conferir obrigatoriamente: <code>TITLE_POV = LEAD</code>. Se o título estiver na perspectiva da influencer em vez da perspectiva do lead, reescrever. Peça que serviria quase sem alteração para qualquer produto deve ser refeita.

No MOV, aplicar a primeira pessoa e a chamada provocativa conforme o CONTRATO ATIVO POR MODALIDADE; TITLE\_POV=LEAD não se aplica à frase pessoal MOV.

# TEXT\_ELEMENTS\_OUTPUT\_CHECK — BARREIRA OBRIGATÓRIA

Barreira interna obrigatória antes da apresentação. Validar somente as peças do CONTRATO ATIVO POR MODALIDADE da execução, sem exigir peças QWE no MOV nem o inverso.

<b>CHECKS COMUNS:</b> quantidade e blocos copiáveis corretos; limites de cada peça; clareza, SAC SAFE, fidelidade comercial, valor simbólico quando aplicável; mesma revisão da MENSAGEM\_CENTRAL, direção interna fundamentada, objetivo, mecanismo, evidências e roteiro aprovado. Abertura e peças devem ter continuidade de sentido, sem exigir palavras idênticas. Não alterar silenciosamente o roteiro para acomodar texto divergente.

<b>QWE:</b> conferir integralmente as seções TEXTO/TÍTULO, MICRO-CTA, DESCRIÇÃO + HASHTAGS, PALAVRAS-CHAVE, FORMATAÇÃO e COERÊNCIA. Isso inclui título afirmativo completo e dirigido ao lead, tamanho permitido, relação entre detalhe real e desejo; descrição de reconhecimento com quatro parágrafos AIDA, capitalização, emojis, limite e termos reais do produto; micro-CTA compreensível e frases-chave pertinentes.

<b>MOV:</b> conferir integralmente os três itens, formatos, limites, perspectiva pessoal, emoji e nome do produto conforme o CONTRATO ATIVO POR MODALIDADE. Não aplicar título tradicional, TITLE\_POV=LEAD, descrição AIDA ou palavras-chave separadas ao MOV.

<b>HASHTAGS:</b> aplicar somente a DIRETRIZ PRIORITÁRIA — HASHTAGS SAC.

<b>RESULTADO:</b> qualquer falha textual define TEXT\_ELEMENTS\_GATE=BLOCKED e retorna a TEXT\_ELEMENTS\_PREP para corrigir somente as peças inválidas; não apresentar defeito detectável internamente nem pedir aprovação para corrigi-lo. Repetir até PASS ou ausência real de informação/evidência; nesse caso pedir somente o dado faltante. Somente PASS permite apresentar o conjunto e abrir o gate pelo Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md).

A capa ainda não existe nesta checagem. Falhas posteriores exclusivas da capa seguem seus handlers no Runtime, preservando imagem e textos aprovados; não antecipar capa nem reabrir seus gates por falha exclusiva de capa.

# TEXT\_ELEMENTS\_GATE

Após PASS na validação interna, apresentar as peças da modalidade vigente e delegar a decisão ao HANDLER — TEXT\_ELEMENTS\_GATE e ao ADAPTADOR\_DE\_INTERFACE do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Somente o usuário aprova.

Na correção textual, alterar somente a peça indicada; se o pedido for pelo conjunto inteiro, refazer todas as peças exigidas pela modalidade conforme o CONTRATO ATIVO POR MODALIDADE. Se não houver motivo da rejeição, solicitar somente o que deseja mudar.

A aprovação não inicia nova execução: encaminha à etapa de âncora da capa conforme o handler vigente. O encerramento depende da aprovação da capa.

# FORMATO OBRIGATÓRIO DA DESCRIÇÃO — AIDA EM 4 PARÁGRAFOS

<b>ESCOPO: QWE.</b> Aplicar integralmente o contrato DESCRIÇÃO + HASHTAGS desta página, que concentra a ordem e quantidade de parágrafos AIDA, capitalização, emojis, palavras-chave no texto e limite total. A conferência ocorre em TEXT\_ELEMENTS\_OUTPUT\_CHECK. No MOV, aplicar seu contrato próprio.

## CONFERÊNCIA INTERNA — ESTRUTURA AIDA

<b>ESCOPO: QWE.</b> Conferir os requisitos de DESCRIÇÃO + HASHTAGS na barreira TEXT\_ELEMENTS\_OUTPUT\_CHECK; esta seção não mantém outro checklist. A estrutura AIDA textual não é exigida no MOV.
