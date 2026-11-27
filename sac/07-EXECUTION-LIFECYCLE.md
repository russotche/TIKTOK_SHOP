# 07 — EXECUTION LIFECYCLE — FASE 5

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-11-04. Fonte: https://app.notion.com/p/326fafd5013b8315bf8481c969d6ef4a

---

## POLÍTICA CANÔNICA DE FECHAMENTO — SEM REGISTRO INDIVIDUAL NO NOTION (DECISÃO 19/10/2026)

<b>Prevalência:</b> por decisão explícita do usuário, o Runtime de 19/10/2026 prevalece sobre qualquer instrução desta página que exija criar, consultar, atualizar ou sincronizar linhas do Registro Ativo, checkpoints, snapshots, logs ou registros individuais por vídeo. Não criar nem atualizar registros individuais no Notion em nenhuma fase da execução.

<b>Autoridade preservada do Lifecycle:</b> esta página continua sendo a única autoridade para calcular, incrementar uma única vez, preservar e resetar os contadores de rastreabilidade do CREATIVE\_PACKAGE\_GATE. Os contadores, a sequência e os marcadores de idempotência (incluindo COUNTERS\_COMMITTED e ARCHIVE\_WRITE\_ATTEMPTED) são mantidos somente no estado da conversa. ARCHIVE\_WRITE é uma operação lógica de fechamento em memória: após COVER\_GATE=1, consolidar artefatos aprovados e atualizar os contadores em memória, então seguir para EXECUTION\_DONE. Não há chamada de escrita no Notion, linha terminal, tentativa de sincronização ou estado de sincronização pendente.

<b>Nova versão e nova execução:</b> preservar os contadores do mesmo produto e iniciar a sequência da nova versão zerada; para novo produto/nova execução independente, aplicar o reset dos contadores e da sequência conforme as regras desta página. Todo reset e toda continuidade ocorrem no estado da conversa, sem marcar linhas como Resetada e sem criar linha Ativa.

<b>Escopo preservado:</b> permanecem inalterados os critérios de contagem (somente seleção humana A/B/C em CREATIVE\_PACKAGE\_GATE; contabilizar somente versão concluída com COVER\_GATE aprovado), a idempotência, a transição COVER\_GATE=1 → ARCHIVE\_WRITE → EXECUTION\_DONE, a opção de nova versão do mesmo produto e todas as autoridades de entrada, Runtime, Rules Engine, Creative Engine, Text Engine e interface. O arquivo passivo 09 permanece sem autoridade operacional.

<b>Leitura de legado:</b> instruções abaixo que mandem gravar no Registro Ativo, criar nova linha Ativa, resetar linha anterior, consultar registros para recuperar contadores ou anunciar sincronização pendente ficam sem efeito operacional na extensão em que conflitem com esta política.

---

## RASTREABILIDADE DO PACOTE — REGRA ATIVA

Para novas versões, contar somente uma escolha A/B/C em <code>CREATIVE_PACKAGE_GATE</code> por execução concluída; manter idempotência de <code>COUNTERS_COMMITTED</code>. Mensagem, abertura e conceito derivam da opção escolhida e não têm contadores humanos independentes. Recomeçar o loop escolhendo modalidade/duração e formando novo pacote.

# AUTORIDADE

Fonte canônica da V2 para encerramento, reset e início de uma nova execução SAC. Não define territórios criativos paralelos nem cria categorias obrigatórias de vídeo.

Fontes relacionadas: entrada e interface [00A — RUNTIME / NÚCLEO DE ENTRADA — SAC](./00A-RUNTIME-NUCLEO-DE-ENTRADA.md); estados [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md); evidências/locks [02 — RULES ENGINE / CREATIVE READINESS — FASE 2](./02-RULES-ENGINE.md); audiovisual [04 — CREATIVE ENGINE / ROTEIRO — FASE 3](./04-CREATIVE-ENGINE-ROTEIRO.md); textos/capa [06 — ELEMENTOS DE TEXTO ENGINE — FASE 4](./06-ELEMENTOS-DE-TEXTO-ENGINE.md); fechamento [07 — EXECUTION LIFECYCLE — FASE 5](./07-EXECUTION-LIFECYCLE.md).

# CONTADORES DE RASTREABILIDADE — REGRA CANÔNICA

Esta página é a única autoridade para incremento, preservação e reset dos contadores de rastreabilidade. Há contagem independente por produto somente para o gate humano CREATIVE\_PACKAGE\_GATE e letra A/B/C. OBJECTIVE e MECHANISM são campos automáticos, não contadores de escolha humana.

A contagem registra somente versões com capa aprovada. Aplicar uma única vez o algoritmo completo da seção ARCHIVE\_WRITE → EXECUTION\_DONE desta página; esta seção não contém outra rotina de fechamento.

Na nova versão do mesmo produto pelo loop autorizado, preservar os contadores vigentes e iniciar a nova sequência zerada. Criar a nova linha <code>Ativa</code> copiando para seu checkpoint os contadores vigentes da versão concluída no estado atual do Runtime; não consultar linhas terminais nem o arquivo passivo para recuperá-los. Em novo produto ou nova execução SAC pelo despacho canônico, zerar os contadores e a sequência.

