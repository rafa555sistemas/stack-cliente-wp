# Stack de cliente — WordPress + MariaDB

Stack Docker Compose reutilizable para un sitio WordPress con su base de datos.

## Requisitos
- Docker Engine + plugin `docker compose` v2

## Arranque (máquina nueva)
```bash
git clone <URL_DEL_REPO> cliente-wp
cd cliente-wp
cp .env.example .env      # rellena las contraseñas reales
nano .env
docker compose up -d
```
La web queda en `http://IP_DEL_SERVIDOR:8080` (o el puerto que pongas en `WP_PORT`).

## Operación diaria
| Acción | Comando |
|---|---|
| Ver estado | `docker compose ps` |
| Ver logs | `docker compose logs -f` |
| Actualizar | `docker compose pull && docker compose up -d` |
| Parar | `docker compose down` (los datos se conservan en volúmenes) |

## Secretos
Las credenciales viven en `.env`, que **no** está en git. Usa `.env.example` como plantilla.
# Mejora aplicada en rama de desarrollo
