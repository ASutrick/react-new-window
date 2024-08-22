## Original Repository

- **This project is a fork of [react-new-window](https://github.com/rmariuzzo/react-new-window) by rmariuzzo**

## This Fork

- **Removes `center` prop so window features (top, left, width, height) work as intended.**

## Features

- **Only 3.68KB** (gzipped!).
- **Support the full `window.open` api**.
- **Built for React 16 & React 18** (uses `ReactDOM.createPortal`).
- **Handler for blocked popups** (via `onBlock` prop).

## Installation

```sh
npm i @asutrick/react-new-window --save
```

## Usage

```js
import React from 'react'
import NewWindow from '@asutrick/react-new-window'

const Demo = () => (
  <NewWindow>
    <h1>Hi 👋</h1>
  </NewWindow>
)
```

When **`<NewWindow />`** is mounted a popup window will be opened. When unmounted then the popup will be closed.

The `children` contents is what will be rendered into the new popup window. In that case `Hi 👋` will be the content. The content can include any react-stateful code.

## Documentation

| Properties       | Type                  | Default     | Description                                                                                                                                                                                                         |
| ---------------- | --------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `url`            | `String`              | ` `         | The URL to open, if specified any `children` will be overriden ([more details on `url`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open)).                                                             |
| `name`           | `String`              | ` `         | The name of the window ([more details on `windowName`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open)).                                                                                              |
| `title`          | `String`              | ` `         | The title of the new window document.                                                                                                                                                                               |
| `features`       | `Object`              | `{}`        | The set of window features ([more details on `windowFeatures`](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)).                                                                      |
| `onUnload`       | `Function`            | `undefined` | A function to be triggered before the new window unload.                                                                                                                                                            |
| `onBlock`        | `Function`            | `undefined` | A function to be triggered when the new window could not be opened.                                                                                                                                                 |
| `onOpen`         | `Function(w: Window)` | `undefined` | A function to be triggered when window open by library.                                                                                                                                                                                                                                              
| `closeOnUnmount` | `Boolean`             | `true`      | If specified, close the new window on unmount.               