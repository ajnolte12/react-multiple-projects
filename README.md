This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

## How to Run locally
1. `npm run start`

## How to Build
1. `npm run build`
2. Files will be placed in the build folder
3. React and react-dom will not be included in the bundle and will need to be included externally

## How To Add New Webpart

1. Add new folder under src/webparts
    * Create index.js that uses ReactDom.render
    * Reference existing index.js
    * Create your main App.js
2. Add your entry to config/paths.js
3. Add your entry to config/webpack.config.{dev/prod}.js

## Changes made to create-react-app
* Ran `npm run eject`
* Added multiple entries to webpack.config.{dev/prod}.js
  * Added entry points to paths.js
  * Modified scripts/build and scripts/start to check for correct required files
* Add react and react dom as externals in webpack.config.prod.js
* Added two seperate index.html files for dev/prod
  * dev-index does not load react from cdn, react and react-dom are bundled in webpack.config.dev.js
  * prod-index includes react from cdn, react and react-dom are not bundled in webpack.config.prod.js (added as externals)