# ubuntu-docker

If you want to use WSL 2 and Ubuntu integration on Windows directly into docker.

```sh
wsl.exe -l -v

wsl.exe --set-version Ubuntu-22.04 2

```

If you don't use WSL 2 Ubuntu integration as default, you need to run windows shell or powershell as legacy mode to avoid an issue with ctrl+z command !

```sh
docker pull ubuntu:latest
docker images
docker run -it --name ubuntu -v E:\Dev\Ubuntu:/home ubuntu
```

```sh
docker start -i ubuntu
docker stop ubuntu
```

```sh
apt update && apt upgrade
apt install sudo
useradd -m flo
cat /etc/passwd
passwd flo
sudo usermod -a -G sudo flo
sudo -su flo
```

```sh
userdel -r flo
```

```sh
sudo apt install git zsh zsh-syntax-highlighting curl i3 rofi compton \
tree ripgrep fd-find silversearcher-ag unzip bat \
neofetch stow mlocate zoxide python3-pip libsqlite3-dev \
libssl-dev wget

cd ~ && mkdir ~/Flo ~/Flo/Dev ~/Flo/Downloads ~/Flo/Apps ~/Flo/Dotfiles
```

```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

sudo chmod 777 ~/.oh-my-zsh/tools/uninstall.sh
sudo ~/.oh-my-zsh/tools/uninstall.sh
rm -rf ~/.oh-my-zsh && rm -rf ~./shell.pre-oh-my-zsh && rm -rf ~/.zshrc && rm -rf ~/.zsh_history
```

```sh
sudo apt install ninja-build gettext libtool libtool-bin autoconf automake cmake g++ pkg-config doxygen

cd ~/Flo/Apps && git clone https://github.com/neovim/neovim Neovim

cd Neovim && make CMAKE_BUILD_TYPE=RelWithDebInfo

sudo make install
```

```sh
cd ~ && pip3 install pynvim
```

```sh
cd ~ && sudo apt update && sudo apt upgrade

sudo apt remove tmux && sudo apt autoremove

rm -rf .tmux

sudo apt install libevent-dev ncurses-dev build-essential bison

cd ~/Flo/Apps && git clone https://github.com/tmux/tmux.git Tmux

cd Tmux && sh autogen.sh

./configure

make && sudo make install

tmux -V

cd ~ && mkdir .tmux .tmux/tmux-powerline-custom-themes

git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

git clone https://github.com/erikw/tmux-powerline.git ~/.tmux/plugins/tmux-powerline

wget https://raw.githubusercontent.com/Flo-Slv/Dotfiles/main/tmux/.tmux.conf

wget https://raw.githubusercontent.com/Flo-Slv/Dotfiles/main/tmux/.tmux.powerlinerc

wget -P ~/.tmux/tmux-powerline-custom-themes https://raw.githubusercontent.com/Flo-Slv/Dotfiles/main/tmux/.tmux/tmux-powerline-custom-themes/flo-theme.sh

tmux

cd ~ && nvim .tmux.conf

# ctrl+z I to install plugins
# ctrl+z r to re source tmux
# Save/close
```
