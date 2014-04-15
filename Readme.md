*This repository is a mirror of the [component](http://component.io) module [gjohnson/pluck](http://github.com/gjohnson/pluck). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/gjohnson-pluck`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
 [![Build Status](https://secure.travis-ci.org/gjohnson/pluck.png?branch=master)](http://travis-ci.org/gjohnson/pluck)

# pluck

  pluck property path from arrays or an object.

## Installation

*component*

```sh
  $ component install gjohnson/pluck
```

or

*npm*

```sh
  $ npm install pluck
```

## Example

Pluck from arrays.

```javascript
var pluck = require('pluck');

var firstName = pluck('name.first');

var items = [
  { name: { first: 'john', last: 'doe' } }
];

var names = firstName(items);
```

Pluck from plain objects.

```javascript
var pluck = require('pluck');

var firstName = pluck('name.first');

var item = {
  name: {
    first: 'john',
    last: 'doe'
  }
};

var name = firstName(item);
```

Pluck using index expressions.

```javascript
var pluck = require('pluck');

var firstName = pluck('name[1].first');
var item = {
  name: [
    {},
    {
      first: 'john',
      last: 'doe'
    }
  ]
};

var name = firstName(item);
```

## License

MIT
