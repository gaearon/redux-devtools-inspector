# redux-devtools-inspector

Another Redux state monitor for [Redux DevTools](https://github.com/gaearon/redux-devtools)

The intention for this monitor is to provide a convinient way to inspect "real world" app states, that could be complicated and deeply nested.

![](2016-02-23.at.16.16.png)

### Installation

```
npm install --save-dev redux-devtools-inspector
```

### Usage

You can use `Inspector` as the only monitor in your app:

##### `containers/DevTools.js`

```js
import React from 'react';
import { createDevTools } from 'redux-devtools';
import Inspector from 'redux-devtools-inspector';

export default createDevTools(
  <Inspector />
);
```

Then you can render `<DevTools>` to any place inside app or even into a separate popup window.

Alternative, you can use it together with [`DockMonitor`](https://github.com/gaearon/redux-devtools-dock-monitor) to make it dockable.  
Consult the [`DockMonitor` README](https://github.com/gaearon/redux-devtools-dock-monitor) for details of this approach.

[Read how to start using Redux DevTools.](https://github.com/gaearon/redux-devtools)

### Features

Inspector has a list of actions and a preview panel, which shows a state after selected action and a diff with previous state. If no actions selected, the last state is shown.

### Props

Name                  | Description
-------------         | -------------
`theme`               | An object, containing classnames or style objects, that are used to style `Inspector` (similar to [react-themeable](https://github.com/markdalgleish/react-themeable)).

### License

MIT
