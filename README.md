[![Build Status](https://travis-ci.org/RedTurtle/plone-less-base.svg?branch=master)](https://travis-ci.org/RedTurtle/plone-less-base)

# plone-less-base

Base less styles for Plone 5 theming

## Use case

We use these styles while bootstrapping a new theme with [plonecli](https://pypi.python.org/pypi/plonecli), in order to have basic plone styles ready and save some time on development.

## Usage

In order to use this correctly, you will need to tell your less compiler to also read files from the `node_modules` folder.

* If you use it through the less cli, by adding the `--include-path=node_modules` argument
* If you configure it with a js object, add the `paths` property, which will look like this: `paths: ['node_modules']`

This is needed because the styles inside this package read other styles from its `bootstrap` dependency, and it will also make it smoother for you to use these styles.

Documentation: http://lesscss.org/usage/#less-options-cross-platform-options.

In order to add these styles to your theme styles, import it like this:

```less
@import 'plone-less-base/styles.less';
```

## Modular import

If you don't need all of the styles provided here, you can cherry-pick the partials you need by making a copy of the [main stylesheet of this package (styles.less)](https://github.com/RedTurtle/plone-less-base/blob/master/styles.less) and commenting the partials you don't need.

## Bonus

As an extra that may be helpful, in the `lib` folder of the package you download from npm, there is a compiled css stylesheet with all of the styles included in this repo.

## Installation

```sh
npm install --save plone-less-base
```

## Compatibility

These styles are developed for Plone 5.x sites.

## License

MIT
