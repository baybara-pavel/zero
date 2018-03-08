<p align="center">
<img src=".github/zero-logo.png" width="400" />
</p>
<p align="center">
  <a href="https://extensions.zeplin.io">
    <img src="https://img.shields.io/badge/zeplin-extension-ffbe12.svg" alt="Zeplin Extension" />
  </a>
</p>
Start your Zeplin extension from Zero with Webpack.

If you want more power features without build process configuration – use official solution [zem](https://github.com/zeplin/zem)

## Zero includes

* Base project file structure
* Webpack (dev watching & production minification)
* Babel
* Prettier
* Eslint (AirBnB & Prettier)
* EditorConfig
* Husky & Lint-staged (pre-commit hooks)

## How to Start

First, you need last stable Node.js `^8.9.4`. Follow this [guide](https://github.com/creationix/nvm/blob/master/README.md#installation) if you don't have any.

Next, install project dependencies:

```bash
npm install
```

To start developing run:

```bash
npm start
```

Result build will be at `dist` dir. To add your extension into local macOS Zeplin client follow the instruction from official [tutorial](https://github.com/zeplin/zeplin-extension-documentation/blob/master/tutorial.md#adding-a-local-extension). Path to your local extension be like:

```
file://[absolute_path_to_zero_project_folder]/dist/manifest.json
```

Don't forget to replace `[absolute_path_to_zero_project_folder]` with your folder absolute path.

And finally, to get production ready build of your extension, just replace Zero credantials in `src/manifest.json` to yours and run following:

```bash
npm run build
```

## Project structure

```
zero
├── README.md
├── node_modules
├── package.json
├── package-lock.json
├── .eslintrc.js
├── .eslintignore
├── .prettierrc
├── .editorconfig
├── .gitignore
├── config
│   └── paths.js
│   └── webpack.common.js
│   └── webpack.dev.js
│   └── webpack.prod.js
├── dist                  <-- result extension build will be there
│   └── index.js
│   └── manifest.json
└── src
    └── _example-lib.js
    └── index.js
    └── manifest.json
```

## Extensions builded with Zero

* [Zepcode](https://github.com/artemnovichkov/zepcode) - Zeplin extension that generates Swift snippets from colors, fonts and layers

## Authors

Baybara Pavel, baybara.pavel@gmail.com

Artem Novichkov, novichkoff93@gmail.com [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/artemnovichkov?utm_source=github&utm_medium=button&utm_term=artemnovichkov&utm_campaign=github)

## License

Zero is available under the MIT license. See the LICENSE file for more info.
