# Toastify

![Built with JavaScript](https://img.shields.io/badge/Built%20with-JavaScript-red?style=for-the-badge&logo=javascript)

[![toastify-js](https://img.shields.io/badge/toastify--js-1.12.0-brightgreen.svg)](https://www.npmjs.com/package/toastify-js)
![MIT License](https://img.shields.io/npm/l/toastify-js)

Toastify is a lightweight, vanilla JS toast notification library.

## Demo

[Click here](https://apvarun.github.io/toastify-js/)

## Features

* Multiple stacked notifications
* Customizable
* No blocking of execution thread

### Customization options

* Notification Text
* Duration
* Toast background color
* Close icon display
* Display position
* Offset position

## Installation

#### Toastify now supports installation via NPM

* Run the below command to add toastify-js to your exisitng or new project.

```
npm install --save toastify-js
```

or

```
yarn add toastify-js -S
```

* Import toastify-js into your module to start using it.

```
import Toastify from 'toastify-js'
```

You can use the default CSS from Toastify as below and later override it or choose to write your own CSS.

```
import "toastify-js/src/toastify.css"
```

#### Adding ToastifyJs to HTML page using the traditional method

To start using **Toastify**, add the following CSS on to your page.

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/toastify-js/src/toastify.min.css">
```

And the script at the bottom of the page

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/toastify-js"></script>
```

> Files are delivered via the CDN service provided by [jsdeliver](https://www.jsdelivr.com/)

## Documentation

```javascript
Toastify({
  text: "This is a toast",
  duration: 3000,
  destination: "https://github.com/apvarun/toastify-js",
  newWindow: true,
  close: true,
  gravity: "top", // `top` or `bottom`
  position: "left", // `left`, `center` or `right`
  stopOnFocus: true, // Prevents dismissing of toast on hover
  style: {
    background: "linear-gradient(to right, #00b09b, #96c93d)",
  },
  onClick: function(){} // Callback after click
}).showToast();
```

> Toast messages will be centered on devices with screen width less than 360px.

* See the [changelog](https://github.com/apvarun/toastify-js/blob/master/CHANGELOG.md)

### Add own custom classes

If you want to use custom classes on the toast for customizing (like info or warning for example), you can do that as follows:

```javascript
Toastify({
  text: "This is a toast",
  className: "info",
  style: {
    background: "linear-gradient(to right, #00b09b, #96c93d)",
  }
}).showToast();
```

Multiple classes also can be assigned as a string, with spaces between class names.

### Add some offset

If you want to add offset to the toast, you can do that as follows:

```javascript
Toastify({
  text: "This is a toast with offset",
  offset: {
    x: 50, // horizontal axis - can be a number or a string indicating unity. eg: '2em'
    y: 10 // vertical axis - can be a number or a string indicating unity. eg: '2em'
  },
}).showToast();
```

Toast will be pushed 50px from right in x axis and 10px from top in y axis.

**Note:**

If `position` is equals to `left`, it will be pushed from left.
If `gravity` is equals to `bottom`, it will be pushed from bottom.

## API

| Option Key | type | Usage | Defaults |
|-----------------|----------------------|----------------------------------------------------------------------------|-------------|
| text | string | Message to be displayed in the toast | "Hi there!" |
| node | ELEMENT_NODE | Provide a node to be mounted inside the toast. `node` takes higher precedence over `text` |  |
| duration | number | Duration for which the toast should be displayed.<br>-1 for permanent toast | 3000 |
| selector | string \| ELEMENT_NODE | ShadowRoot | CSS Selector or Element Node on which the toast should be added | body |
| destination | URL string | URL to which the browser should be navigated on click of the toast |  |
| newWindow | boolean | Decides whether the `destination` should be opened in a new window or not | false |
| close | boolean | To show the close icon or not | false |
| gravity | "top" or "bottom" | To show the toast from top or bottom | "top" |
| position | "left" or "right" | To show the toast on left or right | "right" |
| backgroundColor | CSS background value | To be deprecated, use `style.background` option instead. Sets the background color of the toast |  |
| avatar | URL string | Image/icon to be shown before text |  |
| className | string | Ability to provide custom class name for further customization |  |
| stopOnFocus | boolean | To stop timer when hovered over the toast (Only if duration is set) | true |
| callback | Function | Invoked when the toast is dismissed |  |
| onClick | Function | Invoked when the toast is clicked |  |
| offset | Object | Ability to add some offset to axis | |
| escapeMarkup | boolean | Toggle the default behavior of escaping HTML markup | true |
| style | object | Use the HTML DOM Style properties to add any style directly to toast | |
| ariaLive | string | Announce the toast to screen readers, see https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions for options | "polite" |
| oldestFirst | boolean | Set the order in which toasts are stacked in page | true |

> Deprecated properties: `backgroundColor` -  use `style.background` option instead

## Browsers support

| ![][ie]<br />IE / Edge | ![][firefox]<br />Firefox | ![][chrome]<br />Chrome | ![][safari]<br />Safari | ![][opera]<br />Opera |
| ---------------------- | ------------------------- | ----------------------- | ----------------------- | --------------------- |
| IE10, IE11, Edge       | last 10 versions          | last 10 versions        | last 10 versions        | last 10 versions      |
