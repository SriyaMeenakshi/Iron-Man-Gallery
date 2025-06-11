# Iron Man: Themed Gallery & Slideshow

### A responsive webpage created for Level 3, Task 1 of the Cognifyz Web Development Internship.

This project is a static webpage built entirely with HTML and CSS, showcasing a tribute to Iron Man. It demonstrates advanced CSS techniques for creating interactive and animated components without relying on JavaScript.



---

## About The Project

The goal of this task was to create a feature-rich, single-page website using only HTML and CSS. The project is divided into two main sections, each demonstrating a different CSS concept, all wrapped in a visually appealing "Iron Man" theme.

## Features

-   **Themed UI**: Dark mode design with an "Iron Man" red and gold color palette.
-   **Responsive Design**: The layout adapts to various screen sizes using CSS Grid with `auto-fit` and a fluid structure.
-   **Click-to-Enlarge Image Gallery**:
    -   A grid of thumbnails that are clickable.
    -   Opens a full-screen, high-resolution version of the image in a lightbox overlay.
-   **Pure CSS Lightbox**:
    -   This interactive feature is built without any JavaScript.
    -   It uses anchor links (`<a href="#img1">`) and the `:target` CSS pseudo-class to control the visibility of the lightbox `div`.
-   **Automatic CSS Slideshow**:
    -   A container that automatically cycles through a set of images.
    -   Features a smooth fade-in/fade-out transition effect.
    -   Built using CSS `@keyframes` for the animation and `animation-delay` to stagger the appearance of each image in the sequence.

---

## Technologies Used

-   **HTML5**: For the structure and content of the webpage.
-   **CSS3**: For all styling, layout, and functionality.
    -   **CSS Grid Layout**: For the responsive image gallery.
    -   **CSS Flexbox**: For centering content within the lightbox.
    -   **CSS Animations (`@keyframes`)**: For the automatic slideshow.
    -   **CSS Transitions**: For smooth hover effects on gallery images.
    -   **CSS Pseudo-classes (`:target`)**: For the core logic of the lightbox.

---

## How It Works

### The Lightbox Effect

The lightbox is powered by the `:target` pseudo-class.
1.  Each thumbnail is wrapped in an `<a>` tag pointing to a unique ID (e.g., `href="#img1"`).
2.  A corresponding `<div>` with that `id` (e.g., `<div id="img1">`) contains the full-size image. This `div` is hidden by default (`display: none`).
3.  When a user clicks the link, the URL fragment changes (e.g., `.../page.html#img1`), and the `div` with `id="img1"` becomes the `:target` of the document.
4.  A CSS rule `.lightbox:target { display: flex; }` makes the targeted `div` visible.
5.  The "close" button is a link back to `#` or an empty fragment, which removes the `:target` state from the div, hiding it again.

### The Slideshow

1.  All images are placed inside a container with `position: relative`.
2.  Each `<img>` is set to `position: absolute`, stacking them on top of each other. All are initially hidden with `opacity: 0`.
3.  A single `@keyframes` animation (`fade-slideshow`) is defined to fade an image in, hold it, and then fade it out over a 12-second duration.
4.  This animation is applied to all images, but with a different `animation-delay` for each one (`0s`, `4s`, `8s`), ensuring they appear one after another in a continuous loop.

---

## Setup

To run this project locally:

1.  Clone the repository:
    ```sh
    git clone https://github.com/your-username/your-repo-name.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd your-repo-name
    ```
3.  Open the `iron_man_gallery.html` file in your web browser.

---

## Acknowledgements

-   This project was completed as part of the **Cognifyz Technologies** Web Development Internship.
-   Inspiration from the Marvel Cinematic Universe.
