# React-Without-CRA
Created an React app without using create react app command line utility.<br/>
steps followed to create react app from scratch:
- created and cloned the repository in github "React-Without-CRA".
- run the command to create package.json file an follow the instructions
  ```
  npm init
  ```
- run the command to install webpack as dev dependencies
  ```
  npm install --save-d webpack webpack-cli webpack-dev-server
  ```
- run the command to install babel presets as dev dependencies
  ```
  npm install --save-d @babel/core @babel/preset-env @babel/preset-react
  ```
- run the command to install babel loader and html webpack plugin as dev dependencies
  ```
  npm install --save-d babel-loader css-loader style-loader html-webpack-plugin
  ```
- create webpack.config.js file at the root level and add all the configurations
  - entry
  - output
  - module
  - plugins
- update package.json file to add babel presets and scripts:
  ```
  "babel": {
    "presets": [
      "@babel/preset-env",
      "@babel/preset-react"
    ]
  },
  "scripts": {
    "start": "webpack-dev-server --open",
    "create": "webpack --progress"
  }
  ```
- now you can run the command to ask webpack to run dev server which will open the app on port 8080
  ```
  npm run start
  ```
 - you can run the command to ask webpack to bundle all the js files into one bundle.js and add the reference in index.html file.
    this command will create dist folder and store index.html and bundle.js file and this you use in your prod to run an app.
    ```
    npm run create
    ```
 
