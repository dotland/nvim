# A Simple and Powerful Neovim Configuration

Neovim is a refactored Vim editor.

For more information on Neovim see the [Introduction](https://github.com/neovim/neovim/wiki/Introduction) wiki page.

## Installation

- Ubuntu
```shell
sudo apt install neovim
```

- Debian
```shell
sudo apt-get install neovim
```

- Fedora
```shell
sudo dnf install neovim
```

- OpenSUSE
```shell
sudo zypper install neovim
```

- Arch Linux
```shell
sudo pacman -S neovim
```

### Pre set up

Install nodejs and yarn
```shell
curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo npm install -g yarn
rm -f nodesource_setup.sh
```

For python autocompletion
```shell
sudo apt install python3 python3-pip
sudo pip install jedi
```

For tagbar support
```shell
sudo apt install exuberant-ctags
```

### Set up

1. Clone this repo
    ```shell
    cd $HOME/.config
    git clone https://github.com/dotland/nvim.git
    ```

2. Install the [Vim plugin manager](https://github.com/junegunn/vim-plug)
    ```shell
    wget --no-check-certificate -P $HOME/.local/share/nvim/site/autoload \
        https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
    ```

3. Open nvim and type `:PlugInstall` to install the plugins defined in the [init.vim](./init.vim) file.

4. Install [Conquer of Completion](https://github.com/neoclide/coc.nvim) for autocomplete.
    ```shell
    cd $HOME/.local/share/nvim/plugged/coc.nvim
    yarn install
    yarn build
    ```
5. Open nvim and add some autocompletion support.
    ```vim
    :CocInstall coc-emmet coc-css coc-cssmodules coc-explorer coc-highlight coc-html 
    coc-java coc-json coc-lsp-wl coc-ltex coc-markmap coc-metals coc-prettier 
    coc-python coc-rome coc-sh coc-snippets coc-sqlfluff coc-svg coc-texlab coc-xml coc-yaml
    ```

To set up nvim for the root, switch user by `sudo su` and repeat the previous steps of [set up](#set-up).

### Post set up

```shell
yarn global add neovim
pip install --user neovim
```

Open nvim and type `:checkhealth` to see if neovim is healthy.

### Fonts

Install Nerd Fonts
```bash
cd ~/Downloads
git clone --depth 1 https://github.com/ryanoasis/nerd-fonts.git
cd ./nerd-fonts
./install.sh FiraCode FiraMono Hack Hermit Inconsolata JetBrainsMono SourceCodePro Ubuntu UbuntuMono
```

Or just untar [mono.tar.gz](https://drive.google.com/file/d/1j31VMUUAZSb4dp80lxsKiV0m27e2E0qR/view?usp=share_link) archived file to the ~/.fonts directory.

Also install [powerline fonts](https://github.com/powerline/fonts) by
```shell
sudo apt-get install fonts-powerline
```

To configure nvim font, change the terminal font preferences.

To change Neovim GUI font see the [ginit.vim](./ginit.vim) file.

See also [A Basic Stable IDE config for Neovim](https://github.com/LunarVim/nvim-basic-ide).

## GUI

There are several graphical user interfaces for Neovim to try one.

- [Neovim Qt](https://github.com/equalsraf/neovim-qt) - a lightweight cross-platform Neovim GUI written in C++ with [Qt](https://www.qt.io/).
- [Neovide](https://github.com/neovide/neovide) - a simple graphical user interface for Neovim.
- [FVim](https://github.com/yatli/fvim) - a cross platform Neovim front-end UI, built with [F#](https://fsharp.org/) + [Avalonia](http://avaloniaui.net/).
- [GNvim](https://github.com/vhakulinen/gnvim) - a rich Neovim GUI without any web bloat.
- [Goneovim](https://github.com/akiyosi/goneovim) - a Neovim GUI written in [Go](https://go.dev/), using a Qt binding for Go.
- [NyaoVim](https://github.com/rhysd/NyaoVim) - a Neovim frontend built on [Electron](https://www.electronjs.org/).
- [neovim-gtk](https://github.com/daa84/neovim-gtk) - a [GTK](https://www.gtk.org/) ui for neovim written in [Rust](https://www.rust-lang.org/) using gtk-rs bindings.
- [glrnvim](https://github.com/beeender/glrnvim) - GPU-accelerated Neovim GUI.
