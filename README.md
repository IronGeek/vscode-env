# ENV

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/IronGeek/vscode-env/Publish?logo=github-actions&logoColor=ffffff)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/IronGeek/vscode-env?logo=github)
![GitHub package.json version](https://img.shields.io/github/package-json/v/IronGeek/vscode-env)
![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/IronGeek.vscode-env?logo=visual-studio-code)
![GitHub](https://img.shields.io/github/license/IronGeek/vscode-env)

Adds formatting and syntax highlighting support for env files (`.env`) to Visual Studio Code  

## Features

- Syntax highlighting

  ![Syntax highlighting](images/highlighting.gif)

- Folding

  The extension will enable folding on file content that are wrapped with the following pattern:

  ```text
  # ...       << begin with comment(s)
  ...
  ...         << folded content
  ...
              << end with a blank line
  ```

  ![Folding](images/folding.gif)

- Formatting

  Use the `Format Document` command (<kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>I</kbd>) from the `Command Pallete` (<kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>P</kbd>) to format the current env file  

  ![Formatting](images/formatting.gif)

## Custom env file extension

The extension support env files with the following extensions:

- `.env`
- `.env.sample`
- `.env.example`

To enable support for other env files with specific naming convention/ file extension, use the `files.associations` settings in Visual Studio Code.

For example, the following settings will enable support for `.env.development` and `.env.production` files:

```json
  "files.associations": {
    ".env.development": "env",
    ".env.production": "env"
  }
```

## Acknowledgements

- [Mike Stead](https://github.com/mikestead) for [dotenv extension for vscode](https://github.com/mikestead/vscode-dotenv)  

## License

This project is licensed under the terms of the [MIT license](LICENSE).
