# cursor-test

Este repo contiene una estructura basica para ejecutar n8n con Docker
Compose. Es una base inicial pensada para principiantes.

## Requisitos

- Docker Engine o Docker Desktop
- Docker Compose v2 (incluido en Docker Desktop)

## Estructura

- docker-compose.yml: define el servicio n8n
- .env.example: variables de entorno base
- data/: persistencia de credenciales y flujos (no se versiona)

## Pasos rapidos

1. Copia el archivo de variables:
   cp .env.example .env
2. Edita .env si deseas cambiar host, zona horaria o la clave de cifrado.
3. Levanta el servicio:
   docker compose up -d
4. Abre la UI:
   http://localhost:5678
5. Para detener:
   docker compose down

## Notas

- Define N8N_ENCRYPTION_KEY y guardala en un lugar seguro; es necesaria
  para restaurar credenciales.
- Si expones n8n en internet, configura HTTPS y un dominio real y
  actualiza WEBHOOK_URL.