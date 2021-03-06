---
type: docs
order: 25
title: "FileInput"
permalink: docs/file-input/
alias: docs/fileinput/

---

`FileInput` is the most barebones UI for selecting files — it shows a single button that, when clicked, opens up the browser's file selector.

```js
const FileInput = require('@uppy/file-input')

uppy.use(FileInput, {
  // Options
})
```

[Try it live](/examples/xhrupload) - The XHRUpload example uses a `FileInput`.

## Installation

This plugin is published as the `@uppy/file-input` package.

Install from NPM:

```shell
npm install @uppy/file-input
```

## Options

The FileInput plugin has the following configurable options:

```js
uppy.use(FileInput, {
  target: null,
  pretty: true,
  inputName: 'files[]',
  locale: {
  }
})
```

> Note that certain [restrictions set in Uppy’s main options](/docs/uppy#restrictions), namely `maxNumberOfFiles` and `allowedFileTypes`, affect the system file picker dialog. If `maxNumberOfFiles: 1`, users will only be able to select one file, and `allowedFileTypes: ['video/*', '.gif']` means only videos or gifs (files with `.gif` extension) will be selectable.

### `id: 'FileInput'`

A unique identifier for this FileInput. It defaults to `'FileInput'`. Use this if you need to add multiple FileInput instances.

### `target: null`

DOM element, CSS selector, or plugin to mount the file input into.

### `pretty: true`

When true, display a styled button (see [example](/examples/xhrupload)) that, when clicked, opens the file selector UI. When false, a plain old browser `<input type="file">` element is shown.

### `inputName: 'files[]'`

The `name` attribute for the `<input type="file">` element.

### `locale: {}`

When `pretty` is set, specify a custom label for the button.

```js
strings: {
  chooseFiles: 'Choose files'
}
```
