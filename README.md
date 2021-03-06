#### In progress...

#### An ESLint [Shareable Config](http://eslint.org/docs/developer-guide/shareable-configs)

#### Possible Errors

- [x] [for-direction](https://eslint.org/docs/rules/for-direction) <kbd>error</kbd>
- [x] [getter-return](https://eslint.org/docs/rules/getter-return) <kbd>error</kbd>
- [x] [no-await-in-loop](https://eslint.org/docs/rules/no-await-in-loop) <kbd>error</kbd>
- [x] [no-compare-neg-zero](https://eslint.org/docs/rules/no-compare-neg-zero) <kbd>error</kbd>
- [x] [no-cond-assign](https://eslint.org/docs/rules/no-cond-assign) <kbd>error</kbd>
- [x] [no-console](https://eslint.org/docs/rules/no-console) <kbd>warn</kbd>
- [x] [no-constant-condition](https://eslint.org/docs/rules/no-constant-condition) <kbd>off</kbd>
- [x] [no-control-regex](https://eslint.org/docs/rules/no-control-regex) <kbd>error</kbd>
- [x] [no-debugger](https://eslint.org/docs/rules/no-debugger) <kbd>error</kbd>
- [x] [no-dupe-args](https://eslint.org/docs/rules/no-dupe-args) <kbd>error</kbd>
- [x] [no-dupe-keys](https://eslint.org/docs/rules/no-dupe-keys) <kbd>error</kbd>
- [x] [no-duplicate-case](https://eslint.org/docs/rules/no-duplicate-case) <kbd>error</kbd>
- [x] [no-empty](https://eslint.org/docs/rules/no-empty) <kbd>error</kbd>
- [x] [no-empty-character-class](https://eslint.org/docs/rules/no-empty-character-class) <kbd>error</kbd>
- [x] [no-ex-assign](https://eslint.org/docs/rules/no-ex-assign) <kbd>error</kbd>
- [x] [no-extra-boolean-cast](https://eslint.org/docs/rules/no-extra-boolean-cast) <kbd>error</kbd>
- [x] [no-extra-parens](https://eslint.org/docs/rules/no-extra-parens) <kbd>off</kbd>
- [x] [no-extra-semi](https://eslint.org/docs/rules/no-extra-semi) <kbd>error</kbd>
- [x] [no-func-assign](https://eslint.org/docs/rules/no-func-assign) <kbd>error</kbd>
- [x] [no-inner-declarations](https://eslint.org/docs/rules/no-inner-declarations) <kbd>error | both</kbd>
- [x] [no-invalid-regexp](https://eslint.org/docs/rules/no-invalid-regexp) <kbd>error</kbd>
- [ ] [no-irregular-whitespace](https://eslint.org/docs/rules/no-irregular-whitespace)
- [x] [no-obj-calls](https://eslint.org/docs/rules/no-obj-calls) <kbd>error</kbd>
- [x] [no-prototype-builtins](https://eslint.org/docs/rules/no-prototype-builtins) <kbd>error</kbd>
- [x] [no-regex-spaces](https://eslint.org/docs/rules/no-regex-spaces) <kbd>error</kbd>
- [x] [no-sparse-arrays](https://eslint.org/docs/rules/no-sparse-arrays) <kbd>error</kbd>
- [x] [no-template-curly-in-string](https://eslint.org/docs/rules/no-template-curly-in-string) <kbd>error</kbd>
- [x] [no-unexpected-multiline](https://eslint.org/docs/rules/no-unexpected-multiline) <kbd>error</kbd>
- [x] [no-unreachable](https://eslint.org/docs/rules/no-unreachable) <kbd>error</kbd>
- [x] [no-unsafe-finally](https://eslint.org/docs/rules/no-unsafe-finally) <kbd>error</kbd>
- [x] [no-unsafe-negation](https://eslint.org/docs/rules/no-unsafe-negation) <kbd>error</kbd>
- [x] [use-isnan](https://eslint.org/docs/rules/use-isnan) <kbd>error</kbd>
- [x] [valid-typeof](https://eslint.org/docs/rules/valid-typeof) <kbd>error | requireStringLiterals</kbd>

#### Stylistic Issues

- [x] [quotes](https://eslint.org/docs/rules/quotes) <kbd>error | single</kbd>

#### Installation

  Setup dependencies
  
  `npm install eslint`

  or 

  `yarn add eslint`


  Setup devDependencies

  `npm install --save-dev eslint-config-und` 

  or 

  `yarn add eslint-config-und --dev`

  ##### Implementacion for TypeScript and Webpack

  `npm install eslint-config-und eslint-loader eslint-plugin-typescript typescript-eslint-parser --save-dev`

  or

  `yarn add eslint-config-und eslint-loader eslint-plugin-typescript typescript-eslint-parser --dev`

  Add `.eslintrc` file:
****
```json
  {
    "parser": "typescript-eslint-parser",
    "parserOptions": {
      "sourceType": "module"
    },
    "plugins": [
        "typescript"
    ],
    "extends": "eslint-config-und"
  }
```

  Add a object into entry module.exports from `webpack.config.js` 

```json
  {
    enforce: 'pre',
    test: /\.tsx?$/,
    exclude: /node_modules/,
    loader: 'eslint-loader'
  }
```

So you can see eslint in acction:

- ![#B82F16](https://placehold.it/15/B82F16/000000?text=+) Red for errors
- ![#C5C33](https://placehold.it/15/C5C33/000000?text=+) Yellow for warn messages

It's all.