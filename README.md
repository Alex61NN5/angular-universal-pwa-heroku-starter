# Angular 7 Universal Heroku Starter

![angular-badge](https://img.shields.io/badge/Angular-7.0.5-red.svg) [![Maintenance](https://img.shields.io/badge/Maintained-yes-green.svg)](https://github.com/Alex61NN5/angular-universal-heroku-starter/graphs/commit-activity) ![awesome](https://img.shields.io/badge/awesome-yes-blue.svg) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/Alex61NN5/angular-universal-heroku-starter/issues) [![GitHub contributors](https://img.shields.io/github/contributors/Naereen/StrapDown.js.svg)](https://github.com/Alex61NN5/angular-universal-heroku-starter/graphs/contributors/)

![angular-universal](https://user-images.githubusercontent.com/20350641/48462006-7ab8c500-e82a-11e8-8f0a-cedf39303957.png)

**DEMO SITE**
https://angular-heroku-starter.herokuapp.com/

**This is a starting point for an Angular Universal application that can then be published correctly to heroku with working SSR(server side rendering)**

This starter was created by creating a new angular application with `@angular/cli@7.0.5` and combining the techniques shown in these two articles.

[deploying-an-angular-universal-app-to-heroku](https://medium.com/augie-gardner/deploying-an-angular-universal-app-to-heroku-eca2b7966947)

[enable-angular-universal-for-existing-app](https://medium.com/@mafshin/enable-angular-universal-for-existing-app-3a17694b9177)

and some additional configuration to get it all working on Angular 7

If you're looking for the Angular Universal repo go to [angular/universal](https://github.com/angular/universal)

## Getting Started

Download the project files and install the dependencies. this project is set up with `yarn`

```
$ git clone https://github.com/Alex61NN5/angular-universal-heroku-starter.git
$ cd angular-universal-heroku-starter
```
then run `yarn`

The `package.json` has an engines section that specifies the node and yarn version to use for the heroku build

In your terminal run the following commands
```
$ node -v
$ yarn -v // or npm -v
```
now either update your node and yarn/npm to match the ones found in the package.json or change the engines to match your versions otherwise when you try to install packages it will throw an error

```
"engines": {
    "node": "9.2.1",
    "yarn": "1.5.1"
},
```

If you wish to use `npm` instead make sure you delete the `yarn.lock` file from the project and then change the `engines` to use the version of `npm` you are running to find this out run `npm -v` an example of what this would look like is 

```
"engines": {
    "node": "9.2.1",
    "npm": "6.4.1"
},
```

You will probably want to change the project name so what you will need to do is do a find and replace of `angular-universal-heroku-starter` and change everything to your new project name. Most of this stuff will be in the angular.json


### Development

To run this project for development you can use the command `ng serve` or `npm start`

This project uses [husky](https://github.com/typicode/husky) to implement git-hooks and [commitLint](https://github.com/marionebl/commitlint) to check commit messages. If you do not wish to use these features remove this from your package.json

```
"husky": {
  "hooks": {
    "pre-commit": "ng lint",
    "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
  }
},
```
remove the `commitlint.config.js` file from the src directory and then run 

`yarn remove husky @commitlint/cli @commitlint/config-angular`

### Test Production/Server Side Rendering

`npm run build:ssr` - Compiles your application and spins up a Node Express to serve your Universal application on http://localhost:4000

## Heroku

**IMPORTANT** For the heroku deploy to work correctly you must change this line in your package.json to match the new name of the project

`"build:client-and-server-bundles": "ng build --prod && ng run <YOUR-PROJECT-NAME>:server"`

#### To deploy to heroku

```
$ git init
$ heroku login
$ heroku create
$ git add .
$ git commit -m "initial commit"
$ git push heroku master
$ heroku open
```

## Universal "Gotchas"

https://github.com/angular/universal/blob/master/docs/gotchas.md

### Contribution

Before contributing please read the [contribution guidelines](https://github.com/Alex61NN5/angular-universal-heroku-starter/blob/master/CONTRIBUTING.md)

### Licence
<hr>

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](/LICENSE)
