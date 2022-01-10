# tModLoader Docker ![tMod Version] ![Terraria Version]  [![Docker Pulls]][0]

[tModLoader] dedicated server  

Terraria server 1.3.5.3 with tModLoader v0.11.8.5.

# Sample Docker Compose

    version: '3'

    services:
      terraria:
        build: https://github.com/markusn1/tmodloader-docker.git
        ports:
          - '7778:7777'
        restart: unless-stopped
        environment:
          - world=world.wld
        volumes:
          - /root/terraria-tmodloader/Worlds:/root/.local/share/Terraria/ModLoader/Worlds
          - /root/terraria-tmodloader/Mods:/root/.local/share/Terraria/ModLoader/Mods
        tty: true
        stdin_open: true

[tModLoader]: https://www.tmodloader.net/
[wiki]: https://terraria.gamepedia.com/Server#Server_config_file
[commands]: https://terraria.gamepedia.com/Server#List_of_console_commands
[tMod Version]: https://img.shields.io/badge/tMod-0.11.8.5-blue
[Terraria Version]: https://img.shields.io/badge/Terraria-1.3.5.3-blue
[Docker Stars]: https://img.shields.io/docker/stars/rfvgyhn/tmodloader.svg
[Docker Pulls]: https://img.shields.io/docker/pulls/rfvgyhn/tmodloader.svg
[default]: https://github.com/Rfvgyhn/tmodloader-docker/blob/master/config.txt
[directly]: https://github.com/tModLoader/tModLoader/wiki/Mod-Browser#direct-download
[Environment Variables]: #environment-variables
[game-manager]: https://hub.docker.com/r/rfvgyhn/game-manager/
[0]: https://hub.docker.com/r/rfvgyhn/tmodloader
