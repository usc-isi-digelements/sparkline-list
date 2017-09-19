# sparkline-list
A Polymer Element showing list of sparkline charts.

### Example
```js
var xProp = date;
var yProp = count;

var results = [
  {"createdDate": new Date(2017, 01, 02) , "value": 0, "group": "chart 1"},
  {"createdDate": new Date(2017, 01, 09) , "value": 3, "group": "chart 1"},
  {"createdDate": new Date(2017, 01, 16) , "value": 5, "group": "chart 1"},
  {"createdDate": new Date(2017, 01, 23) , "value": 3, "group": "chart 1"},
  {"createdDate": new Date(2017, 01, 30) , "value": 9, "group": "chart 1"},
  {"createdDate": new Date(2017, 02, 06) , "value": 1, "group": "chart 1"},
  {"createdDate": new Date(2017, 02, 13) , "value": 9, "group": "chart 1"},
  {"createdDate": new Date(2017, 02, 20) , "value": 7, "group": "chart 1"},
  {"createdDate": new Date(2017, 02, 27) , "value": 1, "group": "chart 1"},
  {"createdDate": new Date(2017, 01, 02) , "value": 0, "group": "chart 2"},
  {"createdDate": new Date(2017, 01, 09) , "value": 6, "group": "chart 2"},
  {"createdDate": new Date(2017, 01, 16) , "value": 2, "group": "chart 2"},
  {"createdDate": new Date(2017, 01, 23) , "value": 1, "group": "chart 2"},
  {"createdDate": new Date(2017, 01, 30) , "value": 5, "group": "chart 2"},
  {"createdDate": new Date(2017, 02, 06) , "value": 7, "group": "chart 2"},
  {"createdDate": new Date(2017, 02, 13) , "value": 2, "group": "chart 2"},
  {"createdDate": new Date(2017, 02, 20) , "value": 8, "group": "chart 2"},
  {"createdDate": new Date(2017, 02, 27) , "value": 3, "group": "chart 2"},
  {"createdDate": new Date(2017, 01, 02) , "value": 1, "group": "chart 3"},
  {"createdDate": new Date(2017, 01, 09) , "value": 4, "group": "chart 3"},
  {"createdDate": new Date(2017, 01, 16) , "value": 7, "group": "chart 3"},
  {"createdDate": new Date(2017, 01, 23) , "value": 7, "group": "chart 3"},
  {"createdDate": new Date(2017, 01, 30) , "value": 1, "group": "chart 3"},
  {"createdDate": new Date(2017, 02, 06) , "value": 7, "group": "chart 3"},
  {"createdDate": new Date(2017, 02, 13) , "value": 1, "group": "chart 3"},
  {"createdDate": new Date(2017, 02, 20) , "value": 9, "group": "chart 3"},
  {"createdDate": new Date(2017, 02, 27) , "value": 2, "group": "chart 3"},
  {"createdDate": new Date(2017, 02, 13) , "value": 1, "group": "chart 4"},
  {"createdDate": new Date(2017, 02, 20) , "value": 9, "group": "chart 4"},
  {"createdDate": new Date(2017, 02, 27) , "value": 2, "group": "chart 4"},
  {"createdDate": new Date(2017, 02, 13) , "value": 5, "group": "chart 5"},
  {"createdDate": new Date(2017, 02, 20) , "value": 2, "group": "chart 5"},
  {"createdDate": new Date(2017, 02, 27) , "value": 2, "group": "chart 5"},
  {"createdDate": new Date(2017, 02, 13) , "value": 4, "group": "chart 6"},
  {"createdDate": new Date(2017, 02, 20) , "value": 6, "group": "chart 6"},
  {"createdDate": new Date(2017, 02, 27) , "value": 2, "group": "chart 6"},
  {"createdDate": new Date(2017, 02, 13) , "value": 3, "group": "chart 7"},
  {"createdDate": new Date(2017, 02, 20) , "value": 1, "group": "chart 7"},
  {"createdDate": new Date(2017, 02, 27) , "value": 9, "group": "chart 7"}
];

convertHistograms = function(points) {
  var pointGroupObj = {};
  var pointGroupArray = [];

  points.map(function(point) {
    if(!pointGroupObj[point.group]) {
      pointGroupObj[point.group] = [];
    }
    var newPt = {};
    newPt[xProp] = point.createdDate;
    newPt[yProp] = point.value;
    pointGroupObj[point.group].push(newPt);
  });

  for (key in pointGroupObj) {
    pointGroupArray.push({
      "pointArray": pointGroupObj[key],
      "key": key
    });
  }
  return pointGroupArray;
};
```

```html
<sparkline-list
  results="[[testPoints]]"
  convert-function="[[convertHistograms]]"
  x-prop="[[xProp]]"
  y-prop="[[yProp]]"
  chart-widths="500px"
  chart-heights="30px"
  max-overall-height="150px">
</sparkline-list>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct