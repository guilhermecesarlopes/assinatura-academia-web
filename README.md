# Assinatura Academia — Web

Front-end em Next.js. A API fica em
[assinatura-academia-api](https://github.com/guilhermecesarlopes/assinatura-academia-api); os contratos
(`@assinatura-academia/contracts`) são instalados via Git daquele repositório.

## Começar

```bash
corepack enable
pnpm install
cp .env.example .env.local        # NEXT_PUBLIC_API_URL
pnpm dev                          # web: :3000 (suba a API em :8787)
```

## Comandos

| Comando                                      | O que faz                      |
| -------------------------------------------- | ------------------------------ |
| `pnpm dev`                                   | sobe o front                   |
| `pnpm typecheck`                             | checagem de tipos              |
| `pnpm build`                                 | build de produção              |
| `pnpm update @assinatura-academia/contracts` | puxa a versão nova do contrato |

## Ambientes

| Ambiente    | API                   |
| ----------- | --------------------- |
| dev (local) | http://localhost:8787 |
| staging     | API de staging        |
| production  | API de produção       |

Regras do projeto: [CLAUDE.md](CLAUDE.md).
