# Tabbed Markdown Viewer

A simple, single-page web application that renders Markdown content into HTML. It features a tabbed interface allowing users to seamlessly switch between the formatted "Preview" and the raw "Markdown" source, with syntax highlighting for readability.

## Setup

This project is a self-contained static HTML file with no build process required.

1.  Save the provided code as `index.html`.
2.  Open the `index.html` file directly in your web browser.

## Usage

Upon opening the application, you will see a container with two tabs:

-   **Preview:** Displays the Markdown content rendered as styled HTML.
-   **Markdown:** Shows the original, raw Markdown source code with syntax highlighting.

Click on a tab to switch between the two views.

## Code Explanation

The application is built within a single `index.html` file, containing the structure, styling, and logic.

-   **HTML (`<body>`)**: Defines the main structure, including the tab buttons (`#markdown-tabs`) and the content panels for the rendered output (`#markdown-output`) and the source code (`#markdown-source`).
-   **CSS (`<style>`)**: Embedded CSS handles the layout and styling of the container, tabs, and rendered Markdown content, aiming for a clean, modern look.
-   **JavaScript (`<script>`)**:
    -   **Dependencies**: It relies on two external libraries loaded via CDN:
        -   `marked.js`: To parse the Markdown string into HTML.
        -   `highlight.js`: To provide syntax highlighting for code blocks within the rendered output and for the raw Markdown source view.
    -   **Initialization**: On `DOMContentLoaded`, the script sets a hardcoded Markdown string.
    -   **Rendering**: It uses `marked.parse()` to generate the HTML for the "Preview" tab and sets the `textContent` for the "Markdown" tab. `highlight.js` is configured to automatically style code blocks.
    -   **Tab Logic**: An event listener on the tab container (`#markdown-tabs`) manages the UI by toggling `.active` classes on the buttons and content panels to show/hide the appropriate view.

## License

This project is licensed under the MIT License.