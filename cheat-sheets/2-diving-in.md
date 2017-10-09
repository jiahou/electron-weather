## Summary
This branch dives into how an app renders, makes minor adjustments to become more familiar with the Electron interface, and concludes with a major refactor of the process to show how easy it is to work with NPM.

## Instructions
#### Exercise One (Make it Functional)
**Step One**: On line 9 of index.html, add:
```js
 require('./index')
```
**Step Two**: Commit the change, and test your code by launching the app.
```sh
npm start
```

#### Exercise Two (Basic Manipulation)

**Step One**: On lines 51 and 52 of main.js, add these two lines of code, then save:
```js
  width: 300,
  height: 450,
```
**Step Two**: See the app in progress.
```sh
npm start
```
**Step Three**: While hovering over the app, type CMD + Option + I to open Google Dev Tools.

**Step Four**: Quit the process and return to main.js.

**Step Five**: Set line 56, resizable, to true, and save.
```js
resizable: true,
```
**Step Six**: Relaunch the app to test resizable windows.
```sh
npm start
```
**Step Seven**: Open Dev Tools again (CMD + Option + I) and find the error in the console tab.

**Step Eight**: Remove line 93 from index.js, which is causing the error in the console dialog, and save.
```js
REMOVE: sendNotification(weather)
```
**Step Nine**: Terminate and relaunch the app.
```sh
npm start
```
**Step Ten**: Open DevTools again to determine if the console error disappears.

#### Exercise Three (Major Refactor)
**Step One**: On line 11 of main.js, add the following code chunk:

```js
  var menubar = require('menubar')
  var mb = menubar()

  mb.on('ready', function ready () {
    console.log('app is ready')
    // your app code here
  })
```

**Step Two**: Comment out ALL remaining lines (18 - 95) of code on main.js

**Step Three**: Save. Then launch the app:
```sh
npm start
```
**Step Four**: Notice the Electron error pop-up.

**Step Five**: Return to package.json, and add a comma to the end of line 20.
```js
"electron": "^1.6.8",
```
**Step Six**: On line 21, paste the following:
```js
"menubar": "^5.2.3"
```
**Step Seven**: Install the new dependency and restart the app.
```sh
npm install
```
```sh
npm start
```

## Next Steps
**Step One**: Close any open files in your text editor to avoid conflicts on a branch change.

**Step Two**: Commit any unstaged changes.

**Step Three**:
```sh
git checkout packaging
```