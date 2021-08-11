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
  
}```

<h4>GIT</h4>

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

