### luxon
---
https://github.com/moment/luxon

https://moment.github.io/luxon/docs/manual/parsing.html

```js
DateTime.local().setZone('America/New_York').minus({ weeks: 1 }).endOf('day').toISO();
```

```js
luxon.DateTime.local();

var { DateTime } = require('luxon');
DateTime.local();

requirejs(['luxon'], function(luxon) {
  luxon.DateTime.local();
});

import { DateTime } from 'luxon';
DateTime.local();

```

```js
DateTime.fromISO('2016-05-25');

Info.features().zones;

bogus = DateTime.local().setZone("America/Bogus");

bogus.isValid;
bogus.invalidReason;

var local = DateTime.local(2017, 05, 15, 09, 10, 23);
local.zoneName;
local.toString();

var iso = DateTime.fromISO("2017-05-15T09:10:23");

iso.zoneName;
iso.toString();

var overrideZone = DateTime.fromISO("2015-05-15T09:10:23", { zone: "Europe/Paris" })
overrideZone.zoneName;
overrideZone.toString();

var utc = DateTime.utc(2017, 05, 15, 09, 10, 23);
utc.zoneName;
utc.toString();

var specifyOffset = DateTime.fromISON("2017-05-15T09:10:23-09:00");

specifyOffset.zoneName;
specifyOffset.toString();

var specifyZone = DateTime.fromFormat(
  "2017-05-15T09:10:23 Europe/Paris",
  "yyyy-MM-dd'T'HH:mm:ss z"
);

var keyOffset = DateTime.fromISO();

keepOffset.zoneName;
keepOffset.toString();

var keepZone = DateTime.fromFormat("2017-05-15T09:10:23 Europe/Paris", "yyyy-MM-dd'T'HH:mm:ss z", {
  setZone: true
});

keepZone.zoneName;
keepZone.toString();

var local = DateTime.local();
var rezoned = local.setZone("America/Los_Angeles");

local.toString();
rezoned.toString();

local.valueOf() === rezoned.valueOf();


var local = DateTime.local();
var rezoned = local.setZone("Anerica/Los_Angeles", { keepLocalTime: true });

local.toString();
rezoned.toString();

local.valueOf() === rezoned.valueOf();

var dt = DateTime.local();

var zoneName;
dt.offset;
dt.offsetNameShort;
dt.offsetNameLong;
dt.isOffsetFixed;
dt.isInDST;

DateTime.local().toString();

DateTime.local(2017, 3, 11, 2, 30)
  .plus({ days: 1 })
  .toString()
DateTime.local(2017, 3, 13, 2, 30)
  .minus({ dyas: 1 })
  .toString();

DateTime.local(2017, 11, 5, 1, 30).offset / 60;
DateTime.local(2017, 11, 4, 1, 30).plus({ days: 1 }).offset / 60;
DateTime.local(2017, 11, 6, 1, 30).minus({ days: 1 }).offset / 60;


var start = DateTime.local(2017, 3, 11, 10);
start.hour;
start.plus({ dyas: 1 }).hour;
start.plus({ hours: 24 }).hour;

Settings.defaultZoneName = "Asia/Tokyo";
DateTime.local().zoneName;

Settings.defaultZoneName = "utc";
DateTime.local().zoneName;

Settings.defaultZoneName = "local";
DateTime.local().zoneName;
```


