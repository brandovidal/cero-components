# Cero Components
Zero to Production is a project in which we will build a productivity management application. In this series of live broadcasts, I will be revealing all the complications that a programmer has when building a web app. This project is live streamed in https://glrz.me/glrodasz.

## Methodologies
### Atomic Design
For this project will be using the methodology to create componentes called [Atomic Design](https://shop.bradfrost.com/products/atomic-design-ebook). The component library will be creating just **Atoms** and **Molecules** with the following definitions:

#### Atoms definition
For this project an atom will be a component that is composed by an unique Atom with or without HTML tags, or just HTML tags.
#### Molecules definition
For this project a molecule is a component that is composed by at least 2 different atoms.

## Components Library
These are the instructions about how this components library project has been created for future reference.
### Storybook configuration
- Start the project with `npx sb init`.
- Choose that is a `React` project.
- Run `yarn storybook`.
- Add global styles `globals.css`.
- Add reset styles `https://jgthms.com/minireset.css`.
- Add typography from **Google Fonts**.
### Design Tokens
- Create `tokens/index.js` file.
- Create `build-tokens` script
- Add brand colors to tokens
- FIXME: Add the rest of tokens
### Create template script
- Create a template script for copy the template of a component with 
the following structure `templates/components` and files:
```
Component.js
Component.module.css
Component.stories.js
index.js
```
- Include inquirer to choose the options from the terminal
- TODO: Copy and parse the rest of template files
### Atoms & Molecules
- Create Heading Atom
- Create Paragraph Atom*
- Create Button Atom
- Create Icon Atom
- Create Picture Atom
- Create ButtonIcon Molecule
- Create Spacer's Layout
- Create Avatar Atom
- Create Card Atom
### Lint and styling
- Add a modified version of [EditorConfig](https://github.com/airbnb/javascript/blob/master/.editorconfig)
1. Install ESLint and create a config file following the instructions [here](https://eslint.org/docs/user-guide/getting-started#installation-and-usage)
2. Install Prettier `yarn add --dev prettier`
3. Install the prettier configuration along ESLint following [these](https://github.com/prettier/eslint-plugin-prettier#recommended-configuration) instructions
4. Finally configure the precommit hook with lint-staged [here](https://prettier.io/docs/en/precommit.html#option-1-lint-stagedhttpsgithubcomokonetlint-staged)
5. TODO: Configure stylelint
### Creating tests
1. Install Jest for React following [this](https://jestjs.io/docs/en/tutorial-react) instructions.
2. Mock the CSS and CSS Modules files for Storybook [here](https://jestjs.io/docs/en/webpack#mocking-css-modules)
3. Configure Storyshoots [here](https://storybook.js.org/docs/react/workflows/snapshot-testing)
4. Configure Chromatic in https://www.chromatic.com/
5. FIXME: Configure Chromatic with GitHub. Review with checks should with got with the Pull request.
6. TODO: Creating unit tests for `scripts` and `utils`
7. TODO: Create a coverage script with `instanbul`.
8. TODO: Upload the coverage HTML report to a service per pull request
### NPM scripts
- TODO: Create an script to watch when the `tokens/index.js` changes and build it. This script should be part of `yarn dev`.
### Github Actions
- FIXME: Create a GitHub action for a pull request
- FIXME: Create a GitHub action for a release
### PUblishing in NPM
- FIXME: Create the process of release a new version using `semantic-release`
- TODO: Configure commitizen to enable conventional commits messages
- TODO: Create a hook to force conventional commit messages
### Adding a Good README
- TODO: Create instructions to run this project in dev
- TODO: Create instructions to run the tests of this project
- TODO: Add NPM, Coverage, GitHub actions badges to the README.
- TODO: Create a `CONTRIBUTING.md` file with instructions.