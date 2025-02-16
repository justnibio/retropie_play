# Play! Setup for Retropie

This will add an entry on [Retropie-Setup](https://github.com/RetroPie/RetroPie-Setup) for [Play! emulator](https://github.com/jpd002/Play-) running on a ARM64 (aka Raspberry) machine.

## Requirements

Check if you have Play already listed in file `~/RetroPie-Setup/platforms.cfg`.

If not, create (or edit) file `/opt/retropie/configs/all/platforms.cfg` and add:

```
switch_exts=".iso .bin .cue .chd .elf"
switch_fullname="Play"
```

## Install

After that, install the Play! setup script with:

```bash
sudo apt install -y flatpak
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install --user -y flathub org.purei.Play
```

Now you can run **RetroPie Setup** script and `play` will available under `exp` (experimental) packages section.
