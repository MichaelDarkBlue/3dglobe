# Animated 3D Globe

This project displays an animated 3D globe with dots representing different land types (water, grass, sand, mountain, snow). The globe is interactive, allowing users to control parameters such as the number of dots, rotation speed, and animation cycle durations.

## Features

-   **Interactive Controls**: Adjust dot count, rotation speed, animation cycle, fade duration, and life duration of dots.
-   **Dynamic Dot Generation**: Dots are generated incrementally based on land data.
-   **Realistic Lighting**: Dots on the "far side" of the globe appear brighter, simulating light reflection.
-   **Responsive Design**: The globe and controls adapt to different screen sizes.

## Setup

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/globe-project.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd globe-project
    ```
3.  Open `index.html` in your web browser.

## File Structure

-   `index.html`: The main HTML file containing the structure, styles, and JavaScript code for the globe.
-   `land-50m.json`: TopoJSON file containing the geographical data for land masses.

## Dependencies

-   **D3.js (v7)**: Used for geographical calculations (`d3.geoContains`).
-   **TopoJSON Client (v3)**: Used to parse the TopoJSON data.

These dependencies are included via CDN in `index.html`.

## How It Works

The script initializes a canvas and sets up various parameters for the globe and dot animation. It fetches geographical data from `land-50m.json` to determine land and water areas.

Dots are generated with random positions, types (water, grass, etc.), and animation phases. The `animate` function continuously updates the dot positions and appearance, creating the animation effect. User controls allow real-time modification of animation parameters.

The projection logic converts 3D coordinates of dots to 2D coordinates on the canvas, and a simple lighting model adjusts dot brightness based on their z-coordinate.
