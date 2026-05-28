# A Minecraft Server for Create: Arcane Engineering

This repo contains a Docker system for installing and launching a server to run the Create: Arcane Engineering modpack.  It contains the mods and config, but will generate a world.

To install, first clone the repo.  Then, from the repo root, run
```bash
docker compose up
```

The server launches in a `screen` under the name `mc`, so you can attach to its console via
```bash
docker exec -it create-ae-mcserver-1 screen -r mc
```

The config is already set, and the eula is already set to true.  Important to note is that Github will not save the world, the backups, the logs, or anything else in the `.gitignore`, so a separate solution would be needed to manage those.

Note that the server backs itself up once per hour (when changes have happened), and will restart itself if the server dies.

## Screen

More verbosely, you can attach to the container with
```bash
docker exec -it create-ae-mcserver-1 /bin/bash
```
then run
```bash
screen -r mc
```
to attach to the server console.  To detach, press `ctrl-a` then `d`.