---
name: iza-ugc-realismo
description: Use ao criar imagens, vídeos ou roteiros UGC/POV da influencer Iza (@queridaizabell) para produtos do TikTok Shop no Google Flow — trava de identidade e produto, prompts anti-"cara de IA", júri de roteiro e checklist de QA antes de postar.
---

# Iza UGC Realismo

Processo para fazer vídeos da Iza que parecem filmados por uma pessoa real, sem quebrar as regras da conta.
Adaptado de três fontes públicas (ver "Créditos" no fim) e das regras do projeto (`isabell/`).

**Ordem obrigatória:** roteiro → júri → imagem base → QA da imagem → vídeo → QA do vídeo → edição → checagem pré-post.
Explique cada etapa ao usuário antes de executar e espere aprovação.

## 0. Regras fixas da conta (nunca quebrar)

- Nunca mostrar ou falar preço, frete, cupom ou valor.
- Nunca abrir com "amiga" ou "gente".
- Depoimento de uso só com avaliação real do anúncio (citar como "quem comprou tá falando…"). Nada de experiência inventada da Iza.
- Produto no vídeo = produto do anúncio (forma, cor, detalhes). Na dúvida de cor, usar só a cor que a foto do anúncio mostra.
- Sempre 9:16, maior resolução disponível, realismo total.
- Na publicação: rótulo de conteúdo gerado por IA ligado + `#publi` (CONAR).
- Nada de mamilo marcado, transparência ou pose sexual explícita: risco de moderação.

## 1. Trava de identidade — Iza

Referência oficial: `isabell/referencias/iza_rosto_oficial.jpg` (sempre a 1ª imagem anexada no Flow).

Bloco para colar em todo prompt (imagem e vídeo):

```
IDENTITY LOCK — @iza = the woman in the first reference image.
Inherit from @iza: face shape, facial features, light blue eyes, eyebrow shape, skin tone,
voluminous dark brown curly hair (loose natural curls, shoulder-length or longer, center part),
apparent age (mid-20s), body proportions.
Do NOT inherit from @iza: background, pose, framing, lighting, clothing, jewelry, makeup intensity.
Same face when turning, laughing, looking down or speaking. No feature averaging, no face swap.
```

Por que funciona: listar o que herdar E o que NÃO herdar. Sem a 2ª lista, o modelo copia fundo, pose e luz da referência, ou trata a foto só como estilo.

## 2. Trava de produto

Referência: foto do anúncio (sempre a 2ª imagem). Decompor a peça em partes, uma por uma:

```
PRODUCT LOCK — @produto = the outfit in the second reference image, 100% match.
Top: [modelo, alça, comprimento, acabamento da barra]. Bottom: [modelo, cós, comprimento, barra].
Fabric: [textura visível]. Color: [cor exata da foto do anúncio] — no other color.
No logos, no labels, no text on garments.
```

Exemplo (baby doll canelado): cropped rosa canelado de alças finas reguláveis, barra ondulada (lettuce edge); short rosa canelado com cós de elástico e barra ondulada.

## 3. Prompt de imagem base (anti-"cara de IA")

Regra central: realismo se compra com **defeitos de câmera de celular**, não com a palavra "realistic".

Estrutura:
1. **CÂMERA:** aparelho nomeado + quem filma. Ex.: "shot on an iPhone 13 held by a friend / propped on a shelf / mirror selfie". Lente 26 mm, leve distorção nas bordas.
2. **DEFEITOS:** horizonte levemente torto, enquadramento imperfeito, ruído ISO 500–900, leve desfoque de movimento, pequena mancha de dedo na lente, compressão de celular.
3. **LUZ:** luz disponível, nunca estúdio. Misturar temperaturas (janela fria + lâmpada quente, ou céu nublado). Sombras assimétricas.
4. **PELE:** poros visíveis no nariz e bochechas, brilho natural na testa, penugem na mandíbula, leve olheira, frizz e baby hairs. Sem base, sem filtro.
5. **EXPRESSÃO:** específica, nunca só "smiling". Ex.: "risada espontânea, rugas de riso no canto dos olhos, dentes com pequenas imperfeições".
6. **FUNDO:** nítido e legível (objetos reais, bagunça leve). Fundo muito desfocado = estúdio = IA.
7. **ENQUADRAMENTO:** no máximo do peito para cima no plano mais fechado. Close de rosto expõe a IA.
8. **MÃOS:** fora do quadro, paradas ou segurando algo de forma estável.
9. **DESLIGAR POLIMENTO (sempre no fim):**
   `No studio lighting, no cinematic look, no beauty filter, no skin smoothing, no retouching, no bokeh, no text, no logos, no watermark.`

Palavras proibidas no prompt: beautiful skin, perfect, flawless, studio, cinematic, 4K, professional lighting, model pose, glamour.

Não misturar no mesmo prompt "handheld/real" com "cinematic/4K": são lógicas de luz diferentes e o resultado vira plástico.

Configuração no Flow: Imagem · 9:16 · **Nano Banana Pro** · x4 (escolher a melhor de uma rodada só).

## 4. Prompt de vídeo (Flow / Veo, clipes de 8 s)

