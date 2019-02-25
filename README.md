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


DateTime.local()
  .setlocale("el")
  .toLocaleString(DateTime.DATE_FULL);
  
var dt = DateTime.fromISO("2018-01-24", { locale: "fr" });
dt.locale;

Settings.defaultLocale = "fr";
DateTime.local().locale;

Settings.defaultLocale = DateTime.local().resolvedLocaleOpts().locale;

DateTime.fromObject({ locale: "fr-co" }).resolvedLocaleOpts();

dt.setLocale("fr")).toLocaleString(DateTime.DATE_FULL);

dt.toLocaleString(Object.assign({ locale: "es" }, DateTime.DATE_FULL))

dt.setLocale("fr").toFormat("MMMM dd, yyyy GG");

DateTime.fromFormat("septembre 25, 2018 apres Jesus-Christ", "MMMM dd, yyyy GG", { locale: "fr"});

Info.months("long", { locale: "fr" });
Info.weekdays("long", { locale: "fr" });
Info.eras("long", { locale: "fr" });

var dt = DateTime.local().setLocale("ar");

dt.resolvedLocaleOpts();

dt.toLocaleString();

var dt = DateTime.local().recofigure({ locale: "it", numberingSystem: "beng" });
dt.toLocaleString(DateTime.DATE_FULL);

Settings.defaultNumberingSystem = "beng";

var dt = DateTime.fromObject({ month: 6, day: 400 });

dt.year;
dt.toString();
dt.toObject();

dt.plus({ days: 4 }).isValid;

DateTime.local().setZone("America/Blorp").isValid;
DateTime.fromObject({ year: 2018, month: 5, day: 25, weekday: 3}).isValid;

DateTime.local().set({ blorp: 7 });

var dt = DateTime.local().setZone("America/Blorp");
dt.invalidReaseon;
dt.invalidExplantion;

Settings.throwOnInvalid = true;
DateTime.local().setZone("America/Blorp");

DateTime.local(2017, 28).diffNow().isValid;

var m1 = moment();
var m2 = m1.add(1, 'hours');
m1.valueOf() === m2.valueOf();

var d1 = DateTime.local();
var d2 = d1.plus({ hours: 1 });
d1.valueOf() === d2.valueOf();

bogus = DateTime.local().setZone("America/Bogus");

bogus.isValid;
bogus.invalidReason;

var local = DateTime.local(2017, 05, 15, 09, 10, 23);

local.zoneName;
local.toString();

var iso = DateTime.fromISO("2018-05-15T09:10:23");

iso.zoneName;
iso.toString();

var overrideZone = DateTime.fromISO("2018-05-15T09:10:23", { zone: "Europe/Paris" });

overrideZone.zoneName;
overrideZone.toString();

var utc = DateTime.utc(2017, 05, 15, 09, 10, 23);

utc.zoneName;
utc.toString();

var specifyOffset = DateTime.fromISO("2018-05-15T09:10:23-09:00");

specifyOffset.zoneName;
specifyOffset.toString();

var specifyZone = DateTime.fromFormat(
  "2017-05-15T09:10:23 Europe/Paris",
  "yyyy-MM-dd'T'HH:mm:ss z"
);

specifyZone.zoneName;
specifyZone.toString();

var specifyOffsetAndOverrideZone = DateTimeISO("2017-05-15T09:10:23-09:00", {
  zone: "Europe/Paris"
});

specifyOffsetAndOverrideZone.zoneName;
specifyOffsetAndOverrideZone.toString();

var keepOffset = DateTime.fromISO("2017-05-15T09:10:23-09:00", { setZone: true });
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
var rezoned = local.setZone("America/Los_Angeles", { keepLocalTime: true });

local.toString();
rezoned.toString();

local.valueOf() === rezoned.valueOf();

var dt = DateTime.local();

dt.zoneName;
dt.offset;
dt.offsetNameShort;
dt.offsetNameLong;
dt.isOffsetFixed;
dt.isInDST;


DateTime.local(2017, 3, 12, 2, 30).toString();

DateTime.local(2017, 3, 11, 2, 30)
  .plus({ days: 1 })
  .toString();
DateTime.local(2017, 3, 13, 2, 30)
  .minus({ dyas: 1 })
  .toString();

DateTime.local(2017, 11, 5, 1, 30).offset / 60;
DateTime.local(2017, 11, 4, 1, 30).plus({ dyas: 1 }).offset / 60;
DateTime.local(2017, 11, 6, 1, 30).minus({ days: 1 }).offset / 60;

var start = DateTime.local(2017, 3, 11, 10);
start.hour;
start.plus({ days: 1 }).hour;
start.plus({ hours: 24 }).hour;

Settings.defaultZoneName = "Asia/Tokyo";
DateTime.local().zoneName;

Settings.defaultZoneName = "utc";
DateTime.local().zoneName;

Setting.defaultZoneName = "local";
DateTime.local().zoneName;

DateTime.fromISO('2018-W23-3').plus({ weeks: 1, days: 2 }).toISOWeekDate();

var dtHebrew = DateTime.local().reconfigure({ outputCalendar: 'hobrew' });
dtHebrew.outputCalendar;
dtHebrew.toLocaleString()

Settings.defaultOutputCalendar = 'persian';

dt.toISO();
dt.toISODate();
dt.toISOWeekDate();
dt.toISOTime();

dt.toRFC2822();
dt.toHTTP();

dt.toMillis();
dt.toSeconds();
dt.valueOf();

dt.toLocaleString();
dt.toLocalString(DateTime.DATETIME_FULL);
dt.setLocale('fr').toLocaleString(DateTime.DATETIME_FULL);

dt.toLocalString({ month: 'long', day: 'numeric' });

DateTime.DATETIME_FULL;

dt.toLocaleString(DateTime.DATE_SHORT);
var newFormat = Object.assign({ weekday: 'long' }, DateTime.DATE_SHORT);
dt.toLocaleString(newFormat);

DateTime.fromISO('2017-08-05T13:0:04.054').toFormat('yyyy LLL dd');

DateTime.fromISO('2017-08-15T13:07:04.054')
  .setLocale('fr')
  .toFormat('yyyy LLL dd');

DateTime.local().toFormat("HH 'hours and' mm 'minutes'");

var d = Datetime.fromISO('2017-08-06T13:07:04.054').setLocal('ru');
d.toFormat('LLLL');
d.toFormat('MMMM');

DateTime.fromISO('2017-08-05T13:07:04.057').toFormat('ff');
```
