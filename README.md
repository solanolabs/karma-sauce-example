# karma-sauce-example

> An example of using the Karma test runner with Sauce Labs.

To get started, clone the repo and run `npm install` (make sure you have [node.js](http://nodejs.org/) installed). You then can run karma locally to see how it works with `karma start`. Try saving a source file in the `src` folder or a test file in the `test` folder to see karma automatically re-run your tests. 

By default, this example runs tests in Chrome and Firefox on your local machine, and you can add more browsers that you have installed in the `karma.conf.js` `browsers` array.

### Karma and Sauce

To use karma with Sauce, create a `sauce.json` file with your Sauce Labs username and access key (if you don't have an account, you can sign up [here](https://saucelabs.com/signup/plan/free)). You can reference the `sampleSauce.json` in the repo to see the format.

### Karma and Sauce on CI

It is cool to run Sauce locally while you develop, but even cooler to run with a Continuous Integration system on every commit to your codebase. To
