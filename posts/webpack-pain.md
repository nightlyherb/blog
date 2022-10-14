---

title: Webpack Pain

date: 2022-10-14

categories:
    - programming
    - frontend

tags:
    - webpack
    - javascript

---

# Webpack Pain

Setting up webpack for a simple static web page was a pain.

-   Webpack assumes all modules are bundled in javascript.
    For CSS and HTML we have to use plugins to bypass the issue,
    and the plugins interact in subtle and nontrivial ways.

    -   **We have to work around and edit our code to please webpack.**

-   Current setup for static web page:

    -   `html-webpack-plugin` with

        -   `template` for the html file
        -   `chunks` to manually set which entry points to include in the html file
        -   using `html-loader` for html files

    -   `mini-css-extract-plugin` with

        -   Using `[MiniCssExtractPlugin.loader, "css-loader"]` for css files
        -   Including CSS **NOT IN HTML** but **IN JS bundle** (e.g. `import "style.css"`)
            -   `mini-css-extract-plugin` extracts the bundled CSS into a separate file,
                and it somehow gets included in the HTML file.
                The behavior is hard to reason about
                and I decided not to spend my time investigating this phenomenon
                and move on with life.

-   Consider using vite
