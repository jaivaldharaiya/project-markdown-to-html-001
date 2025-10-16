# Dynamic Markdown Renderer

## Summary

This is a simple, single-page web application that renders Markdown content into HTML. It features a clean, tabbed interface allowing users to switch between the rendered HTML preview and the original Markdown source code. The application uses the `marked.js` library for conversion and `highlight.js` for syntax highlighting.

## Setup

This is a self-contained static HTML file with no build process or server required.

1.  Save the provided HTML code as `index.html`.
2.  Open the `index.html` file directly in your web browser.

## Usage

Upon loading the page, you will see the rendered HTML content in the "Preview" tab.

-   Click the **Preview** tab to view the final HTML output.
-   Click the **Markdown** tab to view the original, syntax-highlighted Markdown source.

## Code Explanation

The application is built within a single `index.html` file, which includes all necessary HTML, CSS, and JavaScript.

-   **HTML**: The structure consists of a main container (`.markdown-container`) which holds the tab buttons (`#markdown-tabs`) and the content panes for the rendered output (`#markdown-output`) and the source code (`#markdown-source`).

-   **CSS**: All styling is embedded within a `<style>` block in the `<head>`. It provides a modern, responsive layout for the container, tabs, and rendered content, mimicking a familiar code editor or documentation style.

-   **JavaScript**: The logic is contained in a `<script>` tag at the end of the `<body>`.
    -   It uses a `DOMContentLoaded` event listener to ensure the script runs after the page is fully loaded.
    -   A hardcoded Markdown string (`# Hello Jaival!...`) is used as the input.
    -   It initializes `marked.js` and configures it to use `highlight.js` for syntax highlighting within code blocks.
    -   The script populates both the preview and source tabs with the appropriate content upon loading.
    -   An event listener on the tab container handles the logic for switching between the active tabs by toggling CSS classes.

-   **Dependencies**: The project relies on two external libraries delivered via CDN:
    -   [marked.js](https://marked.js.org/): For converting Markdown to HTML.
    -   [highlight.js](https://highlightjs.org/): For syntax highlighting.

## License

This project is licensed under the MIT License.