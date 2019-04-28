# v-tilterino
Vue Directive tilting the element on hover events and depending on device orientation (if on mobile).

The directive is built around [Vanilla-tilt.js](https://micku7zu.github.io/vanilla-tilt.js/)

## Usage

You can install the directive with `npm` via `npm install v-tilterino`

Use it in Vue

```
// main.js

import Tilterino from 'v-tilterino'

...

Vue.use(Tilterino, installOptions)

...
```

Use the `v-tilt` directive in any HTMLElement or component

```
// MyComponent.js

<template>
  ...
  <MyComponent v-tilt>
  ...
  </MyComponent>
  
  <div v-tilt>
  ...
  </div>
</template>
```

Options can be passed as installOptions when registering the plugin or directly on the element carrying the directive,
prepended with `data-tilt-`; e.g.:

```
<div v-tilt data-tilt-{option}={value}>
...
</div>

<div v-tilt data-tilt-reverse="true">
...
</div>
```

All installOptions with defaults are:

```
{
  reverse: false,
  max: 5,
  perspective: 1000,
  easing: "cubic-bezier(.03,.98,.52,.99)",
  scale: 1,
  speed: 300,
  transition: true,
  axis: null,
  "mouse-event-element": null,
  reset: true,
  gyroscope: true,
  gyroscopeMinAngleX: -25,
  gyroscopeMaxAngleX: 25,
  gyroscopeMinAngleY: -25,
  gyroscopeMaxAngleY: 25
}
```

On how to use these options I refer to [Vanilla-tilt.js](https://micku7zu.github.io/vanilla-tilt.js/)
