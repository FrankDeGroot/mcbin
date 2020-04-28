# mcbin
Minecraft bin folder with some useful commands, based on [this tutorial](https://linuxize.com/post/how-to-install-minecraft-server-on-ubuntu-18-04/).

# Features
* Minecraft server runs as user systemd service.
* Daily backup.
* Warning near shut down.
* Switch server versions.
* Snapshot upgrade.

# Assumptions
* Ubuntu 18.04 (or similar: apt, systemd).
* User `mc` with minimal `sudo` during setup.
* Cloned to `~/bin`.
* Backups stored in `~/backups`.
* Server(s) stored in `~/server`.
* Shuts down at 22:00 PM.

# Directory structure for `~/server`
* Symbolic link `current` for the running version.
* Directory common with all files and directories shared across versions (`server.properties`, `eula.txt`, `*.json`, `logs`, ...).
* `~/server/snapshot` for snapshot versions.

# Usage
* `git clone https://github.com/FrankDeGroot/mcbin.git ~/bin`
* `PATH=~/bin:$PATH` in your `.bash_aliases` or whatever favorite startup script you have.
* `mccreate` though I don't recommend running it blindly.
