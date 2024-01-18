# @nish1896/eslint-config-lint-rules

**[eslint](https://eslint.org/) and [stylistic](https://eslint.style/) rules to help you and fellow developers follow the industry-recommended coding practices for easier readability, maintenance and productivity!**

The usage of `eslint-stylistic` over [prettier](https://prettier.io/) will give you additional options to format your code and hopefully avoid conflict of rules between `eslint` and `prettier` for which you additionally had to install [eslint-config-prettier](https://www.npmjs.com/package/eslint-config-prettier). Some of the rules imported from this plugin will give you a warning ⚠️ when running `eslint --fix` indicating that the code issue can be ignored while the rules triggering an error ❌ indicate that your code might not be as per the industry standards and that coding style should be avoided.

## Installation

You'll first need to install [ESLint](https://eslint.org/):

```
npm i eslint --save-dev
```
```
yarn add -D eslint
```

Next, install `@nish1896/eslint-plugin-nish-lint` and `@stylistic/eslint-plugin` :

```
npm install @nish1896/eslint-config-lint-rules @stylistic/eslint-plugin --save-dev
```
```
yarn add -D @nish1896/eslint-config-lint-rules @stylistic/eslint-plugin
```

## Usage

Add `@nish1896/eslint-config-lint-rules` to the extends section of your `.eslintrc` configuration file. The plugin also has `eslint-stylistic` rules defined, but unfortunately it needs to be manually configured in your `.eslintrc` or `eslint.config.js`.

```json
{
    "extends": [
        "@nish1896/eslint-config-lint-rules"
    ],
    "plugins": [
        "@stylistic/eslint-plugin"
    ]
}
```

To run linting across your project, add a *"lint"* command to your `package.json` file.

```
npm pkg set scripts.lint="eslint --fix"
```

[Integrate with husky](https://typicode.github.io/husky/getting-started.html) as a `pre-commit` git hook to make sure no bad code passes through!

## List of Rules

Check out the complete list of [eslint](https://eslint.org/docs/latest/rules/) and [stylistic](https://eslint.style/rules/default) rules.

To search or read about the documentation of a specific rule, append the rule name as a suffix to [https://eslint.org/docs/latest/rules/](https://eslint.org/docs/latest/rules/) or [https://eslint.style/rules/default](https://eslint.style/rules/default). 

⚠️ ***WARNING*** - avoid using this style of code.  
❌ ***ERROR*** - your code is 🗑️  
🔧 ***FLEXIBLE*** - make eslint less strict and more developer-friendly.  

## **Enabled Stylistic rules**

All rule names start with `@stylistic/` prefix.

|Rule Name|⚠️|❌|🔧|
|-|-|-|-|
|[array-bracket-newline](https://eslint.style/rules/default/array-bracket-newline)||✔️| { multiline: true, minItems: 4 } |
|[arrow-parens](https://eslint.style/rules/default/arrow-parens)|✔️|| as-needed|
|[arrow-spacing](https://eslint.style/rules/default/arrow-spacing)||✔️||
|[block-spacing](https://eslint.style/rules/default/block-spacing)||✔️||
|[brace-style](https://eslint.style/rules/default/brace-style)||✔️||
|[comma-dangle](https://eslint.style/rules/default/comma-dangle)||✔️|  always-multiline |
|[comma-spacing](https://eslint.style/rules/default/comma-spacing)||✔️||
|[eol-last](https://eslint.style/rules/default/eol-last)||✔️||
|[function-call-argument-newline](https://eslint.style/rules/default/function-call-argument-newline)||✔️| consistent |
|[function-paren-newline](https://eslint.style/rules/default/function-paren-newline)||✔️| multiline |
|[indent](https://eslint.style/rules/default/indent)||✔️| 2 |
|[jsx-closing-bracket-location](https://eslint.style/rules/default/jsx-closing-bracket-location)||✔️||
|[jsx-closing-tag-location](https://eslint.style/rules/default/jsx-closing-tag-location)||✔️||
|[jsx-first-prop-new-line](https://eslint.style/rules/default/jsx-first-prop-new-line)|✔️|| multiline-multiprop |
|[jsx-indent](https://eslint.style/rules/default/jsx-indent)||✔️| 2 |
|[jsx-indent-props](https://eslint.style/rules/jsx-indent-props)||✔️| 2 |
|[jsx-quotes](https://eslint.style/rules/default/jsx-quotes)|✔️|| prefer-double |
|[jsx-self-closing-comp](https://eslint.style/rules/default/jsx-self-closing-comp)||✔️||
|[key-spacing](https://eslint.style/rules/default/key-spacing)||✔️||
|[linebreak-style](https://eslint.style/rules/default/linebreak-style)|✔️|||
|[lines-around-comment](https://eslint.style/rules/default/lines-around-comment)|✔️|||
|[no-extra-semi](https://eslint.style/rules/default/no-extra-semi)||✔️||
|[no-floating-decimal](https://eslint.style/rules/default/no-floating-decimal)||✔️||
|[no-mixed-operators](https://eslint.style/rules/default/no-mixed-operators)||✔️||
|[no-mixed-spaces-and-tabs](https://eslint.style/rules/default/no-mixed-spaces-and-tabs)|✔️|||
|[no-multi-spaces](https://eslint.style/rules/default/no-multi-spaces)||✔️||
|[no-multiple-empty-lines](https://eslint.style/rules/default/no-multiple-empty-lines)||✔️||
|[no-trailing-spaces](https://eslint.style/rules/default/no-trailing-spaces)|✔️|||
|[object-curly-spacing](https://eslint.style/rules/default/object-curly-spacing)||✔️| always |
|[object-property-newline](https://eslint.style/rulesobject-property-newline)|✔️|||
|[operator-linebreak](https://eslint.style/rules/default/operator-linebreak)||✔️| before |
|[quotes](https://eslint.style/rules/default/quotes)||✔️| single |
|[semi-spacing](https://eslint.style/rules/default/semi-spacing)|✔️|||
|[spaced-comment](https://eslint.style/rules/default/spaced-comment)|✔️|||
|[switch-colon-spacing](https://eslint.style/rules/default/switch-colon-spacing)|✔️|||
|[template-curly-spacing](https://eslint.style/rules/default/template-curly-spacing)||✔️||
|[type-annotation-spacing](https://eslint.style/rules/default/type-annotation-spacing)|✔️|||
|[type-generic-spacing](https://eslint.style/rules/default/type-generic-spacing)||✔️||
|[type-named-tuple-spacing](https://eslint.style/rules/default/type-named-tuple-spacing)||✔️||
|[wrap-regex](https://eslint.style/rules/default/wrap-regex)||✔️||

## **Enabled eslint rules**

|Rule Name|⚠️|❌|🔧|
|-|-|-|-|
|[array-callback-return](https://eslint.org/docs/latest/rules/array-callback-return)|✔️|||
|[arrow-body-style](https://eslint.org/docs/latest/rules/arrow-body-style)|✔️|| as-needed |
|[curly](https://eslint.org/docs/latest/rules/curly)|✔️|||
|[default-case](https://eslint.org/docs/latest/rules/default-case)|✔️|||
|[default-param-last](https://eslint.org/docs/latest/rules/default-param-last)|✔️|||
|[dot-notation](https://eslint.org/docs/latest/rules/dot-notation)||✔️||
|[eqeqeq](https://eslint.org/docs/latest/rules/eqeqeq)||✔️||
|[func-names](https://eslint.org/docs/latest/rules/)|✔️|| as-needed |
|[id-denylist](https://eslint.org/docs/latest/rules/id-denylist)|✔️|| 'e', 'cb', 'callback' |
|[id-length](https://eslint.org/docs/latest/rules/id-length)||✔️| { min: 3, max: 25 } |
|[multiline-comment-style](https://eslint.org/docs/latest/rules/multiline-comment-style)||✔️| starred-block |
|[no-await-in-loop](https://eslint.org/docs/latest/rules/no-await-in-loop)|✔️|||
|[no-debugger](https://eslint.org/docs/latest/rules/no-debugger)|✔️|||
|[no-eq-null](https://eslint.org/docs/latest/rules/no-eq-null)||✔️||
|[no-inline-comments](https://eslint.org/docs/latest/rules/no-inline-comments)||✔️||
|[no-plusplus](https://eslint.org/docs/latest/rules/no-plusplus)||✔️||
|[no-shadow](https://eslint.org/docs/latest/rules/no-shadow)|✔️|||
|[no-unreachable](https://eslint.org/docs/latest/rules/no-unreachable)|✔️|||
|[no-unused-vars](https://eslint.org/docs/latest/rules/no-unused-vars)|✔️|||
|[no-use-before-define](https://eslint.org/docs/latest/rules/no-use-before-define)||✔️||
|[no-var](https://eslint.org/docs/latest/rules/no-var)|✔️|||
|[object-shorthand](https://eslint.org/docs/latest/rules/object-shorthand)||✔️||
|[prefer-const](https://eslint.org/docs/latest/rules/prefer-const)||✔️||
|[prefer-exponentiation-operator](https://eslint.org/docs/latest/rules/prefer-exponentiation-operator)|✔️|||
|[prefer-promise-reject-errors](https://eslint.org/docs/latest/rules/prefer-promise-reject-errors)|✔️|||
|[prefer-rest-params](https://eslint.org/docs/latest/rules/prefer-rest-params)||✔️||
|[require-await](https://eslint.org/docs/latest/rules/require-await)||✔️||
|[sort-keys](https://eslint.org/docs/latest/rules/sort-keys)|✔️|| 'asc', { caseSensitive: true, natural: false, minKeys: 2 } |
|[sort-vars](https://eslint.org/docs/latest/rules/sort-vars)||✔️| { ignoreCase: true } |
|[use-isnan](https://eslint.org/docs/latest/rules/use-isnan)|✔️|||

## **eslint-plugin-react rules**
| Rule Name |⚠️|❌|🔧|
|-|-|-|-|
|[react/jsx-uses-vars](https://github.com/jsx-eslint/eslint-plugin-react/blob/master/docs/rules/jsx-uses-vars.md)||✔️||
|[react/jsx-filename-extension](https://github.com/jsx-eslint/eslint-plugin-react/blob/master/docs/rules/jsx-filename-extension.md)|✔️|| { extensions: ['.tsx, '.jsx] } |

## **Disabled eslint rules**
| Rule Name | reason |
|-|-|
|[@typescript-eslint/no-unused-vars](https://typescript-eslint.io/rules/no-unused-vars/) | set eslint `no-unused-vars` rule to `warn`
|[react/react-in-jsx-scope](https://github.com/jsx-eslint/eslint-plugin-react/blob/master/docs/rules/react-in-jsx-scope.md) | react v17+ don't require `react` import | 

Checkout out other [recommended community plugins](/Recommendations.md)

[Create your own plugin](https://eslint.org/docs/latest/extend/plugins).

# Support Me

If you found this plugin useful, please don't forget to star the repository. It would make my day if you consider [buying me a coffee](https://www.buymeacoffee.com/nish1896)  