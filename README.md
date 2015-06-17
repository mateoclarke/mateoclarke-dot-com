# my portfolio

Here lies the repo for my personal site built with **[Jekyll](http://jekyllrb.com)**.



### 1. Install Jekyll

Poole is built for use with Jekyll, so naturally you'll need to install that. On Macs, it's rather straightforward:

```bash
$ gem install jekyll
```


You may also need to install Pygments, the Python syntax highlighter for code snippets that plays nicely with Jekyll. Read more about this [in the Jekyll docs](http://jekyllrb.com/docs/templates/#code_snippet_highlighting).

### 2. Running locally

Start a Jekyll server. In Terminal, from Jekyll site root directory is named):

```bash
$ jekyll serve
```

Open <http://localhost:4000> in your browser, and voilà.


## Options

Poole includes some customizable options, typically applied via classes on the `<body>` element.


### Rems, `font-size`, and scaling

Poole is built almost entirely with `rem`s (instead of pixels). `rem`s are like `em`s, but instead of building on the immediate parent's `font-size`, they build on the root element, `<html>`.

By default, we use the following:

```css
html {
  font-size: 16px;
  line-height: 1.5;
}
@media (min-width: 38em) {
  html {
    font-size: 20px;
  }
}

```

To easily scale your site's typography and components, simply customize the base `font-size`s here.


## License

Open sourced under the [MIT license](LICENSE.md).

<3
