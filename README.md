# Basic Mac Setup

## Applications

### Browsers
- [Arc](https://arc.net) : Efficient, customizable browser with unique organizational features.
- [Google Chrome](https://www.google.com/chrome/index.html) : Fast, simple, Google-integrated web browser.
- [Firefox](https://www.mozilla.org/en-US/firefox/mac/) : Privacy-focused, customizable open-source browser.

### Productivity
- [1Password](https://1password.com/downloads/mac/) : Secure password manager and digital vault.
- [Notion](https://www.notion.so/desktop/mac) : All-in-one note-taking, task management, and organizational tool.
- [Slack](https://slack.com/downloads/mac) : Team communication and collaboration platform.
- [Discord](https://discord.com/download) : Community-centric voice, video, and text chat app.
- [Zoom](https://www.zoom.us/download#client_4meeting) : High-quality video conferencing and virtual meeting tool.

### Development
- [Raycast](https://www.raycast.com) : Streamlined command center for developer productivity.
- [Warp](https://www.warp.dev) : Fast, efficient, GPU-accelerated terminal application.
- [Visual Studio Code](https://code.visualstudio.com/) : Versatile and lightweight code editor with extensive extensions.
- [Xcode](https://apps.apple.com/gb/app/xcode/id497799835?mt=12) : Apple's IDE for macOS and iOS development.

## Initial Setup
1. Xcode Command Line tools (If Xcode IDE was installed, then this step can likely be skipped. Check with `xcode-select --print-path`)
    ```
    xcode-select --install
    ```
2. [Homebrew](https://brew.sh)
    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
3. [Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH) (Newer Macs come with Zsh by default. Check with `zsh --version`)
    ```
    brew install zsh
    ```
    - If the installation script doesn't set zsh to your default shell run:
      ```
      chsh -s $(which zsh)
      ```
4. [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh#basic-installation)
    ```
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
    - Add plugins to your shell in the `.zshrc` file like so:
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
      - **git**, **nvm**, **yarn**, and **z** are all included in oh-my-zsh
    - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)
      ```
      git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
      ```
   - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
     ```
     git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting 
     ```
5. [NVM](https://github.com/nvm-sh/nvm#installing-and-updating)
   ```
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | zsh
    nvm install node
    nvm install --lts
    nvm use node
    ```
    - Check to make sure everything stalled properly
      ```
      node -v && npm -v
      ```
- _*Anytime changes are made to the `.zshrc` file run `source ~/.zshrc`*_ 

### Shell Themes
- [Oh My Posh](https://ohmyposh.dev/docs/installation/macos)
- [PowerLevel10k](https://github.com/romkatv/powerlevel10k#oh-my-zsh)
- [Included Oh My Zsh Themes](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

### Fonts I like
- [Monaspace](https://monaspace.githubnext.com)
- [Hack Nerd Font](https://www.nerdfonts.com)
- [Victor Mono](https://rubjo.github.io/victor-mono/)
- [Fira Code](https://github.com/tonsky/FiraCode/wiki/Installing)
