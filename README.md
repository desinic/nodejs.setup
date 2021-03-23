## Update Node

Please follow the below instructions to update node in your machine:

## Windows

1.Update npm
```text
npm install npm@latest -g
```
1.Clear npm cache
```text
npm cache clean -f
```
1.Install n
```text
npm install -g n
```
1.Install n
```text
Update node to latest version
```

## Mac
1.With Homebrew
```text
brew update
brew upgrade node
```

## Install and Update yarn

Please follow the below instructions to install or update yarn in your machine.

##On Windows
1.Install yarn
```text
npm install -g yarn
```

1.Update yarn
```text
yarn set version latest
```
## On Mac

1.Install yarn
```text
brew install yarn
```
1.Update yarn
```text
brew update
brew upgrade yarn
```
#VS Code Editor Setup

In order to follow along the tutorial series, I recommend you to use Visual Studio Code Editor and install & apply the below extensions and settings.

**Extensions**

-[Eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
-[Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
-[Path Autocomplete](https://marketplace.visualstudio.com/items?itemName=ionutvmi.path-autocomplete)

**Settings**
Go to your Visual Stuido Code `settings.json` file and add the below settings there:

```Json
// theme
  "workbench.colorTheme": "Andromeda Colorizer",
// config related to code formatting
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.formatOnSave": true,
"[javascript]": {
  "editor.formatOnSave": false
},
"prettier.disableLanguages": ["javascript"],
"editor.codeActionsOnSave": {
  "source.fixAll.eslint": true,
  "source.organizeImports": true
},
"eslint.alwaysShowStatus": true
```

##Linting Setup

In order to lint and format your code automatically according to popular airbnb style guide, I recommend you to follow the instructions as described in video. References are as below.

**Install Dev Dependencies**

```text
"lint": "yarn add -D eslint prettier && npx install-peerdeps --dev eslint-config-airbnb-base && yarn add -D eslint-config-prettier eslint-plugin-prettier"
```
**Setup Linting Configuration file**

Create a `.eslintrc.json` file in the project root and enter the below contents:

```Json
{
  "extends": ["prettier", "airbnb-base"],
  "parserOptions": {
    "ecmaVersion": 12
  },
  "env": {
    "commonjs": true,
    "node": true
  },
  "rules": {
    "no-console": 0,
    "indent": 0,
    "linebreak-style": 0,
    "prettier/prettier": [
      "error",
      {
        "trailingComma": "es5",
        "singleQuote": true,
        "printWidth": 100,
        "tabWidth": 4,
        "semi": true
      }
    ]
  },
  "plugins": ["prettier"]
}
```
