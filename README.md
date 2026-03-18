# Collage Builder

A sleek, feature-rich, entirely client-side web application for creating beautiful photo collages. Built natively with HTML5, vanilla JavaScript, and Tailwind CSS, Collage Builder allows users to seamlessly assemble, customize, and export high-quality image spreads effortlessly right in the browser.

## Features

- **Flexible Grid Templates:** Choose from standard uniform grids, vertically/horizontally nested layouts, and specialized "Large Center" designs.
- **Drag and Drop Mechanics:** Effortlessly swap image positions by dragging and dropping them into different slots.
- **Dynamic Pan & Zoom:** Double-click any image slot to unlock panning and scaling/zooming controls to frame your shots perfectly.
- **Custom Styling:** Control internal grid spacing, round corners, and apply custom colored borders globally across all slots.
- **Text Overlays:** Add, customize, resize, and freely drag decorative text overlays across your composition with native font and color controls.
- **Save & Load Progress:** Native File-System integration utilizing `fflate` compression allows you to securely save your active workspace as a customized `.collage` project file and restore your exact pan/zoom configurations later!
- **High-Quality Exporting:** Powered by `html2canvas`, export your final composition flawlessly to crisp PNG or compressed JPG files.

## Technology Stack

- **HTML5 & Vanilla JavaScript** (No complex build frameworks required)
- **Tailwind CSS** (via CDN for incredibly rapid, modern UI styling)
- **Split.js** (For interactively adjustable layout pane resizing)
- **html2canvas** (For rendering the final DOM structure to exportable Image Data)
- **fflate** (For handling high-speed, invisible `.collage` project save-state compression)

## Usage

Since Collage Builder executes 100% locally within your browser with zero backend dependencies, setting it up is instant:

1. Clone or download this repository.
2. Open `collageV6.html` directly in any modern web browser.
3. Upload your photos to get started!

## Deployment

Because this is a static site, you can host Collage Builder entirely for free via GitHub Pages, Vercel, Netlify, or AWS S3.

## License

MIT License. Feel free to fork, modify, and build upon this application.
