# Topcon Suite — API Documentation

Portal de documentação de APIs dos produtos **Topcon Suite**: TopconCRM, TopconTECH e TopconDispatch.

🌐 **Live:** [https://topconsuite.github.io/apis-documentation/](https://topconsuite.github.io/apis-documentation/)

## Visão Geral

Interface web estática com:

- **Home** — Cards de acesso rápido aos 3 produtos
- **Authentication** — Guia de autenticação (API Key / Subscription Key)
- **Integration Flows** — Diagramas visuais de integração ERP
- **API Reference** — Documentação interativa via [Redoc](https://redocly.com/redoc)
- **i18n** — Suporte a Inglês (EN) e Português (PT-BR)
- **Tema** — Dark / Light mode

## Estrutura

```
├── index.html                  # Página principal (SPA)
├── crm-swagger-en.json         # OpenAPI spec — CRM (EN)
├── crm-swagger-pt-BR.json      # OpenAPI spec — CRM (PT-BR)
├── tech-swagger-en.yaml        # OpenAPI spec — TECH (EN)
├── tech-swagger-pt-BR.yaml     # OpenAPI spec — TECH (PT-BR)
├── dispatch-swagger-en.yaml    # OpenAPI spec — Dispatch (EN)
├── dispatch-swagger-pt-BR.yaml # OpenAPI spec — Dispatch (PT-BR)
├── icons/                      # Logos dos produtos
│   ├── topcon.png
│   ├── crm.png
│   ├── techlogo.png
│   └── dispatch.png
└── flows/                      # Diagramas de integração
    ├── flow-1.png ... flow-7.png
```

## Rodar Localmente

```bash
npx serve .
```

Acesse `http://localhost:3000`

> **Nota:** Não funciona via `file://` — os arquivos de spec precisam ser servidos por HTTP.

## Deploy

Hospedado via **GitHub Pages** (branch `main`, pasta root).

Qualquer push na `main` atualiza o site automaticamente.

## Tecnologias

- HTML/CSS/JS puro (sem build)
- [Redoc](https://redocly.com/redoc) — renderização OpenAPI
- [js-yaml](https://github.com/nodeca/js-yaml) — parsing de YAML specs
- [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) — tipografia
- [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) — código