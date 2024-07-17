
**`document-css`**

Enables inclusion of most of the [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS) in the `styles.html` [partial](https://pandoc.org/MANUAL.html#partials) (have a look with `pandoc --print-default-data-file=templates/styles.html`). Unless you use [`--css`](https://pandoc.org/MANUAL.html#option--css), this variable is set to `true` by default. You can disable it with e.g. `pandoc -M document-css=false`.