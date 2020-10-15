#Details

This works in a complete gitlab CI/CD flow , 
> Create portainer container
> Push to My Azure Image register 
> Deploy to ak8 cluster in Microsoft Azure
> Then it can be customsed from the GUI to monitor other nodes in the same cluter 


# Usage


This setup comes up with the [Traefik](https://github.com/containous/traefik) v2.2.8 reverse proxy to access the Portainer instance via a virtual host

The default configuration will make Portainer frontend available via the `portainer.yourdomain.com` domain

Deploy this stack on any Docker node:

```
docker-compose up -d
```

And then access Portainer by hitting [http://portainer.yourdomain.com](http://portainer.yourdomain.com) with a web browser.

**NOTE**: Your machine must be able to resolve `portainer.yourdomain.com` (or your own domain if you updated it).
