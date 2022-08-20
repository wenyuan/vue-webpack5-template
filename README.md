# Vue Webpack5 Template

A generic Vue.js Project template based on Webpack5, which is not created by @vue/cli directly.

## Introduction

* This project is used to learn about WebPack5.
* Try to manual configuration according to various needs instead of using ready-made scaffolding tools.

## Preparation

```bash
git clone https://github.com/wenyuan/vue-webpack5-template.git

cd vue-webpack5-template/

npm install
```

## Usage

### Development

```bash
npm run serve
```

### Production

```bash
npm run build
```

> Note: You need to install [http-server](https://www.npmjs.com/package/http-server) globally to deploy a simple HTTP server.

```bash
npm install http-server -g
```

Watch the compiled page  by creating a server in the `dist` directory.

```bash
cd dist/ && http-server -c-1
```

## DevDependencies

This  template uses the following dependencies in dev mode and their specific purposes:

> The following  packages are installed by `npm install <package-name> --save-dev`.

### Webpack5

The most basic dependencies.

> TODO...( list core packages and their descriptions...)

### Babel

Babel is used to convert code written in ES6+ syntax to backward compatible JavaScript syntax.

> TODO...( list core packages and their descriptions...)

### Loaders

Tools specifically designed to handle files that are not JavaScript (Webpack recognizes JavaScript only by default) translate these resources into resources that Webpack recognizes.

> TODO...( list core packages and their descriptions...)

### Plugins

> TODO...( list core packages and their descriptions...)

## Associated Project

* [webpack-template](https://github.com/wenyuan/webpack-template): This is a generic Webpack5 template without any frontend framework(Neither based on Vue.js or React or others...)

## Thanks

Thanks to open source developers for their contributions.