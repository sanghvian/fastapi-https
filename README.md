### Instructions

1. Create an A name record as a subdomain in your domain provider and point it to this server's IP address (to get the IP address of your server, just run `sudo curl ifconfig.me`).

2. Use this blog - https://blog.ankitsanghvi.in/how-to-https-your-api/ -  to generate SSL certificates using letsencrypt and download and store them locally in this directory (you have to just specify the path in the nginx.conf file)chmod +x setup_docker.sh. 

3. Clone this repo onto your server

4. Make the server setup script executable: 

```bash
chmod +x setup_docker.sh
```

4. Run the script:

```bash
./setup_docker.sh
```

5. Log out and log back in to apply the Docker group changes.
After running this script, you can proceed with running Docker Compose as described earlier.

```bash
docker-compose up -d
```

6. You can now access the API at https://your-server-ip:8080