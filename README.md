## Creating and publishing npm module

1. Create index.js file
  ````js
  exports.printMsg = function() {
    console.log( "This message is from npm-andrewgurung-demo pkg" );
  };
````

2. Create package.json file using `npm init`
  - The two required fields are `name` and `version`
  ```js
  {
    "name": "npm-andrewgurung-demo",
    "version": "1.0.0",
    "description": "A demo package by Andrew Gurung",
    "main": "index.js",
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    "repository": {
      "type": "git",
      "url": "https://github.com/andrewgurung/npm-andrewgurung-demo.git"
    },
    "keywords": [
      "demo",
      "andrewgurung",
      "andrew",
      "gurung"
    ],
    "author": "Andrew Gurung (http://andrewgurung.github.io)",
    "license": "ISC",
    "bugs": {
      "url": "https://github.com/andrewgurung/npm-andrewgurung-demo/issues"
    },
    "homepage": "https://github.com/andrewgurung/npm-andrewgurung-demo#readme"
  }
  ```

3. Publish npm package
  - Any file bundled with `package.json` can be published as a npm module
  - Add a npm user `npm adduser`
  - Verify user `npm config ls`
  - Publish your npm module `npm publish`

  ```shell
  $ npm adduser
  Username: andrewgurung
  Password:
  Email: (this IS public) andrewgurung@gmail.com

  $ npm config ls

  $ npm publish
  ```

4. Using your new npm package
  - Make a new directory. `mkdir consumer`
  - Install the new npm package. `npm install npm-andrewgurung-demo`
  - Create a test.js file
    ```js
    var npmAndrew = require('npm-andrewgurung-demo');
    npmAndrew.printMsg();
    ```
  - Run test.js from node
    ```js
    $ node test.js
    This message is from npm-andrewgurung-demo pkg
    ```

    Command:
    ```shell
    $ mkdir consumer
    $ cd consumer/
    $ npm install npm-andrewgurung-demo
    $ node test.js
    ```
