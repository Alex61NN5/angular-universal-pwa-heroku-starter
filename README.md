# Angular 7 Universal Heroku Starter

![angular-universal](https://user-images.githubusercontent.com/20350641/48462006-7ab8c500-e82a-11e8-8f0a-cedf39303957.png)

This starter was created by creating a new angular application with `@angular/cli@7.0.0` and combining the techniques shown in these two articles.

[deploying-an-angular-universal-app-to-heroku](https://medium.com/augie-gardner/deploying-an-angular-universal-app-to-heroku-eca2b7966947)

[enable-angular-universal-for-existing-app](https://medium.com/@mafshin/enable-angular-universal-for-existing-app-3a17694b9177)

and some additional configuration to get it all working on Angular 7

## Getting Started

// todo

## Installation

// todo

### Development

// todo

run with ng serve

### Test Production
// todo


## Server Side Rendering
// todo


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
