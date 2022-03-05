# A Simple and Powerful Neovim Configuration

Neovim is a refactored Vim editor.

For more information on Neovim see the [Introduction](https://github.com/neovim/neovim/wiki/Introduction) wiki page.

## Installation

Ubuntu
```shell
$ sudo apt install neovim
```

Debian
```shell
$ sudo apt-get install neovim
```

Fedora
```shell
$ sudo dnf install neovim
```

OpenSUSE
```shell
$ sudo zypper install neovim
```

Arch Linux
```shell
$ sudo pacman -S neovim
```

### Pre set up

Install nodejs and yarn
```shell
$ curl -k -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
$ sudo bash nodesource_setup.sh
$ sudo apt-get install -y nodejs
$ sudo npm install -g yarn
$ rm -f nodesource_setup.sh
```

For python autocompletion
```shell
$ sudo apt install python3 python3-pip
$ sudo pip install jedi
```

For tagbar support
```shell
$ sudo apt install exuberant-ctags
```

### Fonts

Install Nerd Fonts
```bash
$ cd ~/Downloads
$ git clone --depth 1 https://github.com/ryanoasis/nerd-fonts.git
$ cd ./nerd-fonts
$ ./install.sh FiraCode FiraMono Hack Hermit Inconsolata JetBrainsMono SourceCodePro Ubuntu UbuntuMono
```

To configure nvim font change terminal font preferences, to change GUI font see ginit.vim file.

## GUI

There are several graphical user interfaces for Neovim to consider.

- [Neovim Qt](https://github.com/equalsraf/neovim-qt) - a lightweight cross-platform Neovim GUI written in C++ with Qt.
- [Neovide](https://github.com/neovide/neovide) - a simple graphical user interface for Neovim.
- [FVim](https://github.com/yatli/fvim) - cross platform Neovim front-end UI, built with [F#](https://fsharp.org/) + [Avalonia](http://avaloniaui.net/).
- [GNvim](https://github.com/vhakulinen/gnvim) - rich Neovim GUI without any web bloat.
- [Goneovim](https://github.com/akiyosi/goneovim) - a Neovim GUI written in Go, using a Qt binding for Go.
- [NyaoVim](https://github.com/rhysd/NyaoVim) - a Neovim frontend built on Electron.
- [neovim-gtk](https://github.com/daa84/neovim-gtk) - GTK ui for neovim written in rust using gtk-rs bindings.
- [glrnvim](https://github.com/beeender/glrnvim) - GPU-accelerated Neovim GUI.

