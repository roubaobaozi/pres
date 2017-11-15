@title[Introduction]
# Prettier

>Prettier is an opinionated code formatter. It enforces a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.

---

@title[An example]
## An example

```javascript
foo(reallyLongArg(), omgSoManyParameters(), IShouldRefactorThis(), isThereSeriouslyAnotherOne());
```

Automagically turns into:

```javascript
foo(
    reallyLongArg(),
    omgSoManyParameters(),
    IShouldRefactorThis(),
    isThereSeriouslyAnotherOne()
);
```

---

@title[An example part 2]

However, when you only have a short line, it’s easy to read still, so:

```javascript
foo(bar(), short());
```

… doesn’t get changed.

---

@title[Options]
## Options

In a .prettierrc file, you can add:

- `printWidth`: when to start wrapping lines
- `tabWidth`: 4
- `singleQuote`: self-explanatory
- `trailingComma`: "es5" (where valid in ES5) or "all"/"none"

---

@title[Options part 2]
- `bracketSpacing`: eg. `{ foo: bar }`
- `jsxBracketSameLine`:
    ```javascript
    <Component
        attribute="value"
    > // <-- false
    ```
-  `parser`: babylon, flow, typescript, postcss, json, graphql, markdown

---
@title[Options part 3]
- `semi`: semi-colons
- `useTabs`: eww
- `overrides`: so we can use the `postcss` parser for prettifying the scss, etc.

There aren’t that many options, because it doesn’t do **that** much. Which could be a good or bad thing.

---

@title[Why use it]
## Why should we use it?

How many linting errors and PR comments are nitpicks?

>“Too many/not enough spaces”

>“Two carriage returns instead of three”

>“Put these on separate lines”

---

@title[Why use it part 2]

What if we could speed up the dev process, and PR process, by avoiding these nitpicks altogether?

What if we could, as a team, have more consistent code without the effort?

---

@title[Why not to use it]
## Why shouldn’t we use it?

1. Will it make us lazy developers?

    Not having to fix these things ourselves can mean that without Prettier, our code looks terrible.
1. Is the lack of rules too restrictive in terms of how customised we might want it to be?

I can’t think of anything else that’s bad. What about **you**?

---

@title[Play]
# Play

[prettier.io/playground/](https://prettier.io/playground/#N4Igxg9gdgLgprEAuc0DOMAEAbAllOAVQAc0AxCAJwAUI1cZdpMBeTAgd0wEFLKBDAJ4AKALb8AHgBU4-UQGVcALzgBKAHQAzXNmxjJMuYpWqAOlEyXM68cWHCAbv2wBXOABpMYF3wQwAklAAJnASqqwAfJjA5lZxXuhY8HLcABL8aNTYQnCUrF4+lH609IzQhqJoANrJotzqkCEAupgAZK0FvrAlDExQFdW19Y1wTVXeXQHBoU0A3LHxlpBQGJi1AELpmdmCufkTRd10veWylTVn6w0QzW0dB8XHZf1ng5fXzeOFfoEhEnPmBaLIowHwWGIWRbxYg7XIARiQazOaQyWRyeQA-J1DjAes8BhcUh9Rl9Jr8ZphEVAXLp3ECoZYYeiAEyIjZbNG7THYx6lPoEjbEsYPWDk-6U9g07B0yEMxlPPqIkW4hXQelxAC+81lmA1qlmIHcIAgxGeaGQoAyMGQmmcaA8IAARgIwABrOAweTEfhgfAAc2QMEobiNQQgYBtdod+HtlFxAj94kj2HtRoAVmgJOsXe7PXI4AAZfBwQPBh0QFwwYiV5nJ1Mgb2UWPIJ38R2CbDQQ0Nyj4GAAdVwQRgAAtkAAOAAMRuIlDocH7AmIpZDICKAEcXLgitQE0mkLaUw77aJcCvj-7sHAAIouCDwc9GmBtwfDsdIAAsT4EOn9AGEIFEfcQCgaASyNFx7SkNtzQPKMNQ1IA)