# eslint-import-resolver-babel-plugin-root-import

This project fork from [olalonde/eslint-import-resolver-babel-root-import](https://github.com/olalonde/eslint-import-resolver-babel-root-import).

A [babel-plugin-root-import](https://github.com/entwicklerstube/babel-plugin-root-import) resolver for [eslint-plugin-import](https://github.com/benmosher/eslint-plugin-import).

## ⚠️ Warning

This project has been transferred to [eslint-import-resolver-babel-plugin-root-import](https://github.com/unconfident/eslint-import-resolver-babel-plugin-root-import).

See [issues#14](https://github.com/olalonde/eslint-import-resolver-babel-root-import/issues/14) for details.

## Installation

```sh
npm install --save-dev eslint-plugin-import eslint-import-resolver-babel-plugin-root-import
```

## Usage

Inside your `.eslintrc` file, pass this resolver to `eslint-plugin-import`:
```
"settings": {
  "import/resolver": "babel-plugin-root-import"
}
```

And your `.babelrc` file look like this:

```json
{
    "presets": ["latest", "react", "stage-0"],
    "plugins": [
        "transform-runtime",
        [
            "babel-plugin-root-import", [{
                "rootPathPrefix": "~",
                "rootPathSuffix": "app/components"
            }, {
                "rootPathPrefix": "$",
                "rootPathSuffix": "app"
            }, {
                "rootPathPrefix": "#",
                "rootPathSuffix": "lib"
            }]
        ]
    ]
}
```

## License

MIT, see [LICENSE.md](/LICENSE.md) for details.


[babel-plugin-root-import]: https://github.com/entwicklerstube/babel-plugin-root-import
