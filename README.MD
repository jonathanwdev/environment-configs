<h1>My V Configs :)</h1><br>

```
<h4>VSCode</h4>
{
  "workbench.colorTheme": "Dracula",
  "editor.fontSize": 14,
  "editor.lineHeight": 22,
  "editor.fontFamily": "Fira Code",
  "editor.fontLigatures": true,
  "explorer.compactFolders": false,

  // Aplica linhas verticais para lembrar de quebrar linha em códigos muito grandes
  "editor.rulers": [
    80,
    120
  ],

  "[javascript]":{
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint":true, 
    }
  },

  "[javascriptreact]":{
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint":true, 
    }
  },

  "[typescript]":{
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint":true, 
    }
  },
  "[typescriptreact]":{
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint":true, 
    }
  },

  "editor.formatOnSave": false,
  "eslint.packageManager": "yarn",
  
  "files.associations": {
    ".sequelizerc": "javascript",
    "*.edge": "html"
  },
  // Aplica um sinal visual na esquerda da linha selecionada
  "editor.renderLineHighlight": "gutter",
  // Aumenta a fonte do terminal
  "terminal.integrated.fontSize": 14,
  // Define o tema dos ícones na sidebar
  "workbench.iconTheme": "material-icon-theme",
  "workbench.startupEditor": "newUntitledFile",
  "editor.tabSize": 2,
  "window.zoomLevel": 0,
  "extensions.ignoreRecommendations": true,
  "emmet.syntaxProfiles": {
    "javascript": "jsx",
  },
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
  },  
  "javascript.updateImportsOnFileMove.enabled": "never",
  "gitlens.codeLens.recentChange.enabled": false,
  "gitlens.codeLens.authors.enabled": false,
  "gitlens.codeLens.enabled": false,
  "breadcrumbs.enabled": true,
  "git.enableSmartCommit": true,
  "editor.parameterHints.enabled": false,
  "typescript.updateImportsOnFileMove.enabled": "never",
  "terminal.integrated.shell.osx": "/bin/zsh",
  "explorer.confirmDragAndDrop": false,
  "liveshare.featureSet": "insiders",
  "explorer.confirmDelete": false,
  "typescript.tsserver.log": "verbose",
  "javascript.suggest.autoImports": false,
  "typescript.suggest.autoImports": false,
  "workbench.activityBar.visible": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
  
}```

<h4>GIT</h4>
```
[user]
	name = Jonathan Souza
	email = jonathan.wdev@gmail.com
[push]
	followTags = true	
[core]
	editor = code --wait
[alias]
	s = !git status -s
	c = !git add -A && git commit -m
	l = !git log	--pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
```

<h4>ZSH</h4>
```
# If you come from bash you might have to change your $PATH.

export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
export ANDROID_HOME=~/android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:/usr/local/go/bin
export PATH=$PATH:~/android-studio/bin

export PATH=$HOME/bin:/usr/local/bin:$PATH

source "$HOME/.cargo/env"

# Path to your oh-my-zsh installation.
export ZSH="/home/jonathan/.oh-my-zsh"

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="spaceship"


plugins=(git)

source $ZSH/oh-my-zsh.sh

# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"

SPACESHIP_PROMPT_ORDER=(
  user          # Username section
  dir           # Current directory section
  host          # Hostname section
  git           # Git section (git_branch + git_status)
  hg            # Mercurial section (hg_branch  + hg_status)
  exec_time     # Execution time
  line_sep      # Line break
  vi_mode       # Vi-mode indicator
  jobs          # Background jobs indicator
  exit_code     # Exit code section
  char          # Prompt character
)

SPACESHIP_PROMPT_ADD_NEWLINE=false
SPACESHIP_CHAR_SYMBOL="❯"
SPACESHIP_CHAR_SUFFIX=" "




### Added by Zinit's installer
if [[ ! -f $HOME/.zinit/bin/zinit.zsh ]]; then
    print -P "%F{33}▓▒░ %F{220}Installing %F{33}DHARMA%F{220} Initiative Plugin Manager (%F{33}zdharma/zinit%F{220})…%f"
    command mkdir -p "$HOME/.zinit" && command chmod g-rwX "$HOME/.zinit"
    command git clone https://github.com/zdharma/zinit "$HOME/.zinit/bin" && \
        print -P "%F{33}▓▒░ %F{34}Installation successful.%f%b" || \
        print -P "%F{160}▓▒░ The clone has failed.%f%b"
fi

source "$HOME/.zinit/bin/zinit.zsh"
autoload -Uz _zinit
(( ${+_comps} )) && _comps[zinit]=_zinit

# Load a few important annexes, without Turbo
# (this is currently required for annexes)
zinit light-mode for \
    zinit-zsh/z-a-rust \
    zinit-zsh/z-a-as-monitor \
    zinit-zsh/z-a-patch-dl \
    zinit-zsh/z-a-bin-gem-node

### End of Zinit's installer chunk

zplugin light zsh-users/zsh-autosuggestions
zplugin light zsh-users/zsh-completions
zplugin light zdharma/fast-syntax-highlighting

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm


# Added by serverless binary installer
export PATH="$HOME/.serverless/bin:$PATH"
```