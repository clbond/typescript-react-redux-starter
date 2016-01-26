# TypeScript/React/Redux Starter

This is the initial version of our starter project using React, TypeScript and Webpack to tie it all together.

## Commands

* `npm install`: install npm dependencies specified in package.json as well as typings specified in tsd.json (typings will be put into *typings* folder which is also git ignored).
* `postinstall`: runs automatically after `npm install` and triggers a `npm run build` to provide a build directory to `npm start` by default

* `npm run dev`: will start a development server (with live reloading) on [http://localhost:3000](http://localhost:3000). Note that in this case the bundle will be generated in memory and your bundle in *dist* might get out of sync.
* `npm start`: starts a production server serving the *dist* directory on [http://localhost:3000](http://localhost:3000)

* `npm run build`: bundle all of the application including js/css/html files, with index.html generated according to a template specified in *index.html* (Everything will be put into *dist* folder).

> Note: Demo username/password can be found [here](https://github.com/rangle/typescript-react-redux-starter/blob/master/src/api/mock/users.tsx)


## Improvements

This is an initial version of this setup and will be expanded in the future. Refer to the [issues section](https://github.com/rangle/typescript-react-redux-starter/issues) to see what needs to be done, or create a [new one](https://github.com/rangle/typescript-react-redux-starter/issues/new).

### Planned work

* Fix/ReOrg BassCSS styles
* Better support for custom typings (so we don't have to commit typings to the repo)
* Test examples (spec & unit)
* Component `displayName`, `propTypes`, `defaultProps` and documentation
* Auto-reloading API server (when specified)
* Enforce single-quotes for TS code and double-quotes for JSX.
  - ref: https://github.com/palantir/tslint/issues/673


## If something doesn't work

Refer to the [issues section](https://github.com/rangle/typescript-react-redux-starter/issues) to see if this has already been logged. Otherwise create a [new issue](https://github.com/rangle/typescript-react-redux-starter/issues/new).

## Want to deploy on Heroku?  Read this.

By default, Heroku's node stack runs `npm install --production`, which ignores the  `devDependencies`
section of your `package.json`. The convention in these cases is that only what is necessary 
for the actual production run should be in `dependencies`.

However this is at odds with modern JS bundlers like webpack, where almost everything is a `devDependency`;
because Heroku does not separate the build and run environments, its default setup isn't the
best fit.

Here is a workaround: https://devcenter.heroku.com/articles/nodejs-support#customizing-the-build-process
