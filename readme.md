# max-control

> Control the ELV Max! heating system with node.js

## Usage

```
var MaxCube = require('./index');
var mc = new MaxCube('192.168.1.110', 62910);

mc.on('connected', function () {
  console.log('ready');

  setTimeout(function () {
    console.log('send');
    mc.setTemperature('0087ae', 'manual', 19);
  }, 5000);
});

mc.on('update', function (data) {
  console.log('got update');
  console.log(data);
});
```
