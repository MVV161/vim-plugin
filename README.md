vim-plug
========

A single-file Vim plugin manager.

### Parallel installation

![](https://raw.github.com/junegunn/vim-plug/master/gif/pi.gif)

### Serial installation

![](https://raw.github.com/junegunn/vim-plug/master/gif/si.gif)

### Parallel update

![](https://raw.github.com/junegunn/vim-plug/master/gif/pu.gif)

### Serial update

![](https://raw.github.com/junegunn/vim-plug/master/gif/su.gif)

### Pros.

- Easier to setup
- Parallel installation/update (requires +ruby)
- Alternative directory structure: user/repo
  - Make it easier to switch plugins of the same name from different authors

### Cons.

- Everything else

### Usage

Download plug.vim and put it in ~/.vim/autoload

```sh
mkdir -p ~/.vim/autoload
curl -fLo ~/.vim/autoload/plug.vim https://raw.github.com/junegunn/vim-plug/master/plug.vim
```

Edit your .vimrc

```vim
call plug#init()

Plug 'junegunn/seoul256'
Plug 'junegunn/vim-easy-align'
" Plug 'user/repo', 'branch_or_tag'
" ...
```

Then :PlugInstall to install plugins. (Default plugin directory: `~/.vim/plugged`)

You can change the location of the plugins with `plug#init(path)` call.

### Commands

| Command                | Description               |
| ---------------------- | ------------------------- |
| PlugInstall [#threads] | Install plugins           |
| PlugUpdate  [#threads] | Install or update plugins |
| PlugClean              | Remove unused directories |
| PlugUpgrade            | Upgrade vim-plug itself   |

(Default number of threads = `g:plug_threads` or 16)
