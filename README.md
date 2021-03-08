# Prettier Config

## Installation

```
npm install --save-dev @robinblomberg/prettier-config
```

## Configuration

Create a file called **.eslintrc.js** at the project root:

```javascript
module.exports = {
  extends: '@robinblomberg/robinblomberg'
}
```

## NPM scripts

Add the following scripts to your package.json (assuming that ESLint is enabled):

```json
{
  "scripts": {
    "format:scripts": "prettier --write src/**/*.{ts,tsx,js,jsx} && eslint src/**/*.{ts,tsx,js,jsx} --fix",
  }
}
```

Adjust the paths according to your project/file structure as necessary.

To run a script, enter the following in your command line:

```
npm run format:scripts
```

## VS Code settings

Add the following to **.vscode/settings.json** in the root of your project:

```json
{
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.insertSpaces": true,
  "editor.rulers": [100],
  "editor.tabSize": 2,
  "eslint.format.enable": false,
  "files.encoding": "utf8",
  "files.eol": "\n",
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true
}
```

This will check the formatting in VS Code, and also format on save.
