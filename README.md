# karma-sauce-example

> An example of using the [Karma](http://karma-runner.github.io/0.12/index.html) test runner with [Sauce Labs](https://saucelabs.com)' browser cloud to run JavaScript unit tests.

![sauce-labs-loves-karma](images/sauce-loves-karma.png)

## Getting Started

To get started, clone the repo:

```bash
git clone https://github.com/saucelabs/karma-sauce-example.git && cd karma-sauce-example
```

Then run the following command to install the local node dependencies and the Karma command line interface globally:

```bash
npm install && npm install -g karma-cli
```

*Note: make sure you have [node.js](http://nodejs.org/) installed before running the above command.* 

## Running Karma locally

You then can run Karma locally to see how it works with the `karma start` command. Try saving a source file in the `src` folder or a test file in the `test` folder to see Karma automatically re-run the test files on the latest source code. 

By default, this example runs tests in Chrome and Firefox on your local machine, and you can add more browsers that you have installed in the `karma.conf.js`'s `browsers` array.

## Running Karma with the [karma-sauce-launcher](https://github.com/karma-runner/karma-sauce-launcher) plugin

To use Karma with Sauce, create a `sauce.json` file with your Sauce Labs username and access key (if you don't have an account, you can sign up [here](https://saucelabs.com/signup/plan/free)). You can reference the `sampleSauce.json` in the repo to see the format. The provided `karma.conf-ci.js` file reads the `sauce.json` file and gets your private sauce credentials, so `sauce.json` is ignored in the git repo.

### Using the karma-sauce-launcher in CI

It is cool to run Sauce locally while you develop, but even cooler to run in a Continuous Integration system on every commit to your codebase. To integrate your CI system with Sauce check out the instructions for [Travis](http://saucelabs.com/opensource/travis), [Jenkins](http://saucelabs.com/jenkins), or [Bamboo](http://saucelabs.com/bamboo).

The provided `karma.conf-ci.js` file already is set up to read environment variables on CI, so you shouldn't need to modify it to run Sauce with your CI system as long as the `process.env.SAUCE_USERNAME` and `process.env.SAUCE_ACCESS_KEY` are set properly.
