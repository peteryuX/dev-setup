# dev-setup
My development environment setup

# Linux

## General
- `sudo apt update`
- `sudo apt upgrade`
- `sudo apt-get install ssh`
- `sudo apt-get install vim`
- `sudo apt-get install git`
- `sudo apt-get install g++` (**required** to install CUDA)

## zsh

- Install zsh, follow the reference [here](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
- Install Oh My ZSH `sh -c "$(wget -O- https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
- Note from https://gist.github.com/renshuki/3cf3de6e7f00fa7e744a
- zsh syntax highlighting: https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md
## tmux

- `sudo apt-get install tmux`
- Install [tmux-config](https://github.com/tony/tmux-config).

## Anaconda
- Install miniconda 3.

## Cuda
- Download `.run` installer of Cuda 7.5 from [official site](https://developer.nvidia.com/cuda-toolkit).
- Open Ubuntu's `System Settings` and find `Software & Updates`
- Find section `Additional Drivers` and select `XXX (proprietary, tested)`
- `sh` the download file.

  **Note**: select **no** when system prompt ask you to install

  To verify if you've installed CUDA successfully, run following command
  ```
  cd /usr/local/cuda/samples/1_Utilities/deviceQuery
  sudo make
  ```
- Edit `.bashrc` (`.zshrc` if you use zsh) to include the following lines:

  ```
  export PATH=/usr/local/cuda-7.5/bin:$PATH
  export LD_LIBRARY_PATH=/usr/local/cuda-7.5/lib64:$LD_LIBRARY_PATH
  ```
## Vim
### Normal
- Copy [this](https://github.com/amix/vimrc/blob/master/vimrcs/basic.vim) into `~/.vimrc`.
### Vundle
- Vundle https://blog.gtwang.org/linux/vundle-vim-bundle-plugin-manager/ 
- `sudo apt-get install git curl`
- `git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
### Python VIM
- fisa-vim-confg https://aji.tw/vundle-vim-%E5%A4%96%E6%8E%9B%E7%AE%A1%E7%90%86%E5%A5%97%E4%BB%B6/
- `sudo apt-get install curl vim exuberant-ctags git ack-grep`
- `sudo pip install pep8 flake8 pyflakes isort yapf`
- `mv ~/.vimrc ~/.vimrc.bak`
- `wget https://raw.githubusercontent.com/amigcamel/fisa-vim-config/master/.vimrc -O ~/.vimrc`

## Visual Studio
- Download deb from https://code.visualstudio.com/.

## Docker
- Install Docker 19.03 https://docs.docker.com/engine/install/ubuntu/
- Install nvidia-container-toolkit https://github.com/NVIDIA/nvidia-docker
- Run w/o sudo https://linoxide.com/linux-how-to/use-docker-without-sudo-ubuntu/
- Test on the tensorflow 2.0 https://www.tensorflow.org/install/docker

# MacOS

## Oh-my-zsh
- Follow the instruction [here](https://ohmyz.sh/)

## Homebrew
- Follow the instruction [here](https://brew.sh/)

## wget
`brew install wget`

## tmux

- `brew install tmux`
- Install [tmux-config](https://github.com/tony/tmux-config).

## TheFuck
- sudo apt install python3-dev python3-pip python3-setuptools
- sudo pip3 install thefuck

## Visual Studio

## Anaconda
- Install miniconda 3.

## Vim
- Copy [this](https://github.com/amix/vimrc/blob/master/vimrcs/basic.vim) into `~/.vimrc`.
