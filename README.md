# RCKSTR Math Solver

## Overview

The RCKSTR Math Solver is a web-based tool designed to solve various mathematical problems, including general math expressions, circle area, square area, and compound shapes' area and perimeter. The tool features a toggleable dark mode, a virtual keypad for special mathematical symbols, and multiple tabs for different types of calculations.

## Features

- **Math Solver**: Solve general mathematical expressions.
- **Circle Area Calculator**: Calculate the area of a circle given its radius.
- **Square Area Calculator**: Calculate the area of a square given its side length.
- **Compound Area Calculator**: Calculate the combined area of a rectangle and a triangle.
- **Compound Perimeter Calculator**: Calculate the perimeter of a compound shape made up of a rectangle and a triangle.
- **Dark Mode**: Toggle between light and dark modes for a comfortable viewing experience.
- **Virtual Keypad**: Easily insert mathematical symbols that are not readily available on a standard keyboard.

## Installation

### Prerequisites

- WordPress installed and running on your web server.
- Basic knowledge of creating and managing a WordPress theme.

### Steps

1. **Create a Child Theme**:
   - Create a new folder in `wp-content/themes/`, e.g., `my-child-theme`.
   - Inside this folder, create a `style.css` file with the following content:
     ```css
     /*
     Theme Name: My Child Theme
     Template: parent-theme-folder-name
     */
     ```
     Replace `parent-theme-folder-name` with the name of your current theme.
   - Create a `functions.php` file inside the same folder:
     ```php
     <?php
     add_action('wp_enqueue_scripts', 'enqueue_parent_styles');
     function enqueue_parent_styles() {
         wp_enqueue_style('parent-style', get_template_directory_uri() . '/style.css');
     }
     ```

2. **Create a Custom Page Template**:
   - In your child theme folder, create a file named `page-math-solver.php` and add the provided HTML, CSS, and JavaScript content.
   - Ensure you include the PHP header for the custom page template:
     ```php
     <?php
     /* Template Name: Math Solver */
     get_header();
     ?>
     ```
   - Add the remaining content of your HTML, CSS, and JavaScript.

3. **Add the Custom Page Template in WordPress**:
   - Go to your WordPress admin dashboard.
   - Create a new page (`Pages > Add New`).
   - Select "Math Solver" from the "Template" dropdown in the "Page Attributes" section.
   - Publish the page.

## Usage

1. **Access the Math Solver**:
   - Navigate to the page where you applied the "Math Solver" template.
   - Use the tabs to select the type of calculation you want to perform.
   - Enter the required values and click the "Calculate" or "Solve" button.
   - Use the virtual keypad to insert special symbols if needed.
   - Press "Enter" to trigger calculations without clicking the button.

2. **Toggle Dark Mode**:
   - Click the "Toggle Dark Mode" button at the top of the page to switch between light and dark themes.

## Footer

&copy; 2024 The Rockstar Team

## Contributions

Contributions are welcome! If you have suggestions for improvements, feel free to create issues or pull requests.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
