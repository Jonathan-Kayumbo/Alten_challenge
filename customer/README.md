This will create a portainer as a service and from GUI , i can control the status of other microservies setup ../vehicles 

# Usage

This setup comes up with the [Traefik](https://github.com/containous/traefik) v2.2.8 reverse proxy to access the Portainer instance via a virtual host, has support for SSL certificates using Let's Encrypt and automatic redirection from http to https.

The default configuration will make Portainer frontend available via the `portainer.yourdomain.com` domain. If you wish to change this, update the `traefik.http.routers.frontend.rule=Host(`portainer.yourdomain.com`)` label for the Portainer service in the `docker-compose.yml` file.

If you're going to use Edge agents. When you set up the endpoint from Portainer Configuration, you need to change the Portainer Server URL setting to match with the label specified for Edge. In this sample, the URL specified for the Edge service is `traefik.http.routers.frontend.rule=Host(`edge.yourdomain.com`)`.

![Edge](/traefik/edge.png)

Deploy this stack on any Docker node:

```
docker-compose up -d
```
