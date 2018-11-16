This repository was originally forked from [https://github.com/igorprado/favicon-notification](https://github.com/igorprado/favicon-notification).

# Favicon Notification
#### A small script (~ 1.4kB minified) to add notification bubble to favicon

## Favicon

If you don't have a nice favicon set on app, read this: [https://github.com/audreyr/favicon-cheat-sheet](https://github.com/audreyr/favicon-cheat-sheet)

## Installing

### NPM:

Run:

```
npm install favicon-notification
```

## Using

### NPM

```js
let FaviconNotification = require('favicon-notification');

// When your app loads
FaviconNotification.init({
  color: '#000000'
});

// On some event
FaviconNotification.add();

// If you want to remove the notification
FaviconNotification.remove();

```

### AMD

If you are using RequireJS, for example, load normally (remeber to set the alias in your RequireJS config):

```js
define(['FaviconNotification'], function(FaviconNotification){
  // When your app loads
  FaviconNotification.init({
    color: '#000000'
  });

  // On some event
  FaviconNotification.add();

  // If you want to remove the notification
  FaviconNotification.remove();
});
```

## Methods

## .init(options)

This script assumes that you have a `/favicon.ico` set. [See how setup your favicon](https://github.com/audreyr/favicon-cheat-sheet). If are you using another path to your favicon, you can set it by passing some options to this method. You can set a different fill and line color too (defaults are fill red and white line).

```js
FaviconNotification.init({
  url: '/path/to/favicon.ico',
  color: '#FFFFFF',
  lineColor: '#000000'
});
```

## .add()

As the name says, this add the notification bubble to the favicon. If you didn't initialized the script using `.init(options)`, this will use the default options to create and set the new favicon with the notification.

```js
FaviconNotification.add();
```
## .remove()

```js
FaviconNotification.remove();
```
