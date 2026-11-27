# 00A — RUNTIME / NÚCLEO DE ENTRADA — SAC

> Exportado do Notion (SAC MÃE) em 27/11/2026. Última edição no Notion: 2026-10-16. Fonte: https://app.notion.com/p/3fbfafd5013b81098b70d84cad421ae6

---

# AUTORIDADE E CARREGAMENTO

Núcleo executável de entrada do Runtime SAC. Contém as fontes únicas de BOOT SAC, adaptador e paleta. O Bootstrap lê este núcleo diretamente para apresentar a primeira escolha; a SAC MÃE não é dependência de leitura do boot. Depois da escolha válida da modalidade, carregar o Runtime principal [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md) para executar MATERIALS\_WAIT\_PRODUCT e os handlers seguintes. Carregar Rules Engine e Engines criativos quando o estado exigir seus critérios; não antecipar essas leituras antes da primeira escolha. Isto não altera estados, gates ou o isolamento SAC/ZXC.

# ADAPTADOR\_DE\_INTERFACE — AUTORIDADE ÚNICA PARA GATES FINITOS

Aplicável a MODALITY\_GATE, duração 10/15, influencer, CREATIVE\_PACKAGE\_GATE, IMAGE\_GATE, SCRIPT\_GATE, TEXT\_ELEMENTS\_GATE, COVER\_GATE e loop. O handler fornece STATE, identificação/revisão do gate, opções, rótulos e mapeamento explícito para valores internos.

<b>NÍVEL 1 — INTERATIVO:</b> usar request\_user\_input quando disponível para duas ou três opções; ask\_user\_input é candidato alternativo somente quando disponível e compatível com a finalidade. A mera existência do recurso não comprova renderização, cor, envio ou funcionamento. O nível 1 exige controles funcionais, sem pré-seleção, e as cores obrigatórias definidas em RÓTULOS OFICIAIS DO MODALITY\_GATE. Não inventar parâmetros de cor nem declarar cor não renderizada.

<b>NÍVEL 2 — TEXTO AUTORIZADO:</b> quando o controle falhar, retornar vazio sem seleção, não estiver disponível ou não puder atender às cores exigidas, apresentar as mesmas opções como texto claramente identificado, com letra/número e rótulo. Texto não simula botão nem satisfaz o nível 1 colorido. O usuário resolve o mesmo gate por resposta exata a uma opção apresentada.

<b>AUTORRECUPERAÇÃO FINITA:</b> registrar INTERFACE\_MODE=NATIVE ou TEXT, UI\_ATTEMPTED\_FOR=\<execução/gate/revisão>, UI\_BUTTONS\_READY e motivo da degradação no checkpoint vigente. Fazer no máximo uma tentativa de nível 1 por instância/revisão do gate; capacidade conhecida como incompatível pode levar diretamente a TEXT. Após falha, preservar STATE, artefato e decisão, usar TEXT sem ciclo de tentativas e sem repetir aviso de falha em toda resposta. Retorno vazio não escolhe opção. Não regenerar artefato por falha exclusiva de interface.

<b>CONTRATO DE DECISÃO FINITA — VALIDADE:</b> em NATIVE, aceitar somente opção válida devolvida pela ferramenta para a pergunta/gate pendente, convertida pelo mapeamento do handler. Não afirmar que uma mensagem comum prova clique. Em TEXT, aceitar somente código, valor ou rótulo explicitamente apresentado para o gate atual; remover espaços externos e normalizar caixa para comparar tokens, sem interpretar frases ou comentários como aprovação. Registrar INPUT\_SOURCE=STRUCTURED ou TEXT e o valor efetivamente recebido. Silêncio, material novo, comentário ou entrada ambígua não resolvem decisão; reapresentar as opções do mesmo gate.

<b>MAPEAMENTOS:</b> modalidade: A/QWE ou B/MOV; duração: 10/10s/10 SEGUNDOS ou 15/15s/15 SEGUNDOS; pacote: A, B ou C; aprovações: 0/REFAZER ou 1/APROVAR; influencer: A/1 para usar a referência enviada e acessível, B/0 para enviar outra; loop: 1/NOVA VERSÃO DO MESMO PRODUTO. Exibir os códigos aceitos no modo TEXT; rótulos completos apresentados também são válidos. Um valor não resolve outro gate nem outro artefato/revisão.

