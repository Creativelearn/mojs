# Contributing to mojs

First of all, thank for taking time to contribute!

The following is a set of guidelines for contributing to mojs. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.


#### Table Of Contents

1. [Code of conduct](#code-of-conduct)
2. [Reporting bugs](#reporting-bugs)
3. [Suggesting enhancements](#suggesting-enhancements)
4. [Working with the project](#working-with-the-project)


## Code of conduct

This project and everyone participating in it is governed by the [mojs of conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [xavier.foucrier@gmail.com](mailto:xavier.foucrier@gmail.com).


## Reporting bugs

This section guides you through submitting a bug report for mojs. Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports.

Before creating bug reports, please check the [issues list](https://github.com/mojs/mojs/issues) as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible.

### Before submitting a bug report

* **Perform a [cursory search](https://github.com/mojs/mojs/issues)** to see if the problem has already been reported. If it has **and the issue is still open**, add a comment to the existing issue instead of opening a new one.

### How do I submit a (good) bug report?

Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues). After you've determined which repository your bug is related to, create an issue on that repository and provide the following information by filling in the template.

* Use a **clear and descriptive title** for the issue to identify the problem
* Describe the **exact steps** which reproduce the problem in as many details as possible
* Explain which behavior **you expected to see** instead and why
* Explain the problem and **include additional details** to help maintainers reproduce the problem
* Include details about your **configuration and environment**
* Include screenshots and animated GIFs if needed
* Specify which version of mojs you're using


## Suggesting enhancements

This section guides you through submitting an enhancement suggestion for mojs, including completely new features and minor improvements to existing functionality. Following these guidelines helps maintainers and the community understand your suggestion and find related suggestions.

* Use a **clear and descriptive title** for the issue to identify the suggestion
* Provide a **step-by-step description of the suggested enhancement** in as many details as possible
* Describe the current behavior and explain **which behavior you expected to see** instead and why
* Explain **why this enhancement would be useful** to most mojs users
* List some other applications **where this enhancement exists**

Don't hesitate to use pull requests to propose code changes.


## Working with the project

MoJS uses [Webpack](https://webpack.js.org/) and [Babel](https://babeljs.io/) for building, [Karma](https://karma-runner.github.io/) for testing and [Github Actions](https://github.com/mojs/mojs/actions) for the CI workflow.

> Most of the core files are written in [CoffeeScript](https://coffeescript.org/), but the plan is to convert to TypeScript in the future.

### Setup

Make sure your environment well fit the `package.json` **engines** field, which is, at the time of writing, aligned with **NodeJS 18** and **NPM 8**.

Run `npm install` to get all dependencies and build tools to get ready!

### Scripts

- `npm run dev` - Start a `webpack-dev-server` and allow you to **develop new features** by seeing them live in your browser. Source map is also enabled to allow easy bug fixes in development.
- `npm run lint` - Run `eslint` to lint the code and **prevent syntax errors** when implementing new code.
- `npm run test` - Run all tests by creating a production-ready file, looking for **Karma tests** in the spec folder, and checking them against the `dist/mo.umd.js` file. Make sure to write new tests for all new code.
- `npm run build` - Build a **production-ready** `mo.umd.js` file with webpack and put it in the `dist` folder.

### Workflow

The Continuous Integration workflow uses **BrowserStack** to run Karma tests against a bunch of selected browsers for compatibility reasons. When running tests locally, **Headless Chrome** will be used as default browser.

Thanks for reading and happy contributing! :tada: :+1:
