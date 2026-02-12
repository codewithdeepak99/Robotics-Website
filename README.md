NIT Patna RoboticsClub Website
Project Overview

live demo:- https://codewithdeepak99.github.io/Robotics-Club-Website-NITP/


This repository hosts the source code for the NIT Patna Robotics Club web platform.


The architecture follows a strict static site generation approach using semantic HTML5, CSS3, and Vanilla JavaScript. The design philosophy prioritizes performance, utilizing native browser APIs for animations and layout (CSS Grid/Flexbox) to eliminate the need for heavy external dependencies or frameworks.

Tech used:- 

Semantic Structure (HTML): The document object model is organized semantically to ensure accessibility and SEO optimization.

Design System (CSS): The visual layer utilizes CSS Custom Properties (Variables) for theming. The interface implements a glassmorphism aesthetic using backdrop-filter and semi-transparent RGBA color spaces.

Behavioral Logic (JavaScript): Interactivity is handled via a single, consolidated script that manages the canvas rendering engine, DOM manipulation for navigation, and Intersection Observers for scroll-based entrance animations.


Module Descriptions
1. Canvas Particle Engine (script.js)
The background visualization is not a video or a static image but a computationally generated network rendered in real-time.

Particle Class: A Particle class is defined to manage individual node properties, including X/Y coordinates, velocity vectors, and color data.

Animation Loop: The animate() function utilizes requestAnimationFrame to create a render loop. In each frame, it clears the canvas, updates particle positions, and calculates the Euclidean distance between particles.

Connection Logic: If two particles are within a specific proximity threshold, a line is drawn between them. The opacity of the line is inversely proportional to the distance, creating a fading network effect.

2. Styling and Theming (style.css)
The CSS architecture is built for maintainability. All primary colors, font families, and layout spacing are defined in the :root scope.

Variables:

--primary: Controls the cyan highlight color used for active states and focus rings.

--card-bg: Defines the alpha-channel background for the glassmorphism effect.

--font-head / --font-body: Centralizes typography choices (Orbitron and Inter).

Responsive Design: Media queries are implemented at the 768px breakpoint. The navigation transforms from a horizontal flex row to a vertical slide-out drawer on mobile devices.

3. Responsiveness
Mobile Navigation: A toggle event listener manipulates class lists on the navigation header to handle state changes (active/inactive).

Scroll Observer: The application uses the IntersectionObserver API. This asynchronous observer watches for elements entering the viewport and triggers a CSS transform (fade-up) to smooth the user experience during scrolling.

Note regarding local file policies: Some browsers restrict ES6 module loading or specific canvas operations when opening files directly via the file:// protocol. It is recommended to use a local development server.

If using VS Code:

Install the "Live Server" extension.

Right-click index.html and select "Open with Live Server".

Configuration
To modify the visual theme without altering the core codebase, navigate to style.css and adjust the root variables:

Color Scheme: Update --primary and --secondary to change the brand colors.

Background: The particle density can be adjusted in script.js by modifying the numberOfParticles calculation in the init() function.

Typography: Font imports are located in the <head> of the HTML files. To change fonts, update the Google Fonts link and the corresponding CSS variables.

Browser Support
The application is tested and fully functional on:

Google Chrome (latest stable)

Mozilla Firefox (latest stable)

Microsoft Edge (Chromium-based)

Safari (macOS and iOS)

Authors

Aditya Kunwar - 2506069 - CSE Dept.
Lucky Kumar - 2512003 - EE(VLSI) Dept.
Utkarsh Kumar - 2504040 - ECE Dept.
Deepak Yadav - 2506076 - CSE Dept.
