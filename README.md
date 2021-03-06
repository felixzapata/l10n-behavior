# l10n-behavior

[![Build Status](https://travis-ci.org/felixzapata/l10n-behavior.png)](https://travis-ci.org/felixzapata/l10n-behavior)

[![Coverage Status](https://coveralls.io/repos/github/felixzapata/l10n-behavior/badge.svg?branch=master)](https://coveralls.io/github/felixzapata/l10n-behavior?branch=master)

Polymer.l10nBehavior provides a normalized interface to localize strings.

Based on the [ECMAScript Internationalization API Specification](http://ecma-international.org/ecma-402/1.0/)

More information about [Intl in the Mozilla Developer Network site](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Intl).


## Usage

1) Add Polymer.l10nBehavior to the behaviors list in the JS file or script of your component:

```js
behaviors: [Polymer.l10nBehavior]
```

2) Import the behavior in your HTML:

```html
<link rel="import" href="../l10n-behavior/l10n-behavior.html">
```

To locate a value, just do the following:
```html
{{locale('value', lang)}}
```

You can override in your component the options to set to the localize function. These options are based on the ECMAScript Internationalization API Specfication. 

### Example

```html
  <template>
    <p>{{localize(12, 'en')}}</p>
  </template>
  ...
  Polymer({
    is: 'my-element',
    properties:{
      optionsL10n:{
        value: function(){
          return { style: 'currency', currency: 'USD' };
        }
      }
    },
    behaviors: [
      Polymer.l10nBehavior
    ]

  });
  ...
```



