# email-validation

[![Linux Build][ci-image]][ci-url]
<!-- to be used when/if numbers are respectable[![NPM Version][npm-image]][npm-url] [![NPM Downloads][downloads-image]][downloads-url]-->

package to perform validation on email addresses.

### Installation

```bash
npm install email-validation
```
### Usage

##### Single email validation with `validate()`

simply pass the `validate` function an email string.

```javascript
const email = require('email-validation');

const result = email.validate('föo@domain.com');
console.log(result) // output: true
```

The `validate` function will return a boolean result.

valid email format = true

invalid email format = false

```javascript
const result = email.validate('@domain.com');
console.log(result) // output: false
```

##### Bulk validation with `validateAll()`

perform bulk validation on an array of emails.
The `validateAll` function will return an object containing two arrays, valid and invalid.

```javascript
const emailArr = ['föo@domain.com', '@domain.com'];

const result = email.validateAll(emailArr);
console.log(result);
```
output:

```
{
  valid: [ 'föo@domain.com' ],
  invalid: [ '@domain.com' ]
}
```

### Tests

```javascript
npm run test
```



[ci-image]: https://img.shields.io/github/workflow/status/markogrady1/email-valid/nodejs/master.svg?label=build
[ci-url]: https://github.com/markogrady1/queues/actions?query=workflow%3Anodejs
[npm-image]: https://img.shields.io/npm/v/node-resque-data.svg
[npm-url]: https://npmjs.org/package/email-valid
[downloads-image]: https://img.shields.io/npm/dm/node-resque-data.svg
[downloads-url]: https://npmcharts.com/compare/node-resque-data?minimal=true