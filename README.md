# Expert-level SkyBlock minecraft server - docker configuration
Dockerized Minecraft fabric server with [Carpet Sky Additions](https://github.com/jsorrell/CarpetSkyAdditions) based on [itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server/) image with RCON web administration. Carpet Sky Additions aims to provide an expert-level SkyBlock style gameplay that depends on players' knowledge of Minecraft mechanics. 

# Installation

Download the repository
```bash
  git clone https://github.com/denkre/LTP
  cd LTP
```

## Configuration
Change the RCON webapp username and password in docker-compose.yml
```bash
      RWA_USERNAME: "admin"
      RWA_PASSWORD: "Heslo123"
```

If you want to automatically OP someone after the server is created, you can config it in docker-compose.yml, you can also add there another commands you want to run after server is started
```bash
    RCON_CMDS_STARTUP:  |- # change to the username you want to give OP to
      op username 
````

## Build
Build and run the server
```bash
  docker compose up
```

## Accessing services
In your Minecraft client add server with address 127.0.0.1:25565
![image](https://github.com/denkre/LTP/assets/37020825/2f323dab-7311-4600-b719-7ef303a27d7b)

In your browser you can access the RCON web administration on address http://127.0.0.1:4326/
![image](https://github.com/denkre/LTP/assets/37020825/678d994d-f59c-4456-b048-ef4cb16657f1)



