# CAPITAL — Kit Completo de Handoff para Desenvolvimento

**Versão:** 0.2 — Blueprint + protótipo navegável  
**Data:** 2026-10-07  
**Contexto:** plataforma de inteligência operacional e observabilidade de capital para operação imobiliária/urbanística, usando Bitrix24 como *System of Record* transacional e o CAPITAL como *System of Work + System of Intelligence*.

## Objetivo

Este pacote consolida o que foi definido para o projeto CAPITAL (evolução do conceito MoneyFlow):

- mostrar **dinheiro na mesa** antes de volume operacional;
- rastrear capital desde **Land Bank → desenvolvimento → marketing → comercial → jurídico → financeiro → caixa**;
- transformar controles em planilhas em **registros estruturados e relacionáveis no Bitrix24**;
- permitir que o usuário opere sem precisar abrir a interface do Bitrix;
- suportar operação humana e agêntica via **Capital API + MCP**;
- usar **RBAC + ABAC** para personalizar contexto, ações e profundidade de dados;
- adotar uma interface *calm by default*, baseada em princípios do Impeccable;
- entregar deployment em **VPS com Docker Compose**, TLS, backups, health checks e observabilidade.

## Regra de ouro

> **Documento é evidência. Dado de negócio é registro.**

Planilhas, arquivos e sistemas legados não são simplesmente anexados. Seus fatos de negócio são descobertos, normalizados, reconciliados e carregados como entidades estruturadas no Bitrix24.

## Estrutura deste handoff

| Pasta | Conteúdo |
|---|---|
| `00-executive` | visão, escopo, princípios e decisões |
| `01-product` | PRD, personas, requisitos, backlog, roadmap |
| `02-architecture` | arquitetura, modelo de dados, Capital Graph, eventos |
| `03-bitrix` | blueprint de SPAs, API, eventos, autenticação, segurança |
| `04-etl` | manual de ETL, templates, reconciliação e scripts de exemplo |
| `05-google-drive` | ingestão e monitoramento de Drive/Sheets/Excel |
| `06-nextcloud` | ingestão via WebDAV/OCS e governança documental |
| `07-design` | PRODUCT.md, DESIGN.md, Impeccable e mocks |
| `08-agents-mcp` | agentes, MCP tools, políticas e níveis de autonomia |
| `09-security` | RBAC/ABAC, LGPD, auditoria, segredos e threat model |
| `10-observability` | logs, métricas, traces e observabilidade de negócio |
| `11-testing` | estratégia de testes, migração, E2E e critérios de aceite |
| `12-collaboration` | Git, PRs, ADRs, colaboração humana/agêntica |
| `13-devops` | Docker Compose, VPS, CI/CD, backup, rollback e runbooks |
| `14-contracts` | OpenAPI, eventos, comandos e schemas |
| `15-references` | fontes oficiais e glossário |

## Mock navegável para apresentação

A versão 0.2 inclui uma SPA estática na raiz e em `13-devops/starter/web/`, com temas claro/escuro, personas RBAC, Capital Graph, Land Bank, Jurídico, Financeiro, Comercial, Marketing, Smart Cities, fila de atenção e drill-down.

## Critério mestre de aceite

> **Se um valor financeiro aparece no CAPITAL, o usuário precisa conseguir navegar até os registros que explicam aquele valor, sua causa, seu responsável, seu prazo e sua próxima ação.**
