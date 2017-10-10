# sparkline-list
A Polymer Element showing list of sparkline charts.

### Example
```js
demo.data = [{
  name: 'Chart 1',
  points: [{
    date: new Date(2017, 01, 02),
    count: 0
  }, {
    date: new Date(2017, 01, 09),
    count: 3
  }, {
    date: new Date(2017, 01, 16),
    count: 5
  }, {
    date: new Date(2017, 01, 23),
    count: 3
  }, {
    date: new Date(2017, 01, 30),
    count: 9
  }, {
    date: new Date(2017, 02, 06),
    count: 1
  }, {
    date: new Date(2017, 02, 13),
    count: 9
  }, {
    date: new Date(2017, 02, 20),
    count: 7
  }, {
    date: new Date(2017, 02, 27),
    count: 1
  }]
}, {
  name: 'Chart 2',
  points: [{
    date: new Date(2017, 01, 02),
    count: 0
  }, {
    date: new Date(2017, 01, 09),
    count: 6
  }, {
    date: new Date(2017, 01, 16),
    count: 2
  }, {
    date: new Date(2017, 01, 23),
    count: 1
  }, {
    date: new Date(2017, 01, 30),
    count: 5
  }, {
    date: new Date(2017, 02, 06),
    count: 7
  }, {
    date: new Date(2017, 02, 13),
    count: 2
  }, {
    date: new Date(2017, 02, 20),
    count: 8
  }, {
    date: new Date(2017, 02, 27),
    count: 3
  }]
}, {
  name: 'Chart 3',
  points: [{
    date: new Date(2017, 01, 02),
    count: 1
  }, {
    date: new Date(2017, 01, 09),
    count: 4
  }, {
    date: new Date(2017, 01, 16),
    count: 7
  }, {
    date: new Date(2017, 01, 23),
    count: 7
  }, {
    date: new Date(2017, 01, 30),
    count: 1
  }, {
    date: new Date(2017, 02, 06),
    count: 7
  }, {
    date: new Date(2017, 02, 13),
    count: 1
  }, {
    date: new Date(2017, 02, 20),
    count: 9
  }, {
    date: new Date(2017, 02, 27),
    count: 2
  }]
}, {
  name: 'Chart 4',
  points: [{
    date: new Date(2017, 02, 13),
    count: 1
  }, {
    date: new Date(2017, 02, 20),
    count: 9
  }, {
    date: new Date(2017, 02, 27),
    count: 2
  }]
}, {
  name: 'Chart 5',
  points: [{
    date: new Date(2017, 02, 13),
    count: 5
  }, {
    date: new Date(2017, 02, 20),
    count: 2
  }, {
    date: new Date(2017, 02, 27),
    count: 2
  }]
}, {
  name: 'Chart 6',
  points: [{
    date: new Date(2017, 02, 13),
    count: 4
  }, {
    date: new Date(2017, 02, 20),
    count: 6
  }, {
    date: new Date(2017, 02, 27),
    count: 2
  }]
}, {
  name: 'Chart 7',
  points: [{
    date: new Date(2017, 02, 13),
    count: 3
  }, {
    date: new Date(2017, 02, 20),
    count: 1
}, {
    date: new Date(2017, 02, 27),
    count: 9
  }]
}, {
  name: 'Chart 8',
  points: [{
    date: new Date(2017, 01, 30),
    count: 20
  }]
}];
```

```html
<sparkline-list data="[[data]]"></sparkline-list>
```

### Styling

`<sparkline-list>` provides the following custom properties and mixins for styling:

Custom property               | Description                            | Default
------------------------------|----------------------------------------|--------
`--sparkline-list-max-height` | The max height for the sparkline list. | 300px

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct
