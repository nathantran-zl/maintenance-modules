# maintenance-modules

[![NPM](https://nodei.co/npm/maintenance-modules.png)](https://nodei.co/npm/maintenance-modules/)

There is no code in this module, the only thing is this README file.

This is a list of modules that are useful for maintaining or developing modules (in no particular order).

### [fixpack](https://github.com/henrikjoreteg/fixpack) by [henrikjoreteg](https://www.npmjs.com/~henrikjoreteg)

A package.json file scrubber for the truly insane. Cleans up your package.json in a deterministic way to ensure high quality, handcrafted, artisinal JSON.

```
npm i fixpack --save-dev
```

### [standard](https://github.com/feross/standard) by [feross](https://www.npmjs.com/~feross)

JavaScript standard style checker/linter. No options allowed! Uses non-configurable opinionated settings to minimize bikeshedding. Never give style feedback on a pull request again!

```
npm i standard --save-dev
```

### [dependency-check](https://github.com/maxogden/dependency-check) by [maxogden](https://www.npmjs.com/~maxogden)

Checks which modules you have used in your code and then makes sure they are listed as dependencies in your package.json (or vice versa).

```
npm i dependency-check --save-dev
```

### [create-module](https://github.com/finnp/create-module) by [finnp](https://www.npmjs.com/~finnpauls)

Helper tool for the usual steps to create a module. Creates empty github repo, generates module boilerplate, runs npm init, does first commit + push, etc.

```
npm i create-module --save-dev
```

### [travisjs](https://github.com/finnp/node-travisjs) by [finnp](https://www.npmjs.com/~finnpauls)

A command line module for travis, especially targeted for managing tests for node modules. Helps you quickly add a travis hook + generate a travis badge for your readme.

```
npm i travisjs --save-dev
```

### [gh-pages-deploy](https://github.com/meandavejustice/gh-pages-deploy) by [meandave](https://www.npmjs.com/~meandave)

Deploy to gh-pages with one command. Lets you add static build settings into your package.json and then automatically build, deploy and push to gh-pages from master using this module.

```
npm i gh-pages-deploy --save-dev
```

### [npm-release](https://github.com/phuu/npm-release) by [phuu](https://www.npmjs.com/~phuu)

Tiny tool for releasing npm modules. Bumps, commits, tags, pushes and publishes.

```
npm i npm-release --save-dev
```

### [npm-check-updates](https://github.com/tjunnone/npm-check-updates) by [tjunnone](https://www.npmjs.com/~tjunnone)

Find newer versions of dependencies than what your package.json allows.

```
npm i npm-check-updates --save-dev
```

### [npe](https://github.com/zeke/npe) by [zeke](https://npmjs.org/~zeke)

Node Package Editor: a CLI for one-off inspection and editing of properties in package.json files. Lets you avoid having to hand-edit JSON.

```
npm i npe -g
```

### [package-json-to-readme](https://github.com/zeke/package-json-to-readme) by [zeke](https://npmjs.org/~zeke)

Generate a README.md from package.json contents. With npm modules, lots of info can be gleaned from properties in the package.json file: name, description, scripts.test, preferGlobal, etc. That's why package-json-to-readme exists. Use it to generate a decent boilerplate README, then iterate from there. 

```
npm i package-json-to-readme -g
```

### [npmwd](https://github.com/zeke/npmwd) by [zeke](https://npmjs.org/~zeke)

Open the npm package URL in your browser that matches your shell's current working directory.

```
npm i npmwd -g
```

### [foundry](https://github.com/twolfson/foundry) by [twolfson](https://www.npmjs.com/~twolfson)

Release manager for npm, bower, component, PyPI, git tags, and any plugin you can write. Publish to multiple package repositories at once.

```
npm i foundry --save-dev
```

### [semantic-release](https://github.com/boennemann/semantic-release) by [boennemann](https://www.npmjs.com/~boennemann)

Fully automate your package's releases. This will determine not only which version to release, but also when – all without you having to care about it ever again. The goal of this package is to remove humans from version numbers and releases. Check out the readme for more info!

```
npm i semantic-release --save-dev
```

### [collaborator](https://github.com/maxogden/collaborator) by [maxogden](https://www.npmjs.com/~maxogden)

Easily add new collaborators to your github repos + npm packages from the CLI, and then generate a `collaborators.md` file with the newly updated list of collaborators. Use this to add new maintainers to your projects.

```
npm i collaborator -g
```

### [gasket](https://www.npmjs.com/package/gasket) by [mafintosh](https://www.npmjs.com/~mafintosh)

Preconfigured pipelines for node.js. A more powerful version of npm scripts, but less frameworky than gulp or grunt. Useful for when you might use Makefiles or bash scripts but want your pipelines to be cross platform.

```
npm i gasket --save-dev
```

## maintenance bash scripts

```
alias patch='pre-version && npm version patch && post-version'
alias minor='pre-version && npm version minor && post-version'
alias major='pre-version && npm version major && post-version'
alias pre-version='git diff --exit-code && npm prune && npm install -q && npm test'
alias post-version='(npm run build; exit 0) && git diff --exit-code && git push && git push --tags && npm publish'
```

- https://gist.github.com/sindresorhus/8435329
