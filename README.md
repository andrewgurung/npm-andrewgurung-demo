## Creating and publishing npm module

1. Create index.js file
2. Create package.json file using `npm init`
Sample package.json file:
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