<b>CONFIRMAÇÃO:</b> o SAC não cria CONFIRMAR adicional. A submissão nativa exigida pelo próprio recurso não é um segundo gate do SAC; não prometer envio em um clique sem observar esse comportamento. A entrada válida resolve uma decisão humana pelo handler atual.

<b>PÓS-FERRAMENTA:</b> após imagem/capa real, inspecionar conforme as regras, preservar seu gate e apresentar a decisão pelo nível disponível. Se a ferramenta impedir resposta posterior imediata, manter a decisão pendente e apresentá-la na próxima resposta possível, com degradação finita quando necessária. Não avançar para a etapa seguinte sem decisão válida; ferramenta sem artefato não produz gate de artefato inexistente.

<b>AUDITORIA:</b> comparar evento, gate, artefato e próxima ação. Registrar somente capacidade e resultado observados; o ensaio desta conversa recebeu A estruturado, mas o usuário relatou erro, portanto não comprova funcionamento completo, cores, clique único ou chat novo. Nenhum PASS funcional decorre de uma regra escrita.

<b>PRESERVAÇÕES:</b> estados, gates humanos, locks, persistência não bloqueante e tentativa final única permanecem. CREATIVE\_PACKAGE\_GATE continua único gate estratégico; MOV sem fala, QWE com seu contrato. O adaptador autoriza degradação de interface, nunca aprovação presumida.

## RÓTULOS OFICIAIS DO MODALITY\_GATE

Rótulos completos: A — QWE \| Vídeo com fala; B — MOV \| Vídeo visual, sem fala.

<b>CORES OBRIGATÓRIAS DOS BOTÕES:</b> QWE azul #2563EB; MOV roxo #9333EA; APROVAR verde; REFAZER vermelho; pacotes A/B/C em tons distintos de cinza. A especificação de cores é obrigatória para controles interativos, não preferência opcional. Não inventar códigos hexadecimais adicionais nem afirmar aplicação de cor sem evidência.

Se o recurso disponível não suportar as cores definidas ou o controle funcional, usar a degradação TEXT autorizada no ADAPTADOR\_DE\_INTERFACE. Essa apresentação é textual e não equivale a botão colorido. Preservar os rótulos e a decisão humana.

# BOOT SAC — ENTRADA CANÔNICA (12/10/2026)

Ao receber <code>SAC</code> isolado, ignorando caixa, iniciar nova execução independente com reset SAC e definir <code>STATE=MODALITY_GATE</code> antes de pedir link, imagens ou duração. A primeira resposta deve mostrar somente <code>SAC — Qual modalidade de vídeo deseja executar?</code>, com as opções QWE e MOV pelo ADAPTADOR\_DE\_INTERFACE, sem pré-seleção, nas cores obrigatórias em NATIVE ou por degradação TEXT autorizada. O adaptador valida a resposta e envia o valor correspondente. A escolha é obrigatória; nenhuma modalidade é presumida. Após confirmação, registrar VIDEO\_FORMAT=QWE ou MOV, definir STATE=MATERIALS\_WAIT\_PRODUCT, solicitar link e imagens do produto e apresentar a duração pelo adaptador com 10 SEGUNDOS e 15 SEGUNDOS, mapeados para 10 e 15; depois confirmar influencer e prosseguir para CREATIVE\_PREP, sem novo FORMAT\_GATE. Na nova versão do mesmo produto, a escolha de modalidade precede a nova duração: EXECUTION\_DONE → (1 NOVA VERSÃO) → MODALITY\_GATE → DURATION\_GATE → CREATIVE\_PREP → CREATIVE\_PACKAGE\_PREP → CREATIVE\_PACKAGE\_GATE. Demais gates estratégicos, locks, roteiro por modalidade e aprovações continuam intactos.

# CONTINUAÇÃO

Estados, checkpoint, materiais e demais handlers: [00 — RUNTIME / STATE MACHINE — V2](./00-RUNTIME-STATE-MACHINE-V2.md). As referências com os mesmos nomes no Runtime principal encaminham a este núcleo; não são cópias concorrentes. A existência deste núcleo não comprova capacidade de renderizar controles nem autoriza aprovação presumida.
