# Angular 7 Universal Heroku Starter

![angular-badge](https://img.shields.io/badge/Angular-7.0.5-red.svg) [![Maintenance](https://img.shields.io/badge/Maintained-yes-green.svg)](https://github.com/Alex61NN5/angular-universal-heroku-starter/graphs/commit-activity) [![GitHub contributors](https://img.shields.io/github/contributors/Naereen/StrapDown.js.svg)](https://github.com/Alex61NN5/angular-universal-heroku-starter/graphs/contributors/)

![angular-universal](https://user-images.githubusercontent.com/20350641/48462006-7ab8c500-e82a-11e8-8f0a-cedf39303957.png)

**This is a starting point for an Angular Universal application that can then be published correctly to heroku with working SSR(server side rendering)**

This starter was created by creating a new angular application with `@angular/cli@7.0.5` and combining the techniques shown in these two articles.

[deploying-an-angular-universal-app-to-heroku](https://medium.com/augie-gardner/deploying-an-angular-universal-app-to-heroku-eca2b7966947)

[enable-angular-universal-for-existing-app](https://medium.com/@mafshin/enable-angular-universal-for-existing-app-3a17694b9177)

and some additional configuration to get it all working on Angular 7

If you're looking for the Angular Universal repo go to [angular/universal](https://github.com/angular/universal)

## Getting Started

Download the project files and install the dependencies. this project is set up with `yarn`, you can switch to `npm` but make sure you delete the `yarn.lock` file otherwise heroku will throw an error

```
$ git clone https://github.com/Alex61NN5/angular-universal-heroku-starter.git
$ cd angular-universal-heroku-starter
```
then run `yarn` or `npm install` depending on which package manager you choose.

### Development

To run this project for development you can use the command `ng serve` or `npm start`

### Test Production/Server Side Rendering

`npm build:ssr` - Compiles your application and spins up a Node Express to serve your Universal application on http://localhost:4000

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

If you would like to contribute to this repo, please fork and then create a pull request.

### Licence
<hr>

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](/LICENSE)