Estrutura por clipe:
1. Trava de identidade + trava de produto (blocos 1 e 2).
2. CÂMERA e defeitos (como no item 3): handheld, leve tremida, foco que "procura", exposição que respira. Sem estabilizador, sem zoom digital, sem cortes invisíveis.
3. STORYBOARD com tempo e uma fala por linha, colada na ação:

```
[0.0–0.5s] inspira, olho na lente, cabeça parada
[0.5–3.0s] (ação) + fala: "…"   ← no máximo ~8 palavras
[3.0–6.0s] (ação) + piscada natural + inclinação de cabeça
[6.0–8.0s] (ação final) + aceno curto
```

4. MICRO-MOVIMENTO: balanço leve do corpo, piscar a cada 3–5 s, cabeça inclina e acena. Personagem parada = IA.
5. MÃOS: estáveis ou fora do quadro. Nunca pedir gesto fino com a mão e caminhada no mesmo momento; separar em dois beats.
6. ÁUDIO: português do Brasil, tom animado e natural, som ambiente do lugar (rua, cozinha). Se a sincronia labial escorregar, corte a frase; não adicione adjetivo.
7. Sem texto gerado na tela (sai ilegível). Texto na tela entra na edição.

**Ritmo de fala (a testar):** a regra original é de 55–60 sílabas por 10 s em inglês. Para português em clipe de 8 s, começar com **~40–50 sílabas**, frases completas, nunca cortar no meio da frase. Ajustar depois do 1º teste.

**Fechamento de vídeo de produto:** terminar com a peça bem visível no corpo + a Iza olhando para a câmera. O CTA vem falado de passagem, não como frase de venda.

## 5. Júri de roteiro (antes de gerar qualquer coisa)

Cada roteiro passa por 6 juízes. Só vai para geração quando passa em todos. Reescrever e rodar de novo até passar.

| Juiz | Reprova se… |
|---|---|
| Gancho | os 3 primeiros segundos não fariam você parar de rolar o feed; ou começa com "amiga"/"gente" |
| Ritmo | lida em voz alta, a fala trava ou soa recitada; passa de ~8 palavras por fala |
| Voz falada | qualquer frase soa como texto de anúncio ou slogan. Preferir fala imperfeita: pausas, frase que fica no ar |
| Estrutura | não segue gancho (0–3 s) → dor/situação → prova (avaliação real) → CTA de passagem; ou passa de 20 s |
| Voz da Iza | não combina com o vídeo POV que viralizou (97 mil views): animada, espontânea, humor do dia a dia |
| Conformidade | tem preço/valor/frete/cupom; tem experiência inventada; promete algo que o anúncio não sustenta (durabilidade, cor não listada) |

Para volume, montar lotes de ~5–10 roteiros aprovados antes de abrir o Flow.

## 6. QA da imagem e do vídeo (nota 0/1/2 por item)

2 = passa · 1 = funciona com falha visível · 0 = falhou. Qualquer 0 → refazer. Mais de um 1 → avaliar com o usuário.

| Item | O que olhar |
|---|---|
| Identidade | É a Iza? Olho azul, cachos, mesmo rosto em todos os quadros |
| Produto | Peça, cor e detalhes iguais à foto do anúncio |
| Realismo | Pele com textura, luz natural, defeitos de celular; nada de plástico |
| Corpo e mãos | 5 dedos, nada derretendo, membros não somem nem aparecem |
| Continuidade | Objetos e posições só mudam por ação visível (ex.: chinelo nos pés não vira chinelo no chão) |
| Áudio | Fala em PT-BR, sincronia labial, som ambiente coerente |
| Saída | 9:16, resolução máxima, sem texto ou marca d'água geradas |
| Moderação | Sem transparência, mamilo marcado ou pose sexual |

Para cada nota 0 ou 1: dizer o segundo/ponto exato, a causa provável e uma correção só. Mudar uma coisa por vez.

## 7. Edição "de criadora"

- Tratar o que o Flow gera como material bruto de um vídeo de celular, não como anúncio pronto.
- Cortar o tempo morto do início, até a energia entrar.
- Encurtar todas as pausas.
- Legendas e textos na tela adicionados na edição (FFmpeg/Remotion/CapCut).
- Som ambiente ou trilha baixinha por baixo.
- Assistir uma vez como espectador comum: se você não pararia de rolar, o problema é o roteiro, não a edição.

## 8. Checagem pré-post

- [ ] Nenhum preço, frete, cupom ou valor (fala, texto, legenda)
- [ ] Depoimento só de avaliação real
- [ ] Produto e cor iguais ao anúncio
- [ ] 9:16, resolução máxima
- [ ] Rótulo de IA ligado + `#publi` na legenda
- [ ] Produto correto vinculado no carrinho

## Créditos

- dennisonbertram/claude-media-skills — `realistic-ugc-video` (técnicas de imperfeição, mãos, ritmo por sílabas, micro-movimento). Ideias adaptadas, texto reescrito.
- LearnPrompt/awesome-seedance (MIT) — templates "Handheld UGC vlog", "UGC creator review", "Reference image identity lock" e rubrica de QA.
- Atlas Cloud, "How to make AI UGC ads" — júri de roteiro e edição "de criadora".
