# WordPress Configuration Extraction Tool

A client-side tool to extract WordPress site configuration settings and generate an HTML report. This tool runs entirely in your browser.

## Badges
<!-- This badge will become active after the first release/tag is pushed and a release is created on GitHub from the tag. -->
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/rinmon/WordPress-Reporter)](https://github.com/rinmon/WordPress-Reporter/releases/latest)
<!-- Add a license badge here if you choose a license -->
<!-- e.g., [![GitHub license](https://img.shields.io/github/license/rinmon/WordPress-Reporter)](https://github.com/rinmon/WordPress-Reporter/blob/main/LICENSE) -->

## Features
- Extracts various WordPress settings via the REST API:
    - General, Display, Discussion, Media, Permalinks settings
    - Active Plugins list
    - Active Theme information
    - Users list and roles
    - (Widgets and Menus are currently not supported due to REST API limitations)
- Generates a downloadable HTML report of the extracted data.
- Operates entirely client-side; no data is sent to any server other than the target WordPress site.
- User credentials are handled in memory and discarded after use.

## How to Use
1.  **Download:** Get the `index.html` file from this repository.
2.  **Open:** Open the `index.html` file directly in your web browser (e.g., Chrome, Firefox, Edge).
3.  **Input Credentials:**
    *   Enter the full URL of your WordPress site (e.g., `https://example.com`).
    *   Enter your WordPress Username or Application Password username.
    *   Enter your WordPress Password or Application Password.
4.  **Extract Data:** Click the "ログインして抽出開始" (Login and Start Extraction) button. The tool will fetch data from your WordPress site.
5.  **Download Report:** Once the extraction is complete, a summary will be displayed. Click the "HTMLをダウンロード" (Download HTML) button to save the report.

## Dependencies
This tool uses the following libraries via CDN:
-   [React](https://reactjs.org/)
-   [ReactDOM](https://reactjs.org/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [Babel Standalone](https://babeljs.io/docs/en/babel-standalone) (for JSX transpilation in the browser)
-   [jsPDF](https://parall.ax/products/jspdf) (Note: PDF generation was initially planned but had issues; current primary output is HTML. jsPDF library is still linked.)

## Compatibility
-   Designed to work on modern desktop browsers:
    -   Google Chrome
    -   Mozilla Firefox
    -   Microsoft Edge
-   Tested on macOS and Windows.

## Development Notes
- The application is a single `index.html` file.
- WordPress REST API must be enabled and accessible on the target site. Basic Authentication or Application Passwords should be usable.

## License
Please add a LICENSE file if you wish to specify one (e.g., MIT License).
