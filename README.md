# Initial project with webpack, react, sass and typescript

## Crearte node project

```
npm init -y
```
## Install Webpack like development dependencies

```
npm -i -D webpack webpack-cli
```

## Install development server

```
npm -i -D webpack-dev-server
```

## Install React and React Router

```
npm -i -S react react-dom react-router-dom
```

## Install babel like development dependencies for use ES6 

```
npm i -D @babel/core @babel/preset-env @babel/preset-react babel-loader
```
## Create .babelrc file to configure babel

```
touch .babelrc
```
Add into .babelrc next configuration to babel

```
{
  "presets": ["@babel/preset-env", "@babel/preset-react"]
}
```

## Create webpack.config.js file

```
touch webpack.config.js
```

Add into webpack.config.js the initial configuration to webpack

```
const path = require("path");

module.exports = {
  entry: path.resolve(__dirname, "src/index.jsx"),
  output: {
    path: path.resolve(__dirname, "dist"),
    filename: "bundle.js"
  },
  resolve: {
    extensions: [".js", ".jsx"]
  },
  module: {
    rules: [
      {
        test: /\.(js|jsx)$/,
        exclude: /node_modules/,
        use: ["babel-loader"]
      }
    ]
  },
  devServer: {
    contentBase: path.resolve(__dirname, "dist"),
    port: 9000
  }
};
```

##


