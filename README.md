<p align=center>
  <a href="https://github.com/x86chi">
    <img alt="dotfiles" src="./logo.png">
  </a>
  <br>
  <a href="macOS">macOS</a>
</p>

Requires `git` and `zsh`

```bash
git clone https://github.com/x86chi/.dotfiles.git --depth=1 ~/.dotfiles

ln -sf ~/.dotfiles/.zshrc ~

# install oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

mkdir -p ~/.gnupg; ln -sf ~/.dotfiles/gpg-agent.conf ~/.gnupg
ln -sf ~/.dotfiles/.vimrc ~
ln -sf ~/.dotfiles/.gitconfig ~
ln -sf ~/.dotfiles/.gitexclude ~

# Optional dotfiles
cp ~/.dotfiles/.gitconfig.local ~

# vim-plug

type below command to neovim:
:call mkdir(stdpath('config'), 'p')

ln -sf ~/.dotfiles/init.vim ~/.config/nvim

# apply vscode configuare
ln -sf ~/.dotfiles/settings.json [path]

# macos [path]: ~/Library/ApplicationSupport/Code/User/

## install vscode extensions
cat ~/.dotfiles/vs_code_extensions_list.txt | xargs -n 1 code --install-extension

## update vscode extensions list
code --list-extensions >> vs_code_extensions_list.txt
```

MacOS vscode path is `~/Library/ApplicationSupport/Code/User/`

---

_dotfiles_ was inspired by [simnalamburt/.dotfiles](https://github.com/simnalamburt/.dotfiles).

_dotfiles_ is primarily distributed under the terms of the MIT license. See [LICENSE](./LICENSE) for details.
