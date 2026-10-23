# test-manager-library-3239137-infra

Infraestructura de **Manager Library**: contenedores, red, volúmenes y motor de base de datos **vacío**.

> El esquema (tablas, índices, restricciones y semilla de categorías) lo crean las **migraciones de Laravel** en el repositorio `api`.  
> Este repositorio **no** contiene `CREATE TABLE` (ver constitution.md Artículo V y ADR-001).

---

## Requisitos

- Docker
- Docker Compose v2

## Arranque rápido

```bash
# 1. Copiar variables de entorno
cp .env.example .env

# 2. Levantar el motor de base de datos (vacío)
docker compose up -d

# 3. Verificar que está sano
docker compose ps
docker compose exec db pg_isready -U library -d library
