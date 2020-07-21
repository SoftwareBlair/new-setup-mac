# Dev Setup Mac

## Terminal 
- [iTerm2](https://www.iterm2.com/)
  - Set text navigation 
    ```
    iTerm → Preferences → Profiles → Keys → Load Preset… → Natural Text Editing
    ```
  - Download different [iTerm2 Themes](https://iterm2colorschemes.com/)

## Editor 
- [Visual Studio Code](https://code.visualstudio.com/)
- Xcode - download through macOS App Store

## Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

## Zsh Setup
```
brew install zsh
```

### Install Oh My Zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

- If the  installation script doesn't set zsh to your default shell run:
  ```
  chsh -s $(which zsh)
  ```
## Zsh Cofiguration

#### Plugins

Add plugins to your shell in the `.zshrc` file like so:
```
plugins=(
  git
  nvm
  yarn
  zsh-autosuggestions
  zsh-syntax-highlighting
  z
)
```
- git, nvm, yarn, and z are all included in oh-my-zsh
  
 - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
    ```
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```

- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
  ```
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting 
  ```


Anytime changes are made to the `.zshrc` file run
 ```
 source ~/.zshrc
 ``` 

### Theme

[PowerLevel10k](https://github.com/romkatv/powerlevel10k#oh-my-zsh) is my preferred theme to use and very easy to setup. Just follow the prompts in the terminal.