###  the-sod
#### I have developed the theme from Scratch.
- Theme options
- Header 
- footer 
- Navigation menu 
- font 
-  portfolio 
-  category 
-  custom post type etc.
#### Features
* Build Process
* Typescript support
* Bundled with webpack 4
* Implements async chunk loading via @loadable/react
* Supports ES6 via Babel transpiling
#### State Management
* redux-entity for domain entity management
* redux-thunk for asynchronous actions
* redux-logger for capturing actions
#### Routing
* react-router v5 for client-side routing
* Async chunk loading at the react-router level
#### HTTP
Customizable, Promise-based HTTP support via Axios
Utilizes a a generic data service to easily fetch data
Example of implementing the data service
#### Styling
* Supports SCSS & SASS syntax
* Browser compatibility via autoprefixing
* Bulma for out-of-the-box styling
#### Develop & Deploy
Environmental configurations for both webpack and redux
Dev: webpack-dev-server with React Hot Loader. redux-logger enabled
Prod: Express server with redux-logger disabled
#### Getting Started
$ git clone https://github.com/mikechabot/react-boilerplate.git
$ npm install
Launch environment:
Production: $ npm start
Development: $ npm run dev
Available at http://localhost:3060
Update port via config.default.json, or override via Custom Configuration

#### Build assets for production:
$ npm run build:prod
Execute tests:
$ npm test
#### Custom Configuration
Use cross-env or a comparable library/command to set the ENV_CONFIG_PATH to the path of your JSON configuration file:

$ cross-env ENV_CONFIG_PATH=/path/to/config.json npm start

Note: This path is made available to Webpack only, however the contents of the file are stamped on a global variable during the build process (process.env.APP_CONFIG, see webpack.config.js), which is then accessible via the ConfigService.

If your configuration is loaded successfully, you can expect to see the following indicator during startup:

** Using custom configuration located at "/path/to/config.json" **
##### Example
Using configuration file @ C:\_workspaces\custom-config.json

$ cross-env ENV_CONFIG_PATH="C:\_workspaces\custom-config.json" npm start

> react-boilerplate@5.0.0 start C:\_workspaces\react-boilerplate
> npm run build:prod && npm run start-prod-server


> react-boilerplate@5.0.0 build:prod C:\_workspaces\react-boilerplate
> npm run clean && cross-env NODE_ENV=production webpack --progress --colors


> react-boilerplate@5.0.0 clean C:\_workspaces\react-boilerplate
> rm -rf ./docs

** Using custom configuration located at "C:\_workspaces\custom-config.json" **
