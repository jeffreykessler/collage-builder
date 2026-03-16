# Collage Builder V5.0 Summary

## Overview
`collageV5.html` is a single-page web application that allows users to create, edit, and export photo collages. It features a three-step workflow (Upload, Choose Grid, Edit) and provides a highly interactive canvas based on draggable gutters, pan/zoom functionalities, and a customizable text overlay feature.

## Tech Stack & Libraries
- **HTML/CSS/JS:** Vanilla implementation without front-end frameworks like React or Vue.
- **Tailwind CSS:** Used via CDN for rapid styling, layout management, and responsive design.
- **Split.js:** Handles the dynamic, resizable grid system (both horizontal and vertical split panes).
- **html2canvas:** Captures the DOM elements of the collage and converts them into a downloadable image.
- **Google Fonts:** Integration of custom fonts (`Inter`, `Roboto`, `Lobster`, `Pacifico`, `Caveat`) for text overlays.

## Key Features
1. **Step 1: Image Upload**
   - Accept multiple images (JPEG, PNG, BMP, WEBP).
   - Thumbnail previews with a removal option.

2. **Step 2: Template Selection**
   - Pre-defined grid layouts ranging from basic N x M grids to complex asymmetrical/nested splits (e.g., "Main + Stack", "Symmetrical 7").
   - Ability to choose dynamic resize modes (adjust cell width vs. height) which dictates the Split.js instantiation.
   - Custom grid generation via prompt inputs for rows and columns.

3. **Step 3: Collage Editing & Interaction**
   - **Image Manipulation:** Images within slots can be panned, zoomed (via buttons or mouse wheel), dynamically replaced, and deleted.
   - **Drag and Drop Swap:** Images can be dragged from the bottom thumbnail bar into slots, or swapped between slots by dragging them over one another.
   - **Styling Controls:** Global controls for border color, cell spacing, corner radius, and the overall aspect ratio of the collage.
   - **Text Overlay:** An interactive text editor overlay allowing custom fonts, sizes, formatting (bold/underline), font colors, and backgrounds. The text box is both draggable and resizable within the collage container.
   - **Export:** The assembled layout can be downloaded as a `.png` or `.jpg` via the html2canvas library. A custom loading spinner appears during processing.

## Architecture Notes
- State is managed locally through a series of global variables (e.g., `uploadedImages`, `collageSlots`, `splitInstances`, `textState`).
- `Split.js` instance setups are complex to accommodate rows-first versus columns-first resizable bounds. A central `rebuildGrid` method tears down and reconstructs the HTML structure while attempting to meticulously preserve image placement and transforms.
