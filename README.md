# Sasstastic
A starting point for any project using Sass.

## Setup
Simply point the sass compiler to `main.scss`. Every required file and directory inside the `sass` folder is already setup to be imported automatically in the correct order.

## Extension
You'll notice every folder contains an `index.scss` file. This file should be used to import every file at the same directory level as itself and any `index.scss` files present in child directories. This pattern makes sure every directory is responsible for only looking after it's own imports and parents do not need to know what is contained within child directories.

## Logistics
There are 4 primary folders included: `bem`, `config`, `utils` and `vanilla`.

### `bem`
Has two specific sub folders: `global` and `specific`.

#### `global`
Holds any global BEM components, examples include headers, content cards, carousels, footers etc.

#### `specific`
Holds any BEM components that are used on one or a couple pages in a very specific section of the application. If a component in here is being used in more than just one section, it should likely live in `global`. An example of a `specific` might be a `EmployeeCard` that is only used on the about us page and nowhere else.

### `config`
Holds any application configurations such as colors, fonts, headings and sizes etc that may likely be changed or altered as the application matures. This also provides a single source of truth for the overall application look and feel.

### `utils`
Holds any utility classes that do not fall into fully fledged BEM components. Examples include reusable color utilities that can be applied to specific elements in the HTML to override or set the foreground/background color.

### `vanilla`
Holds all the default selector styles. These are selectors that are typically used without any association to a specific BEM component. Such as an `h1` or `hr` or even the look an feel of `p`'s.

## License

MIT - Copyright (c) 2016 Tristan Strathearn <tristan@pixls.com.au>, see LICENSE.
