JumpServer - Docker Compose

Requisitos

Docker Desktop

Docker Compose v2+

Primeira execucao

Copie .env.example para .env.

Ajuste SECRET_KEY e BOOTSTRAP_TOKEN.

Execute:

docker compose up -d --build

Acesse:

http://localhost:8080

SSH:

localhost:2222

Rebuild

Para reconstruir a imagem a partir do repositorio:

docker compose build --no-cache
docker compose up -d

Parar

docker compose down

Os volumes jsdata e pgdata nao sao removidos pelo down.

Remover tambem os dados

ATENCAO: isto apaga os dados persistentes do JumpServer:

docker compose down -v