# javascript_tutorial1

Webpack 4 und Babel7
https://medium.com/@jeffrey.allen.lewis/the-ultimate-2018-webpack-4-and-babel-setup-guide-npm-yarn-dependencies-compared-entry-points-866b577da6a
https://www.valentinog.com/blog/webpack/

Create Nodejs projet:
npm init -y
=> creates package.json

Webpack dependencies:
npm install webpack webpack-cli webpack-dev-server --save-dev
=> gets necessary dependencies

Babel dependencies:
npm install @babel/cli @babel/core @babel/node @babel/preset-env @babel/register --save-dev
npm install babel-loader --save-dev
=> gets necessary dependencies

Seeing up Babel
Create a .babelrc file at the root
Add Babel presets
{
  "presets": [
    "@babel/preset-env"
  ]
}

Setting up Webpack
Create webpack.config.js at the root

Add in package.json
"scripts": {
  "dev": "webpack --mode development",
  "build": "webpack --mode production"
}

For Html Webpack plugin:
npm i html-webpack-plugin html-loader --save-dev

In webpack.config.js set:
const HtmlWebPackPlugin = require("html-webpack-plugin");
      {
        test: /\.html$/,
        use: [
          {
            loader: "html-loader",
            options: { minimize: true }
          }
        ]
      }
  plugins: [
    new HtmlWebPackPlugin({
      template: "./src/index.html",
      filename: "./index.html"
    })
  ]

Create an HTML file into ./src/index.html

https://wanago.io/2018/07/23/webpack-4-course-part-three-working-with-plugins/
npm i mini-css-extract-plugin css-loader --save-dev

