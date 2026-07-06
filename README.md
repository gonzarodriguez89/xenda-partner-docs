# Xenda Partner API — Docs

Documentación **pública para partners** (Oshma y futuros) de la Xenda Partner API.
Publicada con [Mintlify](https://mintlify.com) — el API Reference con playground
interactivo se genera desde `openapi.yaml`.

## Cómo se actualiza

- **Fuente de verdad partner-facing**: `openapi.yaml` (spec OpenAPI 3.1, incluye el
  webhook `reply.received`) + los `.mdx` (guías en español).
- **Regla** (espejada en el CLAUDE.md de `whatsapp-broadcast`): cualquier cambio en la
  Partner API de Xano (`api/partner/**` o el webhook `kapso/inbound-replies`) debe
  actualizar `openapi.yaml` y agregar una entrada en `changelog.mdx` acá.
- **Deploy**: automático al pushear a `main` (GitHub App de Mintlify conectada a este
  repo). No hay deploy por CLI.
- Lo **interno** (arquitectura Xano, checklist de go-live, secrets, Kapso) vive en
  `docs/PARTNER_CAMPAIGNS_API.md` del repo `whatsapp-broadcast` — **nunca acá**: todo lo
  que entra a este repo es público para partners.

## Preview y validación local

```bash
npm i -g mint
mint dev              # preview en http://localhost:3000
mint broken-links     # links internos
mintlify validate     # valida openapi.yaml
```
