# Vue 3 Off-Canvas with Canvas Element

This is a TypeScript and Vue 3 component that creates a responsive off-canvas menu with a canvas element. The component uses the Bootstrap 5 off-canvas component and includes some additional classes for controlling the canvas element.

## Installation

To use this component, you will need to have Vue 3 and the Bootstrap 5 library installed in your project. You can then install this component via npm:

```bash
npm i s-canvas
```
### Usage
To use this component, you can import it into your Vue 3 component like so:


````
  <!-- Using a link -->
    <a class="btn btn-primary" data-bs-toggle="offcanvas" href="#offcanvasExample" role="button" aria-controls="offcanvasExample">
      Open Canvas
    </a>

    <!-- Using a button -->
    <button class="btn btn-primary" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasExample" aria-controls="offcanvasExample">
      Open Canvas
    </button>

    <!-- The canvas component -->
    <s-canvas title="My Canvas" id="offcanvasExample">
      <!-- Content goes here -->
    </s-canvas>
````

Props
This component accepts the following props:

- title	String	The title of the off-canvas menu.
- id	String	The id of the off-canvas menu.
- position	String	The position of the off-canvas menu (start, end, top, bottom).
- size	String	The size of the off-canvas menu (xxl, xl, lg, sm).
