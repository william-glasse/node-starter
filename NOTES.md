Packages to install


✅ Git - .gitignore
✅Eslint (configs: AirBnB, prettier) plugins: (prettier)
✅    .eslintrc file, .eslintignore,   
✅ Create dummy source file and test file
✅ Prettier
✅    .prettierrc, .prettierignore,
✅ Add extensions - Prettier, Eslint
✅ Jest
    ✅ jest.config.js,
    ✅ add npm script for running jest in watch mode
Husky
    commitmessage, precommit, prepush hooks.
Commitlint
    commitlint.config.js
TypeSync
Automatically get EsLint to run fix (lint-staged, precommit)
Setup Git repository remotely.






Gearoids lint staged
"lint-staged": {
    "*": [
      "npm run detect-secrets"
    ],
    "*.js": [
      "eslint --cache --fix",
      "git add"
    ],
    "**/*.{css,html,js,json,md,page,xml,yaml,yml}": [
      "prettier --write",
      "git add"
    ],
    "package.json": [
      "typesync --silent",
      "sort-package-json",
      "git add"
    ]
  },