# NFT Marketplace for Beginner

Youtube Link(<https://www.youtube.com/watch?v=2bjVWclBD_s>)

## Hardhat

```
npx hardhat node
```

```
## Deploy
npx hardhat run src/backend/scripts/deploy.js --network localhost

## Debug
npx hardhat console --network localhost
const contract = await ethers.getContractAt("CONTRACT NAME", "CONTRACT ADDRESS")
const tokenCount = await contract.tokenCount()
const name = await contract.name()
const symbol = await contract.symbol()

## Test
npx hardhat test
```

### Hardhat Network

![image](https://user-images.githubusercontent.com/48934522/168472901-2b68aba6-9227-4d38-88c2-4db3f64c6bcc.png)

![image](https://user-images.githubusercontent.com/48934522/168472958-4f198c09-f58f-4a45-a22b-f18a38c0a91d.png)

<!--

## Introduction

The `readme-to-test` libary allows to easily validate code examples defined in the README file.

It finds all JavaScript blocks of code defined in target project's README file and converts them to unit tests.
Tests are run with Mocha and can be easily integrated with the build process (and Git's pre-commit hook).

## Installation

`npm install readme-to-test --save-dev`

## Command line

The validation can be triggered by executing the following command in the target project's main directory:

```
node ./node_modules/.bin/readme-to-test
```

The README file is automatically located. The validator creates a temporary directory (`.tmp` by default) and creates a separate self-contained unit test file for each block of JavaScript code found in the README. Then all the generated tests are run with Mocha. The directory is only deleted after a successful validation.

## Integrating with the build

The validate-readme-examples script can supplement the existing tests:

```
{
  "name": "library",
  "version": "1.0.0",
  "main": "main-script.js",
  "scripts": {
    "validate-readme-examples": "readme-to-test",
    "test": "mocha unit/tests/ && npm run validate-readme-examples"
  }
}
```

## Examples

#### With console.log

The following block of code:

``` js
import library from 'library';

const result = library.someFunction();

console.log(result);
// prints 'result from some function';
```

will be converted into a unit test:

``` js
import assert from 'assert';
import library from './main-script.js';

it('Converts prints statement following console.log to assertion', () => {

    const result = library.someFunction();

    console.log(result);
    assert.deepEqual(result, 'result from some function');
}
```

#### No console output

``` js
var library = require('library');
// library.version === '1.0'
```

``` js
var assert = require('assert');

it('Converts equality statement to assertion', () => {

    var library = require('library');
    assert.deepEqual(library.version, '1.0');
}
```
-->