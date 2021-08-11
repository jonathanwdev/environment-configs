<h1>My Vscode Configs :)</h1><br>

```

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
  
}

GIT

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
	
	
ZSH

export PATH=~/.npm-global/bin:$PATH

export ZSH=$HOME/.oh-my-zsh


export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"


ZSH_THEME="spaceship"






plugins=(git)

source $ZSH/oh-my-zsh.sh


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
SPACESHIP_USER_SHOW=always
SPACESHIP_PROMPT_ADD_NEWLINE=true
SPACESHIP_CHAR_SYMBOL="🂮"
SPACESHIP_CHAR_SUFFIX=" "



zinit light zdharma/fast-syntax-highlighting
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions

```

