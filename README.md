# Barker

Barker is an SCSS starter kit for design systems.

It includes:

- A [Style Dictionary](https://v4.styledictionary.com/) configuration for defining design tokens.
- A sensible project layout and organized SCSS files for themes, components, layouts, and base styles.
- SCSS mixins and functions for accessing design tokens.
- A [Webpack](https://webpack.js.org/) configuration with [Esbuild](https://esbuild.github.io/), [dart-sass](https://sass-lang.com/dart-sass/) and [PostCSS](https://postcss.org/).
- A [Stylelint](https://stylelint.io/) configuration.

## Usage

This kit cannot be installed and does not include any generators. Instead, clone
the repository into your project and adapt it to your needs.

```bash
git clone git@github.com:woylie/barker.git
cd barker
rm -rf .github .git
```

## Folder Structure

    .
    ├── build                   # Build artefacts (token definitions, CSS, etc.)
    │   ├── css                 # CSS output
    │   └── tokens              # Token output
    │       ├── css             # CSS custom properties
    │       ├── js              # JavaScript
    │       ├── css             # JSON definitions
    │       └── scss            # SCSS mixins and variables
    ├── src                     # Source files
    │   ├── css                 # Styles
    │   ├── js                  # JavaScript
    │   └── tokens              # Design Tokens
    └── ...

### Build Folder

The build folder contains the build artefacts.

    .
    ├── ...
    ├── build                   # Build artefacts
    │   ├── css                 # CSS output
    │   └── tokens              # Token output
    │       ├── css             # CSS custom properties
    │       ├── js              # JavaScript
    │       ├── css             # JSON definitions
    │       └── scss            # SCSS mixins and variables
    └── ...

### CSS Folders

    .
    ├── ...
    ├── src
    │   ├── css
    │   │   ├── _extends.scss           # SCSS placeholders for @extend
    │   │   ├── _functions.scss         # SCSS functions for using design tokens
    │   │   ├── _mixins.scss            # SCSS mixins
    │   │   ├── base                    # Global base layer
    │   │   │   ├── _animations.scss    # Keyframe animations
    │   │   │   ├── _general.scss       # Global styles
    │   │   │   ├── _index.scss         # Entry point for base layer
    │   │   │   └── _typography.scss    # Global typography styles
    │   │   ├── components              # Components are styled elements
    │   │   ├── layouts                 # Layouts arrange components on the page
    │   │   ├── main.scss               # Entry point
    │   │   ├── themes                  # Place for light/dark themes etc.
    │   │   └── utilities               # Utility classes generated from design tokens
    │   └── ...
    └── ...

## Commands

| Description                                         | Command                   |
| --------------------------------------------------- | ------------------------- |
| Development build (tokens, CSS, JS, etc.)           | `yarn build`              |
| Build Style Dictionary tokens                       | `yarn build-tokens`       |
| Watch mode (does not watch Style Dictionary tokens) | `yarn watch`              |
| Stylelint                                           | `yarn stylelint`          |
| Fix Stylelint issues                                | `yarn stylelint --fix`    |
| Format with Prettier                                | `yarn prettier . --write` |

## Resources

- The design token structure is based on [Design Tokens Format](https://design-tokens.github.io/community-group/format/) where possible.
- The structure is inspired by [CubeCSS](https://cube.fyi/), even though it isn't a faithful implementation.
- Barker is based on ideas described in the
  [Design Systems article series](https://www.mathiaspolligkeit.com/tags/design-systems/).