O Runtime consulta estes valores para exibir as pistas <code>{[n]}</code> e não altera os contadores. O Lifecycle é a autoridade do incremento e da marca idempotente. A gravação terminal no Registro Ativo deve ser tentada antes da resposta final; falha de escrita gera sincronização pendente e preserva os valores no estado da conversa, sem bloquear <code>EXECUTION_DONE</code>, a conclusão ou o loop. O Registro Ativo conserva os valores persistidos quando a escrita tem sucesso; ele não cria recomendações nem aprendizado automático.

# ARCHIVE\_WRITE → EXECUTION\_DONE

Somente após <code>COVER_GATE=1</code> a versão criativa atual é considerada concluída para fins de artefato. A transição operacional obrigatória é <code>COVER_GATE=1 → ARCHIVE_WRITE → EXECUTION_DONE</code>.

Após <code>COVER_GATE=1</code>, preparar em memória o fechamento da versão: artefatos aprovados, produto, modalidade, duração, pacote escolhido e contadores. Se <code>COUNTERS_COMMITTED</code> ainda não corresponder ao ID da execução, calcular uma única vez o incremento da letra escolhida no <code>CREATIVE_PACKAGE_GATE</code> e marcar <code>COUNTERS_COMMITTED=<ID_DA_EXECUÇÃO></code> no estado da conversa; esse marcador evita novo incremento e não comprova persistência no Notion. Em <code>ARCHIVE_WRITE</code>, se <code>ARCHIVE_WRITE_ATTEMPTED</code> ainda não corresponder ao ID, defini-lo no estado da conversa antes da chamada e tentar uma única atualização final na linha existente do Registro Ativo, incluindo os dois marcadores, os contadores calculados, <code>STATE=EXECUTION_DONE</code> e <code>Status=Concluída</code>. Se a tentativa já ocorreu, não repetir. Não escrever no arquivo passivo nem criar página adicional no encerramento. Se falhar, preservar todos os dados e marcadores em memória e marcar sincronização pendente, sem declarar gravação confirmada. Com sucesso ou falha, seguir para <code>EXECUTION_DONE</code>, sem reabrir gates, recalcular contadores ou bloquear o loop. Essa tentativa única abrange o fechamento após aprovação da capa; não altera checkpoints anteriores ou a criação da linha da próxima versão.

Ao entrar em <code>EXECUTION_DONE</code>:

- consumir o fechamento já preparado, sem segunda gravação e sem novo incremento;
- apresentar a conclusão e a opção de nova versão pelo adaptador mesmo se a atualização final tiver falhado;
- o registro deve conter somente dados já definidos/aprovados na execução: produto/referência, <code>SCRIPT_DURATION</code> (10s ou 15s), AUDIENCE\_CONTEXT, NEED\_DIAGNOSIS, NEXT\_ADVANCE, OBJETIVO DO CRIATIVO, MECANISMO CRIATIVO, MENSAGEM\_CENTRAL, abertura, conceito selecionado, imagem aprovada, roteiro aprovado, ELEMENTOS DE TEXTO e capa aprovada;
- não ler o arquivo antes, durante ou depois da gravação para orientar a execução;
- falha da atualização final no Registro Ativo gera sincronização pendente, sem invalidar artefatos aprovados nem reabrir gates;
- não iniciar automaticamente nova execução;
- não criar menu de tipos de vídeo;
- não selecionar estratégia, objetivo, mecanismo ou avanço para um próximo ciclo;
- após o encerramento, apresentar somente a opção <b>NOVA VERSÃO DO MESMO PRODUTO</b> pelo adaptador, conforme <code>POST_EXECUTION_LOOP</code> abaixo; o rótulo visível não exibe <code>1</code>; não oferecer novo produto nem encerramento neste chat.

<b>SAÍDA ENXUTA:</b> apresentar somente EXECUÇÃO CONCLUÍDA ✅ e a opção NOVA VERSÃO DO MESMO PRODUTO pelo adaptador; em NATIVE, sem número no rótulo; em TEXT, com o código necessário à resposta nem narrativa administrativa. O Runtime aplica o evento e a transição do loop; uma escrita sem confirmação nunca é anunciada como gravada.

Em falha da atualização final, a saída enxuta inclui uma única indicação “Sincronização pendente”, junto à conclusão e à opção de nova versão. Essa indicação torna a pendência visível, não declara gravação, não cria gate nem autoriza segunda tentativa terminal. O campo Sincronização será reconciliado somente na próxima escrita legítima.

# NOVA EXECUÇÃO — RESET OBRIGATÓRIO

Ao iniciar uma nova execução conforme a ativação canônica definida no Bootstrap/Runtime:

