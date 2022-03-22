<div id="top"></div>
<br />
<div align="center">
<h1 align="center">REACT App </h1>
</div>

## Installation

- Install TypeScript globally

  ```sh
  npm install -g typescript
  tsc --v # checks typescript version
  ```

- create-react-app:

  ```sh
  #Typescript
  npx create-react-app my-app --template typescript

  #Javascript
  npx create-react-app my-app
  ```

- prettier/eslint/husky

  ```sh
  #Typescript
  npm install -D eslint eslint-plugin-react prettier prettier-eslint eslint-plugin-jest eslint-plugin-react-hooks @typescript-eslint/eslint-plugin @typescript-eslint/parser husky @commitlint/{config-conventional,cli}

  #Javascript
  npm install -D eslint eslint-plugin-react prettier prettier-eslint eslint-plugin-jest eslint-plugin-react-hooks husky @commitlint/{config-conventional,cli}
  ```

- commitlint config

  ```sh
  echo "module.exports = {extends: ['@commitlint/config-conventional']};" > commitlint.config.js
  ```

- install git hooks

  ```sh
  yarn prepare / npm prepare
  ```

- add hooks

  ```sh
  # Add hook
  npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'
  # Sometimes above command doesn't work in some command interpreters
  # You can try other commands below to write npx --no -- commitlint --edit $1
  # in the commit-msg file.
  npx husky add .husky/commit-msg \"npx --no -- commitlint --edit '$1'\"
  # or
  npx husky add .husky/commit-msg "npx --no -- commitlint --edit $1"

  # or
  yarn husky add .husky/commit-msg 'yarn commitlint --edit $1'
  ```

## Contributing

1. Create your Feature Branch (`git checkout -b feature/amazing-feature`)
2. Commit your Changes (`git commit -m 'feat: Add some AmazingFeature'`)
3. Push to the Branch (`git push origin feature/AmazingFeature`)
4. Open a Merge Request

See the docs for commits convention https://www.conventionalcommits.org/

<p align="right">(<a href="#top">back to top</a>)</p>

<div id="vscode"></div>

## Setup VS Code

### Extensions

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint/)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode/)
- [Vue VS Code Extension Pack](https://marketplace.visualstudio.com/items?itemName=sdras.vue-vscode-extensionpack/)

- Set Prettier as your default formatter. Open up your command palette (Command + Shift + P) and look for Preferences: Open Settings (JSON). Then you’ll need to change your editor default formatter and add an extra config to format code when you save your files:

  ```sh
    {
      "editor.defaultFormatter": "esbenp.prettier-vscode",
      "editor.formatOnSave": true,
      "[javascript]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
      },
      "[typescript]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
      },
    }
  ```

<p align="right">(<a href="#top">back to top</a>)</p>
