# Contributing

:mega: **Support/Questions?**: Please see our [Support
Page](http://ionicframework.com/support) for general support questions. The
issues on GitHub should be reserved for bug reports and feature requests.

### Bug Reports

Run the command(s) with `--verbose` to produce debugging output. We may ask for
the full command output, including debug statements.

Please also copy/paste the output of the `ionic info` command into your issue
and be as descriptive as possible. Include any steps that might help us
reproduce your issue.

### Feature Requests

Post an issue describing your feature to open a dialogue with us. We're happy
to hear from you!

### Pull Requests

Pull requests are most welcome! But, if you plan to add features or do large
refactors, please **open a dialogue** with us first by creating an issue. Small
bug fixes are welcome any time.

#### Local Setup

##### Structure

Our CLI is organized into a single multi-package repository. Common tools, such
as Typescript and jest, are installed in the base directory while package
dependencies are each installed in their respective `packages/**/node_modules`
directories.

Each `packages/*` folder represents a package on npm.

* `packages/ionic`: Executable package.
* `packages/@ionic/cli-utils`: Utilities package.
* `packages/@ionic/cli-plugin-*`: CLI plugins.

##### Toolset

* npm 5 is required.
* We recommend Node 7.6+.
* Our codebase is written in [Typescript](https://www.typescriptlang.org/). If
  you're unfamiliar with Typescript, we recommend using [VS
  Code](https://code.visualstudio.com/) and finding a tutorial to familiarize
  yourself with basic concepts.
* Our test suite uses [Jest](https://facebook.github.io/jest/).

##### Setup

1. Fork the repo & clone it locally.
1. `npm install` to install the dev tools.
1. `npm run bootstrap` (will install package dependencies and link packages
   together)
1. Optionally `npm run link` to make `ionic` point to your dev CLI.
1. `npm run watch` will spin up TS & JS watch scripts for all packages.
1. Typescript source files are in `packages/*/src`.
1. Good luck! :muscle: Please open an issue if you have questions or something
   is unclear.

##### Running Dev CLI

You can switch between your dev CLI and stable with `npm run link` and `npm run
unlink && npm i -g ionic`.

##### Code Structure

TODO: Be helpful about where to look for commands, utilities, etc.

##### Publishing Notes

Cancel any watch scripts before proceeding.

* **testing releases**: `npm run publish:testing`
* **canary releases**: `npm run publish:canary`
* **stable releases**: `npm run publish`
