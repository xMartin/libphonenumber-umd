# libphonenumber-umd
Google's libphonenumber packaged as UMD exposing the `i18n` namespace

See https://github.com/googlei18n/libphonenumber

## Usage
NodeJS module
```javascript
var libphonenumber = require('libphonenumber-umd');
```

or AMD
```javascript
require(['libphonenumber-umd'], function (libphonenumber) {
  ...
```

or

```html
<script src="libphonenumber-umd/libphonenumber"></script>
<script>
  var libphonenumber = window.i18n;
  ...
```

ex:
```javascript
function format (number) {
  var phoneUtil = libphonenumber.phonenumbers.PhoneNumberUtil.getInstance();
  number = phoneUtil.parseAndKeepRawInput(number, 'DE');
  return phoneUtil.format(number, libphonenumber.phonenumbers.PhoneNumberFormat.E164);
};

format('030 555-555'); // +4930555555
```
