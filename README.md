# server-conf
Documentation Based on my Experience with HP MicroServer N40L


Blog Post in [Ghost](https://ghost.deathgabox.work/)

**Extra**
- Base install on my [Dotfiles Repo](https://github.com/DeathGabox/Dotfiles)
- Inspired on [Atareo Self Hosted Repo](https://github.com/atareao/self-hosted)



**Things i CAN'T do with this**
1. Running apps who support cpu instructions better than x86-64-v1

Examples:

- [Grimoire Issue 126: Illegal Instructions](https://github.com/goniszewski/grimoire/issues/126) -> I use my laptop to serve grimoire
- [Mysql issue 1055: oracle 9 need x86-64-v2](https://github.com/docker-library/mysql/issues/1055) -> I stay with [mysql-oraclelinux8](https://hub.docker.com/_/mysql/tags?name=oraclelinux8)
