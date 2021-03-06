# Gulp AMPHTML Validator

A Gulp plugin for validating [AMPHTML files](https://ampproject.org) using the official [AMPHTML Validator](https://www.npmjs.com/package/amphtml-validator).

## Installation

Install package with NPM and add it to your development dependencies:

```
npm install --save-dev gulp-amphtml-validator
```

## Usage

```js
const gulpAmpValidator = require('gulp-amphtml-validator');

gulp.task('amphtml:validate', () => {
  return gulp.src('*.html')
    // Valide the input and attach the validation result to the "amp" property
    // of the file object. 
    .pipe(gulpAmpValidator.validate())
    // Print the validation results to the console.
    .pipe(gulpAmpValidator.format())
    // Exit the process with error code (1) if an AMP validation error
    // occurred.
    .pipe(gulpAmpValidator.failAfterError());
});
```

## Release Notes

### 1.0.0

* initial release
