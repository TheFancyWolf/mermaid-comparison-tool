# Mermaid Diagram Comparison Tool

## Description

The Mermaid Diagram Comparison Tool is a web-based utility designed to help users visually compare two Mermaid diagrams and understand their differences. It renders both diagrams and leverages AI (via the Gemini API) to generate a concise, natural language list of changes between an "Old" and a "New" version. This tool is particularly useful for tracking changes in software architecture, system flows, or any process documented with Mermaid diagrams.

It features a dark mode interface, automatic text contrast adjustment for diagram readability, and a versatile fullscreen modal view that allows for focused single-diagram inspection or a side-by-side comparison with independent zoom and pan capabilities for each diagram.

## Features

* **Side-by-Side Diagram Input:** Paste or type Mermaid code for "Diagram Old" and "Diagram New".
* **Live Rendering:** Renders both diagrams on the main page.
* **AI-Powered Difference Analysis:** Generates a bullet-point list summarizing the key structural and flow differences between the two diagrams (e.g., added/removed/modified nodes and relationships).
* **Fullscreen Modal View:**
    * Click on a diagram on the main page to open it in a focused fullscreen view.
    * Toggle to a "Compare Diagrams" mode to see both diagrams side-by-side within the fullscreen modal.
    * Independent zoom (in, out, reset/fit-to-view) and pan (click-and-drag) controls for each diagram pane in the modal.
    * Remembers zoom/pan state for each diagram in both single and split-view modes within the session.
* **Dark Mode Interface:** A visually comfortable dark theme for the entire tool.
* **Automatic Text Contrast:** JavaScript logic attempts to automatically adjust text color within diagram nodes for better readability against various node background colors.

## How to Use

1.  **Input Diagrams:**
    * Paste the Mermaid code for your first diagram (e.g., the older version) into the "Diagram Old" text area.
    * Paste the Mermaid code for your second diagram (e.g., the newer version) into the "Diagram New" text area.
2.  **Render & Analyze:**
    * Click the "🔬 Render & Compare Diagrams" button.
    * The tool will render both diagrams below their respective input areas.
    * An AI-generated list of differences will appear below the rendered diagrams.
3.  **Fullscreen View & Comparison:**
    * Click on either the "Rendered Diagram Old" or "Rendered Diagram New" on the main page to open it in a fullscreen modal.
    * The modal will initially show the clicked diagram in a single, fit-to-view pane.
    * **Modal Controls:**
        * Use the "Old Diagram" or "New Diagram" buttons at the top of the modal to switch which diagram is shown in the single-pane view.
        * Click the "Compare Diagrams" button to switch to a side-by-side split view of both diagrams.
        * Click "Hide Comparison" (which the "Compare Diagrams" button becomes) to return to the last active single-diagram view.
        * Use the dedicated zoom controls (+, -, Reset) for each pane to adjust the view.
        * Click and drag within a diagram pane to pan.
        * Click the "×" button to close the modal.

## Technology Used

* **HTML:** Structure of the web page.
* **CSS:** Styling, including some utility classes from **Tailwind CSS** (via CDN).
* **JavaScript:** For all client-side logic, including:
    * Mermaid.js integration for rendering diagrams.
    * DOM manipulation for dynamic updates.
    * Event handling for interactivity (buttons, zoom, pan).
    * Automatic text contrast adjustment.
    * Calling the Gemini API for diagram comparison.
* **Mermaid.js:** A JavaScript-based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically.
* **Gemini API:** Used for the AI-powered analysis of diagram differences. (Note: An API key is required for this functionality if used outside of an environment where it's provided, like AI Studio.)

## How to Run Locally

1.  Save the complete HTML code of the tool as an `.html` file (e.g., `mermaid_comparison_tool.html` or `index.html`).
2.  Open this file in any modern web browser (like Chrome, Firefox, Edge, Safari).

## Sharing

This tool is a single HTML file and can be easily shared:
* Directly as an `.html` file.
* Hosted on any static web hosting service (e.g., GitHub Pages, Netlify, Vercel).
* Pasted into online code playgrounds like CodePen or JSFiddle.
