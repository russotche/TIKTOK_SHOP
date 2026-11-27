# TIKTOK_SHOP

Sistema de criação de vídeos de afiliado do TikTok Shop com a influencer de IA **Iza** (@queridaizabell).

O conteúdo de `sac/` foi exportado do Notion (árvore **SAC MÃE**) em 27/11/2026. O Notion continua sendo a fonte original; este repositório é uma cópia versionada.

## Estrutura

```
sac/        Sistema SAC (Sistema de Avanço de Compra), modalidades QWE (com fala) e MOV (sem fala)
isabell/    Regras, fluxo, roteiros e testes da Iza criados no projeto TIKTOK_ISABELL
docs/       Avaliações e decisões
```

## SAC — mapa de autoridades

| Assunto | Arquivo |
| --- | --- |
| Visão geral e mapa | [sac/00-SAC-MAE.md](sac/00-SAC-MAE.md) |
| Entrada (gatilho `SAC`) | [sac/00-BOOTSTRAP-ATIVACAO.md](sac/00-BOOTSTRAP-ATIVACAO.md) |
| Interface e primeiro despacho | [sac/00A-RUNTIME-NUCLEO-DE-ENTRADA.md](sac/00A-RUNTIME-NUCLEO-DE-ENTRADA.md) |
| Estados e transições | [sac/00-RUNTIME-STATE-MACHINE-V2.md](sac/00-RUNTIME-STATE-MACHINE-V2.md) |
| Materiais (Fase 1) | [sac/01-FLUXO-OPERACIONAL.md](sac/01-FLUXO-OPERACIONAL.md) |
| Evidências, locks, IMAGE_READY (Fase 2) | [sac/02-RULES-ENGINE.md](sac/02-RULES-ENGINE.md) |
| Orientações da Fase 2 | [sac/03-ORIENTACOES-OPERACIONAIS.md](sac/03-ORIENTACOES-OPERACIONAIS.md) |
| Roteiro (Fase 3) | [sac/04-CREATIVE-ENGINE-ROTEIRO.md](sac/04-CREATIVE-ENGINE-ROTEIRO.md) |
| Índice da Fase 3 | [sac/05-PADRAO-OPERACIONAL-ROTEIRO.md](sac/05-PADRAO-OPERACIONAL-ROTEIRO.md) |
| Elementos de texto e capa (Fase 4) | [sac/06-ELEMENTOS-DE-TEXTO-ENGINE.md](sac/06-ELEMENTOS-DE-TEXTO-ENGINE.md) |
| Encerramento e contadores (Fase 5) | [sac/07-EXECUTION-LIFECYCLE.md](sac/07-EXECUTION-LIFECYCLE.md) |
| Guia de navegação | [sac/08-FLUXO-OPERACIONAL-INTEGRADO.md](sac/08-FLUXO-OPERACIONAL-INTEGRADO.md) |
| Arquivo histórico | [sac/09-ARQUIVO-PASSIVO.md](sac/09-ARQUIVO-PASSIVO.md) |
| Registro de execuções | [sac/10-REGISTRO-ATIVO-QWE.md](sac/10-REGISTRO-ATIVO-QWE.md) |

Fluxo: `SAC → modalidade (QWE/MOV) → materiais → duração → influencer → pacote criativo A/B/C → imagem → roteiro → elementos de texto → capa → fim`.

## Iza

- [Regras de conformidade](isabell/regras-conformidade-influencer-ia.md)
- [Fluxo de produção](isabell/fluxo-producao.md)
- [Roteiros e dados de desempenho](isabell/roteiros-isabell.md)
- [Teste 01 — baby doll canelado](isabell/teste-01-baby-doll-canelado.md)

## Avaliação

- [Avaliação do SAC — 27/11/2026](docs/avaliacao-sac-2026-11-27.md) (nota 6/10)
