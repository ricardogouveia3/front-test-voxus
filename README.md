# Gulp Boilerplate

This project uses:

- [Pug](https://pugjs.org/)
- [Sass](http://sass-lang.com/)
- [Gulp](https://gulpjs.com/)
- [Browsersync](https://www.browsersync.io/)

## Getting Started

### Installation

First of all, install the dependencies to run this boilerplate.

- [NodeJS](http://nodejs.org/)
- [Gulp](https://gulpjs.com/)

```sh

# Clone this repository
git clone git@github.com:ricardogouveia3/gulp-boilerplate.git
cd gulp-boilerplate

# install dependencies
npm install

```

After that, you should be good to go :)

### Folders/Files Structure

```sh
├── assets/
│   ├── sass/
│   │   ├── partials/
│   │   │   └── _*.sass
│   │   └── style.sass
│   │   └── variables.sass
│   ├── img/
│   │   └── *.{jpg||png||svg}
├── build/
│   ├── assets/
│   │   ├── css/
│   │   │   └── style.min.css
│   │   └── img/
│   │       └── *.min.{jpg||png||svg}
│   ├── js/
│   │   └── index.min.js
│   ├── *.html
│   └── favicon.ico
├── js/
│   └── *.js
├── pug/
│   └── *.pug
├── .editorconfig
├── .gitignore
├── gulpfile.js
├── package.json
└── README.md
```

### Tasks

#### Dev Tasks

These tasks are used for live reloadind and debugging. They are time saving focused. Don't use then for deploying.

- `gulp pug-dev`: Compiles `index.pug` into `index.html` on root directory.
- `gulp sass-dev`: Compiles `style.sass` and its dependencies; concat result to style.min.css (expanded style in this step).
- `gulp js-dev`: Concat `*.js` from modules into `index.min.js`.

#### Build Tasks

These tasks are used for building and deploying. They are perforance and good practice focused. They may be to slow for live reloading (or may cause looping task).

- `gulp pug-build`: Compiles `index.pug` into `index.html` on root directory.
- `gulp sass-build`: Compiles `style.sass` and its dependencies; autoprefix resulting css; concat result to style.min.css.
- `gulp js-build`: Concat `*.js` from modules into `index.min.js`.
- `gulp image-build`: Optimize images (jpg, png, svg) from assets.

#### Server/Live Tasks

- `gulp watch`: Starts browsersync. Watch for chances in `.pug`, `.sass` and `.js` files. Calls dev tasks.
- `gulp browsersync`: Calls browsersync.

#### Default tasks

- `gulp`: Calls watch. Used for dev stages.
- `gulp build`: Calls build tasks. Used for buiding.

## License

[MIT License](http://ricardogouveia3.mit-license.org/) © Ricardo Álvaro Gouveia Gomes Filho
