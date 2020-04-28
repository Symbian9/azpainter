# ![🖌](data/icon.png) AzPainter
[![Check latest release version](https://img.shields.io/github/release/symbian9/azpainter.svg)](https://github.com/Symbian9/azpainter/releases/latest) [![Coverity Scan Build Status](https://scan.coverity.com/projects/13683/badge.svg)](https://scan.coverity.com/projects/symbian9-azpainter) [![Packaging status](https://repology.org/badge/tiny-repos/azpainter.svg)](https://repology.org/project/azpainter/versions)

🖌 *AzPainter* is mainly a full color painting software for illustration drawing.

## Website

Official Website: http://azsky2.html.xdomain.jp/soft/azpainter.html (Japanese)

Other:

- English: https://azworldweb.wordpress.com
- Brazilian Portuguese: https://aznosekai.wordpress.com
- Russian: http://zenway.ru/page/azpainter

## Tutorials

To learn how to use AzPainter, take a look at the [«Tutorials» wiki-page](https://github.com/Symbian9/azpainter/wiki/Tutorials) for textual and video tutorials.

## Screenshots

<details>
  <summary>Expand to see screenshots of AzPainter</summary>

![Screeenshot 1, Japanese UI](http://azsky2.html.xdomain.jp/soft/img/azpainter.png)

![Screenshot 2, Free Software](http://i.imgur.com/p551IRB.png)

</details>

## Brushes

Built-in and community created brushes listed on [«Brushes» wiki-page](https://github.com/Symbian9/azpainter/wiki/Brushes).

## Themes

Read [«Themes» wiki-page](https://github.com/Symbian9/azpainter/wiki/Themes) for more info on customizing interface colors.

## Packaging status

**Note:** Current packages & build instructions available only for Unix-like OS: 

<details>
  <summary>Expand to view the downstream package repositories that currently carry the AzPainter package</summary>

[![Packaging status](https://repology.org/badge/vertical-allrepos/azpainter.svg)](https://repology.org/project/azpainter/versions)

</details>

- [BSD-based](https://github.com/Symbian9/azpainter/wiki/Packaging-status#bsd-based-os)
- [Linux-based](https://github.com/Symbian9/azpainter/wiki/Packaging-status#linux-based-os)
- [macOS](https://github.com/Symbian9/azpainter/wiki/Packaging-status#macos)

- [AppImage (master branch)](https://github.com/Symbian9/azpainter/releases/tag/continuous) [![Build status](https://travis-ci.org/Symbian9/azpainter.svg?branch=master)](https://travis-ci.org/Symbian9/azpainter) (Note: AppImages are self-contained executables)

> **Important note:** Continuous AppImage-builds are not yet usable. Currently they're used only for testing purposes!

All available packages listed on [wiki-page](https://github.com/symbian9/azpainter/wiki/Packaging-status).

## Prerequisites

- [X Window System](http://x.org/) (X11R6 or later)  
   **Note:** (X11R 7.5 or later when you want to recognize pen pressure)
- Unix-like OS (BSD-based, Linux-based, macOS, etc.)

> **Important Note:** MS Windows is not officially supported **BUT** you could try to compile & run AzPainter using Cygwin/X or Xming tools. More details on building on Windows found on the dedicated [wiki-page](https://github.com/Symbian9/azpainter/wiki/Packaging-status#windows).

## Installation

### Dependencies

```txt
gcc
make
automake
Xlib       (libX11)
Xext       (libXext)
XInput2    (libXi)
freetype2  (libfreetype)
fontconfig (libfontconfig)
zlib
libpng
libjpeg
```

----

#### Linux Distros

<details>
  <summary>Expand this section to read about installing AzPainter on various Linux distros</summary>
  
#### Debian/Ubuntu

```bash
gcc make automake libx11-dev libxext-dev libxi-dev \ 
libfreetype6-dev libfontconfig1-dev zlib1g-dev libjpeg-dev
```

**Important Note:**

- For Debian 9.0 / Ubuntu 16.10 or later you'll need: `libpng-dev`
- For Debian 8.0 (or less) / Ubuntu 16.04 (or less) you'll need: `libpng12-dev`

#### RedHat

```bash
gcc make automake libX11-devel libXext-devel libXi-devel \ 
libfreetype6-devel libfontconfig-devel zlib-devel libpng-devel libjpeg-devel
```

#### Arch Linux

You'll need to download AzPainter from the [AUR](https://aur.archlinux.org/packages/azpainter/)  
You can use [yay](https://github.com/Jguer/yay) or [trizen](https://github.com/trizen/trizen) or your package manager to install the package

</details>

----

## Compile from Source

<details>
  <summary>Expand this section for instructions on how to compile AzPainter from source</summary>

1. Download & unpack tarball of [latest sources release](https:/github.com/symbian9/azpainter/releases/latest).

  ```bash
  $ ./configure
  $ make
  $ sudo make install-strip
  ```
  Note: It will be installed in the `/usr/local` by default.

2. Run `./configure`  
  **Note:** You can customize the install directory e.g. installing to `/usr` will require the following flag:

  ```bash
  $ ./configure --prefix=/usr
  ```
  If you can not find the header files of freetype you can specify their location with the `--with-freetype-dir` flag:  

  ```bash
  $ ./configure --with-freetype-dir=/usr/include/freetype2
  ```

3. Invoke `AzPainter`

  ```bash
  $ ./azpainter
  ```

</details>

## Usage

- **Using the GUI:** find AzPainter in your distro's application menu and invoke it.

- **Using the terminal:** as mentioned before, invoking AzPainter from the terminal is as simple as typing:  

  ```bash
  $ azpainter
  ```

## Developer

> Copyright (C) 2013-2020 Azel

- http://azsky2.html.xdomain.jp/
- <azelpg@gmail.com>

## LICENSE

This software is released under the GNU GPLv3 License.

Please see the file `GPL3` for details.