- marcar como <code>Resetada</code> a linha anterior ainda não terminal, registrando <code>novo SAC</code> como motivo;
- criar uma nova linha <code>Ativa</code> no Registro Ativo antes de solicitar materiais;
- iniciar uma nova execução independente;
- zerar materiais ativos, evidência, <code>SCRIPT_DURATION</code>, AUDIENCE\_CONTEXT, CONTEXT\_READING, NEED\_DIAGNOSIS, NEXT\_ADVANCE e sua aprovação, OBJETIVO DO CRIATIVO e sua aprovação, MECANISMO CRIATIVO e sua aprovação, MENSAGEM\_CENTRAL e sua aprovação/revisão;
- zerar opções de abertura A–C, <code>OPENING_STYLE_SELECTED</code>, <code>OPENING_STYLE_OK=FALSE</code>, variantes de conceito A–C, <code>CONCEPT_SELECTED</code>, <code>CONCEPT_APPROVED=FALSE</code>, <code>CONCEPT_OK=FALSE</code>, <code>IMAGE_READY</code>, imagem candidata e imagem aprovada;
- zerar roteiro, validações de roteiro, ELEMENTOS DE TEXTO, validações textuais, texto de capa, capa candidata, capa aprovada, referências e checkpoints <code>COVER_*</code>;
- definir <code>COVER_TEXT_READY=FALSE</code>, <code>COVER_READY=FALSE</code>, <code>COVER_APPROVED=FALSE</code>, <code>PAUSED=FALSE</code>;
- limpar o STATE de retorno da pausa e decisões de gates da execução anterior;
- delegar o estado inicial e a solicitação de materiais ao BOOT SAC e handlers do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md), com modalidade antes da coleta;
- não reutilizar automaticamente link, imagens, influencer, evidência, abertura, estratégia ou qualquer aprovação anterior.

Depois do reset de dados, seguir exclusivamente os handlers iniciais e a sequência estratégica automática do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). Cada nova execução SAC é independente; decisões e aprovações da anterior não governam a seguinte.

# REGRA DE NÃO-HERANÇA

Nenhum contexto de audiência, diagnóstico, avanço, objetivo, mecanismo, mensagem central, abertura, conceito, imagem, roteiro, ELEMENTO DE TEXTO ou capa de execução anterior pode ser tratado como vigente ou aprovado em uma nova execução sem ser reconstruído ou passar novamente pelo gate correspondente. O arquivo passivo não pode ser usado como fonte para preencher essas informações.

# POST\_EXECUTION\_LOOP — MESMO PRODUTO

Após <code>COVER_GATE=1</code> e entrada em <code>EXECUTION_DONE</code>, o QWE nunca oferece encerrar e nunca oferece novo produto neste mesmo chat. A continuidade funciona exclusivamente em loop para criar uma nova versão do mesmo produto.

Ao finalizar uma execução, mostrar obrigatoriamente:

<b>EXECUÇÃO CONCLUÍDA ✅</b>

<b>NOVA VERSÃO DO MESMO PRODUTO</b>

Reinicia a parte estratégica e criativa para criar outro vídeo do mesmo produto, com novo NEXT\_ADVANCE, objetivo, mecanismo, mensagem central, abertura, conceito, imagem, roteiro, ELEMENTOS DE TEXTO e capa.

Somente evento válido NOVA VERSÃO DO MESMO PRODUTO/1, conforme o nível vigente do ADAPTADOR\_DE\_INTERFACE do Runtime, inicia nova versão. Comentário, silêncio e entrada ambígua não iniciam o loop.

## ROTA ÚNICA DO LOOP

Ao receber o evento válido NOVA VERSÃO DO MESMO PRODUTO/1 conforme o ADAPTADOR\_DE\_INTERFACE:

- preservar, quando ainda disponíveis e confiáveis, o link do produto, as imagens do produto, as evidências factuais válidas e a influencer já confirmada; não exigir novo upload desses materiais apenas para iniciar outra versão do mesmo produto;
- se algum material necessário não estiver mais disponível ou confiável, pedir somente esse material específico, sem inventar nem substituir referência;
- carregar na nova linha ativa os contadores vigentes do mesmo produto conforme a regra canônica desta página; não consultar linhas concluídas nem o arquivo passivo para recuperá-los;
- zerar <code>SCRIPT_DURATION</code>, <code>AUDIENCE_CONTEXT</code>, <code>CONTEXT_READING</code>, <code>NEED_DIAGNOSIS</code>, <code>NEXT_ADVANCE</code> e sua aprovação, OBJETIVO DO CRIATIVO e sua aprovação, MECANISMO CRIATIVO e sua aprovação, MENSAGEM\_CENTRAL e sua aprovação/revisão;
- zerar abertura A–C, conceito A–C e a sequência de rastreabilidade da nova versão, preservando os contadores vigentes do mesmo produto conforme a regra canônica desta página; zerar imagem candidata/aprovada, roteiro, ELEMENTOS DE TEXTO, capa e todos os gates/checkpoints posteriores;
- criar uma nova linha Ativa no Registro Ativo com os dados e contadores preserváveis acima; delegar modalidade, duração e todas as transições seguintes ao HANDLER — EXECUTION\_DONE e ao BOOT SAC do Runtime [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md), sem manter sequência de estados paralela nesta página;
- a nova versão é uma execução criativa independente do mesmo produto, mas reaproveita somente os materiais factuais preserváveis.
