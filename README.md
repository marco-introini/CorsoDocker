# Corso Docker

Una piccola introduzione a Docker con esempi

## Risorse utili

- Dockerfile Reference: https://docs.docker.com/engine/reference/builder/
- Compose reference: https://docs.docker.com/compose/compose-file/compose-file-v3/
- Docker Hub: https://hub.docker.com/

## Eseguire i comandi

### Creazione dell'immagine da Dockerfile

- posizionarsi nella directory 01_AlpineLinux
- eseguire: 
`docker build -t alpine_linux .`
- questo esegue il download di quanto specificato nel Dockerfile e crea l'immagine

### Esecuzione

`docker run -it alpine_linux`

- -i lascia lo standard input attivo
- -t crea una console sulla vm

## Utilizzo di docker compose

Nella directory principale: `docker-compose up -d`

Per vedere se funziona vai con il browser su: http://localhost:8003

