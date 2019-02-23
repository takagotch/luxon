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



```


