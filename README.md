# ⚒ Drupal JS Build

Command line to build JS files the way Drupal core does.

Just create your JS files as [name].es6.js. When this tool is executed, those files will be compiled by Babel to [name].js.

The script files were directly taken from Drupal core codebase without any modification so it will be easy to update them whenever necessary.

## Overview

Install it:

```
npm i drupal-js-build --save-dev
```

or globally:

```
npm i -g drupal-js-build
```

To build the files:

```
npx drupal-js-build
```

To watch the files:

```
npx drupal-js-build watch
```

### Bonus
This tool can also compile SASS files using `node-sass`. 

The recommended folder structure is `./css/sass/[file].scss`. The files will be compiled to parent folder as `./css/[file].css`

To compile js and scss files:

```
npx drupal-js-build --css
```

or

```
npx drupal-js-build watch --css
```

To compile scss files only:

```
npx drupal-js-build --only-css
```

or

```
npx drupal-js-build watch --only-css
```

### Ignoring files/folders.

Files may be ignored by creating a local `.drupalbuild.js` file in the working
 directory running the script.
 
 The file should export an array of glob patterns. e.g.
 ```javascript
module.exports = [
  // Don't include the local ignore-me folder.
  './ignore-me/**'
];
```
