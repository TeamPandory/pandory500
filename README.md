
# Pandory Mod for the A500 Mini
by @**emuchicken** and @**dajoho**

## WHAT IS PANDORY?

Pandory is "sideloaded" firmware for the A500 mini which gives you full access to the machine and allows you to run native programs that enable many new game emulators, such as RetroArch. It comes in the form of a WHDLOAD package and exploits a hidden-feature of the A500 amiberry emulator to run native code. It runs completely from USB stick and is **100% removable**.

## WHAT DOES PANDORY DO?
Pandory enables:
- A new native RetroArch menu, with OpenGL video-driver support, allowing many new emulators alongside Amiga, including:
    - Megadrive
    - SNES
    - Playstation 1
    - 32X
    - Amiga PUAE
        - *RetroArch has been configured with ADF and IPF support.*
    - Commodore 64
    - Atari ST
    - PC-Engine / TurboGrafx
    - MS-DOS
    - Game Boy
    - Game Boy Color
    - Game Boy Advance
    - Game Gear
    - MasterSystem
    - Quake/DOOM ports
    - ScummVM (Retroarch version)
    - *.. and many more ..*
- Full root access to your device via Linux Terminal
- ScummVM (Native version)
- Allows switching between the normal A500 menu / Pandory Menu
- Thousands of thumbnails for many different games
- Allows configuration and mapping of controllers not usually supported by the A500 mini
- Background music
- Flexible aspect ratio configuration options

## HOW DO I GET IT?
Download the latest zip via torrent, or use the direct link here.

## INSTALL

Copy the `Pandory` and `THEA500` folders to a FAT32-formatted USB stick. You can use the program [Rufus](https://rufus.ie/downloads/) to do this. If you already have a `THEA500` folder, such as one from the fantastic [Aminimiga](https://www.aminimiga.com/) project, you don't need to copy ours. To uninstall, just delete the `Pandory` folder.


## USAGE

Insert your prepared USB, select it from the A500 menu, choose the `Pandory` folder and start `Pandory`. You should be greeted with the RetroArch menu. We have pre-installed a few homebrew games for your perusal.


## INSTALLING ROMS

If you want to add roms, put them on your USB stick in a subfolder of `Pandory/.user/roms/`. In order for them to become visible in the RetroArch menu, use the RetroArch settings menu to refresh your playlists, or to add a new playlist. We have pre-configured many playlists for individual consoles, but you can also add your own. To do this, use the `Manual scan` option in the RetroArch menu. Select a folder, select a core and start scanning. 

*Pandory contains **several thousand** screenshots from almost any game you wish to add. If you name your roms/folders according to the libretro naming scheme (see http://thumbnails.libretro.com/), the thumbnails should automatically appear.*


## BIOS FILES

Some games require BIOS files. RetroArch will tell you what they are called if they are missing. If needed, copy any required files to `Pandory/.user/.config/retroarch/system`.  Pandory automatically copies the embedded A500-Amiga Kickstart files to this folder when you first start, so installing Amiga BIOS files is not necessary.


## RETROARCH SHORTCUTS

To quit a game, hold start and select.
To modify settings while a game is running, or to remap controls, hold start. For some N64 games you will need to map the D-PAD to Controller Y+/Y- and X+/X- manually.


## WHERE IS EVERYTHING ON THE A500?

Since RetroArch is a linux application, the paths to all the files are in unix format on the A500. Here are some useful locations that you might need in the RetroArch menu:

USB-Stick: `/mnt`
Pandory-Roms: `/mnt/Pandory/.user/roms/`
RetroArch-Settings: `/mnt/Pandory/.user/.config/retroarch`
RetroArch-Themes: `/tmp/pandory/share/retroarch/assets`
RetroArch-Cores: `/tmp/pandory/share/retroarch/cores`
RetroArch-Thumbnails: `/tmp/pandory/share/retroarch/cores`
Linux Binaries: `/tmp/pandory/bin`


## HACKING

As the USB stick has to be in FAT32 format, and FAT32 has performance problems when working with many thousands of files, we distribute Pandory as a virtual filesystem. This is the `.pandory` file within the Pandory folder. It is a linux ext2 disk image and contains all of the pandory programs, libraries, RetroArch assets, cores and game thumbnails. The `.pandory` file is mounted in the folder `/tmp/pandory` on the A500. If you wish to edit it, you can use an installation of Linux, such as [Manjaro Gnome,](https://manjaro.org/downloads/official/gnome/) right click the `.pandory` file and open it with Disk-Image-Mounter. It is also possible to mount the filesystem with the following commands:  `mkdir /tmp/pandory && mount -o loop .pandory /tmp/pandory`.

## THANKS

- Many thanks to http://androidarts.com/ for the pixel-art icons used in the RetroArch menus.
- Lotus Turbo Challenge 2 title screen music used with permission by Barry Leitch. Thanks Barry! Please support him at his bandcamp here: https://barryleitch.bandcamp.com/

## LICENSE 
The whole of the Pandory A500 modification, including reverse-engineered development toolchain, patched 3rd party packages and buildscripts will be released under GPL (or their own respective open-source license) within the next few days. We're still tidying things up so that they are usable and pretty.

## COMMUNITY

Want to chat about the Pandory A500 Mod? Come and visit us on Discord: https://pg3d-hax.uk/discord 
