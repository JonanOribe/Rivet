# Rivet
docker compose down -v --rmi all

docker compose up -d

docker exec -it --user root paperclip chown -R 1000:1000 /paperclip/instances

# Inicializa el archivo de configuración en red LAN
docker exec -it paperclip pnpm paperclipai onboard --bind lan

# Genera el enlace de invitación del administrador
docker exec -it paperclip pnpm paperclipai auth bootstrap-ceo


