![KOAN](/client/images/koan.png)

[![Build Status](https://travis-ci.org/soygul/koan.svg?branch=master)](https://travis-ci.org/soygul/koan)

KOAN Stack is a boilerplate that provides a starting point for full stack JavaScript Web development with [Koa](https://github.com/koajs/koa), [AngularJS](http://angularjs.org/), and [Node.js](http://www.nodejs.org/) along with [MongoDB](https://www.mongodb.org/) and [WebSockets](https://developer.mozilla.org/en/docs/WebSockets). A summary of tech stack:
* **Client**: AngularJS and Bootstrap. Client side is fully static and CDN ready. All client packages are located at `client\bower_packages`.
* **Server**: Koa for RESTful API serving on Node.js. ES6 `async`/`await` functions all the way!
* WebSockets along with JSON-RPC is used for real-time client-server communication and browser sync.
* OAuth 2 is used for social authentications. Instead of auth cookies, we use JWT along with HTML5 *local storage*.
* Grunt tasks are used to facilitate development and testing.
* MongoDB for persistence.
* ## Live Example
Below are the screenshots from the bundled demo app, which is a Facebook like real-time sharing app. Follow instructions in the next section if you want to play with it locally, or deploy it to Heroku.

**Login page:**

![Login Page](/client/images/scrshot_login.png)

**User home page:**

![Home Page](/client/images/scrshot_home.png)
## Getting Started
Make sure that you have Node.js v7.6 or higher (for Node <7.6, use [v1.6 release](https://github.com/soygul/koan/releases/tag/v1.6)), and MongoDB v2 or higher (running on the default port 27017) installed on your computer. To get started with KOAN stack, do following:

```bash
git clone --depth 1 https://github.com/soygul/koan.git
cd koan
npm install
npm start
```

Your application should run on the 3000 port so in your browser just go to [http://localhost:3000](http://localhost:3000). If you want to run tests, simply type:

```bash
npm test
```

## Configuration
All configuration is specified in the [/server/config](/server/config/) directory, particularly the [config.js](/server/config/config.js) file. Here you can hook up any social app keys if you want integration with Twitter, Facebook, or Google.

## Heroku Deployment
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

`Procfile` and `app.json` are making this repo readily available for Heroku deployment. You can start by clicking the above button.
## Testing
You can run all the tests with `npm test`. Tests are run with:
* Client (unit): Jasmine + Karma (Angular default)
* Client (e2e): Jasmine + Protractor (Angular default)
* Server: Mocha/SuperTest/Should (Koa default)

See [/test/server/users.js](/test/server/users.js) for an example.

## Credits
Client side is entirely based on the official: [Angular Seed](https://github.com/angular/angular-seed). Server side simply utilizes generally accepted Koa middleware and Node.js best practices.

## The Name
The project name is an acronym for Koa, Angular, and Node. It also is the name for a Zen Buddhist riddle used to focus the mind during meditation and to develop intuitive thinking.
