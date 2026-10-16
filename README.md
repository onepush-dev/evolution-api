# Evolution API — self-hosted WhatsApp API (Baileys) on Railway. Deploy on Railway with one click.

Services: `evolution-api` (evoapicloud/evolution-api:v2.3.7, digest-pinned, volume at `/evolution/instances`), Railway Postgres, Railway Redis.

Zero deploy-time inputs. `AUTHENTICATION_API_KEY` is generated (`${{secret(32)}}`); read it from the service Variables tab and send it as the `apikey` header.
Manager UI: `https://<domain>/manager`.

Key variables: `SERVER_URL=https://${{RAILWAY_PUBLIC_DOMAIN}}`, `DATABASE_CONNECTION_URI=${{Postgres.DATABASE_URL}}`, `CACHE_REDIS_URI=${{Redis.REDIS_URL}}`, `PORT=SERVER_PORT=8080`.
