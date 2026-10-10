# Assinatura Academia — Web

Next.js (App Router), TypeScript strict. A API fica em assinatura-academia-api; os tipos de domínio vêm de
`@assinatura-academia/contracts`, instalado via Git daquele repositório (docs no repo da API: docs/adr/0003).

## Comandos

- pnpm dev | pnpm typecheck | pnpm build | pnpm format
- Contrato mudou na API: `pnpm update @assinatura-academia/contracts`

## Regras invioláveis

- Tipos de domínio só em @assinatura-academia/contracts. Não duplicar nem redeclarar aqui.
- Toda resposta da API validada com o schema do contrato antes de usar.
- Sem `any`, sem `@ts-ignore`, sem `!` non-null.
- Nunca ler/escrever .env nem logar segredo ou dado pessoal.
- Nenhum segredo no front: só variáveis `NEXT_PUBLIC_*` chegam ao navegador.

## Convenções

- Rotas em src/app/; componentes reutilizáveis em src/components/.
- Server Components por padrão; `'use client'` só quando houver estado/evento no navegador.
- Chamadas à API só via src/lib/api.ts.
- Import interno com `@/` (ex.: `@/lib/api`).

## Fluxo

Branch `feat|fix|chore/<id-monday>-slug`. PR com título Conventional Commits + `[#<id>]`.
Squash merge. Teste junto com a mudança.
