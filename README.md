# Pandory Mod for the A500 Mini
by @**emuchicken** and @**dajoho** of Team Pandory https://www.youtube.com/teampandory

## WHAT IS PANDORY?

The Pandory Mod is "sideloaded" firmware for the A500 mini which gives you full access to the machine and allows you to run native programs that enable many new game emulators, such as RetroArch. It comes in the form of a WHDLOAD package and exploits a hidden-feature of the A500 amiberry emulator to run native code. It runs completely from USB stick and is **100% removable**.

[![POWER UP Your A500 Mini: PANDORY500 V3 on a USB Stick!](https://i1.ytimg.com/vi/DIRgmOtiol4/hqdefault.jpg)](https://www.youtube.com/watch?v=DIRgmOtiol4)

[YouTube Video v3](https://www.youtube.com/watch?v=DIRgmOtiol4)

[![A500 Mini Pandory Mod UPDATE! - What's new in Pandory500 ?](https://i1.ytimg.com/vi/tx8HyMEk8CM/hqdefault.jpg)](https://www.youtube.com/watch?v=tx8HyMEk8CM)

[YouTube Video v2](https://www.youtube.com/watch?v=tx8HyMEk8CM)

[![Pandory Mod for the A500 Mini on Youtube](https://i1.ytimg.com/vi/LpL2f1RfqBQ/hqdefault.jpg)](https://www.youtube.com/watch?v=LpL2f1RfqBQ)

[YouTube Video v1](https://www.youtube.com/watch?v=LpL2f1RfqBQ)


## WHAT DOES PANDORY DO?
Pandory enables:
- A new native RetroArch menu, with OpenGL video-driver support, allowing many new emulators alongside Amiga, including:
    - **Megadrive**
    - **SNES**
    - **Playstation 1**
    - **32X**
    - **Amiga PUAE**
        - *RetroArch has been configured with ADF and IPF support.*
    - **Commodore 64**
    - **Atari ST**
    - **PC-Engine / TurboGrafx**
    - **MS-DOS**
    - **Game Boy**
    - **Game Boy Color**
    - **Game Boy Advance**
    - **Game Gear**
    - **MasterSystem**
    - **Quake/DOOM ports**
    - **ScummVM (RetroArch version)**
    - *.. and many more ..*
- Full root access to your device via Linux Terminal
- NATIVE ScummVM Emulator - For point and click adventure games
- NATIVE OpenBOR Emulator - For fan-made beat-em-ups
- NATIVE PPSSPP - Playstation Portable Emulator
- NATIVE DOSBox Staging - IBM PC / MS-DOS Emulator
- NATIVE OpenCubic Music Player (plays MP3/MOD/XM and many more)
- NATIVE MilkyTracker (Make your own mod music)
- NATIVE Quake, Doom and Duke3D in HD
- NATIVE Video Player - with joypad support (mpv)
- Virtual cores to allow retroarch to start the native emulators
- Almost ALL settings are configurable in the `Pandory/.user` folder of the USB stick
- Allows switching between the normal A500 menu / Pandory Menu
- Thousands of thumbnails for many different games
- Allows configuration and mapping of controllers not usually supported by the A500 mini -> pandory bypasses SDL2-input and uses Linux-UDEV directly.
- Random background menu music.
- A selection of free homebrew-games to test before you add your own games.
- Flexible aspect ratio configuration options


## HOW DO I GET IT?

## INSTALL

Download the latest zip [here](https://www.teampandory.com/pandory500). 

Latest release notes are [here](https://github.com/TeamPandory/pandory500/releases/)

Copy the `Pandory` and `THEA500` folders to a FAT32-formatted USB stick. You can use the program [Rufus](https://rufus.ie/downloads/) to perform the formatting. If you already have a `THEA500` folder, such as one from the fantastic [Aminimiga](https://www.aminimiga.com/) project, you don't need to copy ours. To uninstall, just delete the `Pandory` folder.

## USAGE

Switch your A500 to 60hz for best performance. Insert your prepared USB, select it from the A500 menu, choose the `Pandory` folder and start `Pandory`. You should be greeted with the RetroArch menu. We have pre-installed a few homebrew games for your perusal.
Using a keyboard and mouse is recommended!


## INSTALLING ROMS

If you want to add roms, put them on your USB stick in a subfolder of `Pandory/.roms/`. In order for them to become visible in the RetroArch menu, use the RetroArch settings menu to refresh your playlists, or to add a new playlist. We have pre-configured many playlists for individual consoles, but you can also add your own. To do this, use the `Manual scan` option in the RetroArch menu. Select a folder, select a core and start scanning. 

*Pandory contains **several thousand** screenshots from almost any game you wish to add. If you name your roms/folders according to the libretro naming scheme (see http://thumbnails.libretro.com/), the thumbnails should automatically appear.*


## BIOS FILES

Some games require BIOS files. RetroArch will tell you what they are called if they are missing. If needed, copy any required files to `Pandory/.user/.config/retroarch/system`.  Pandory automatically copies the embedded A500-Amiga Kickstart files to this folder when you first start, so installing Amiga BIOS files is not necessary. Dreamcast/Naomi/Atomiswave BIOS files should go in `Pandory/.user/.config/flycast/share`.


## RETROARCH SHORTCUTS

To quit a game, hold start and select.
To modify settings while a game is running, or to remap controls, hold start. For some N64 games you will need to map the D-PAD to Controller Y+/Y- and X+/X- manually.


## WHERE IS EVERYTHING ON THE A500?

Since RetroArch is a linux application, the paths to all the files are in unix format on the A500. Here are some useful locations that you might need in the RetroArch menu:

- USB-Stick: `/mnt`
- Game-Roms: `/mnt/Pandory/.roms/`
- RetroArch-Settings: `/mnt/Pandory/.user/.config/retroarch`
- Settings for other applications: `/mnt/Pandory/.user/.config/retroarch`
- Linux Binaries: `/tmp/pandory/bin`

## HACKING

As the USB stick has to be in FAT32 format, and FAT32 has performance problems when working with many thousands of files, we distribute Pandory as a virtual filesystem. This is the `.pandory` file within the Pandory folder. It is a linux ext2 disk image and contains all of the pandory programs, libraries, RetroArch assets and other system files. The `.pandory` file is mounted in the folder `/tmp/pandory` on the A500. If you wish to edit it, you can use an installation of Linux, such as [Manjaro Gnome,](https://manjaro.org/downloads/official/gnome/) right click the `.pandory` file and open it with Disk-Image-Mounter. It is also possible to mount the filesystem with the following commands:  `mkdir /tmp/pandory && mount -o loop .pandory /tmp/pandory`.


## THANKS

- Many thanks to http://androidarts.com/ for the pixel-art icons used in the RetroArch menus.
- Lotus Turbo Challenge 2 title screen music used with permission by Barry Leitch. Thanks Barry! Please support him at his bandcamp here: https://barryleitch.bandcamp.com/
- Thanks to https://github.com/SimonLarsen/tobutobugirl, as we include TobuTobuGirl as a free rom inside Pandory.
- Thanks to XxDUSTYxX for letting us use some of his tracks as background music.
- To _jj0 and oleavr for their work on hacking the kernel and enabling the possibility of adding new hardware drivers to THEA500.

## LICENSE 
Pandory contains software which is covered by different licenses. Almost everything is covered by GPL3/GPL2 or MIT licenses, with the exception of the `host-rum` binary, which is closed source and covered by the Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) https://creativecommons.org/licenses/by-nc-nd/4.0/ license. It will be provided under the conditions of the GPL3 if/when the firmware exploit is closed. 

Code Repository and Toolchain: [https://code.teampandory.com/pandory/pandory500](https://code.teampandory.com/pandory/pandory500). 

Third-party packages: [https://code.teampandory.com/thirdparty](https://code.teampandory.com/thirdparty) (see the `pandory500` Branches for specific modifications)

## COMMUNITY

Want to chat about the Pandory A500 Mod? Come and visit us on Discord: https://teampandory.com/discord
