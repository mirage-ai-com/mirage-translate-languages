# Mirage Translate Languages

[![Build Status](https://github.com/mirage-ai-com/mirage-translate-languages/actions/workflows/action.yml/badge.svg)](https://github.com/mirage-ai-com/mirage-translate-languages/actions) [![NPM](https://img.shields.io/npm/v/mirage-translate-languages.svg)](https://www.npmjs.com/package/mirage-translate-languages) [![Downloads](https://img.shields.io/npm/dt/mirage-translate-languages.svg)](https://www.npmjs.com/package/mirage-translate-languages)

🔤 Maps the languages currently supported by the Mirage Translate API endpoint. The data **auto-updates every 3 days**, if needed.

Copyright 2023 Crisp IM SAS. See LICENSE for copying information.

**😘 Maintainer**: [@eliottvincent](https://github.com/eliottvincent)

## Usage

```js
const { isLanguageSupported } = require("mirage-translate-languages");

console.log(isLanguageSupported("en"));
// true
```


## API

### Access to supported languages

The raw set of supported languages, as returned by the Mirage Translate API, is made accessible:

```js
const { languages } = require("mirage-translate-languages");

console.log(languages);
// {af: {…}, am: {…}, ar: {…}, as: {…}, az: {…}, …}

// OR
const mirageTranslate = require("mirage-translate-languages");

console.log(mirageTranslate.dataLanguages);
// {af: {…}, am: {…}, ar: {…}, as: {…}, az: {…}, …}
```

### Check if a language is supported
`isLanguageSupported(code)` returns whether a language is supported or not:
* `code` must be a BCP 47 language tag, as per [ISO 3166-1](https://en.wikipedia.org/wiki/ISO_3166-1)

```js
const { isLanguageSupported } = require("mirage-translate-languages");

console.log(isLanguageSupported("en"));
// true
```
