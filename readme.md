![Build Status](https://img.shields.io/github/actions/workflow/status/B1gum/Tungsten/ci.yml?branch=main)
![License](https://img.shields.io/github/license/B1gum/Tungsten)
![Latest Release](https://img.shields.io/github/v/release/B1gum/Tungsten)


# Tungsten

**Tungsten** is a Neovim plugin that seamlessly integrates Wolfram functionalities directly into your editor. Includes capabilities like equation solving, plotting, partial derivatives, and more—all within Neovim.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
  - [Using packer.nvim](#using-packernvim)
  - [Using lazy.nvim](#using-lazynvim)
  - [Using vim-plug](#using-vim-plug)
- [Usage](#usage)
  - [Example: Solving an Equation](#example-solving-an-equation)
- [Roadmap](#roadmap)
  - [Ongoing](#ongoing)
  - [Q1 2025](#q1-2025)
  - [Q2 2025](#q2-2025)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)


## Features

- **Equation Solving:** Solve single equations, systems of equations, PDEs, and ODEs.
- **Plotting:** Generate 2D and 3D plots with extensive customization options.
- **Calculus Operations:** Perform differentiation (including partial derivatives), integration, and summations.
- **Simplifying Expressions:** Easily handle simplification of expressions written in LaTeX syntax
- **Imaginary Units:** Support for complex numbers and imaginary units.

## Installation

You can install **Tungsten** using your preferred Neovim plugin manager. Please refer to your plugin manager's documentation for specific installation instructions.


### Using packer.nvim

```lua
use 'B1gum/Tungsten'
```

### Using lazy.nvim
Add the following to your lazy.nvim setup configuration:

```lua
require('lazy').setup({
  {
    'B1gum/Tungsten',
    config = function()
      -- Plugin configuration goes here
    end
  }
})
```


### Using vim-plug
Add the following to your init.vim or init.lua:

```vim
Plug 'B1gum/Tungsten'
```

Then run `:PlugInstall` within Neovim.


## Usage

After installation, **Tungsten** provides several commands to enhance your mathematical computations within Neovim:

- `:TungstenAutoEval` – Evaluate expression symbolically.
– `:TungstenAutoEvalNumeric` – Evaluate expression numerically
– `:TungstenSolve` – Solve for variable in a single equation.
- `:TungstenSolveSystem` – Solve systems of equations.
- `:TungstenRoot` – Find roots of equations.
- `:TungstenPlot` – Generate plots.
- `:TungstenTaylor` – Generate a Taylor expansion.


### Example: Solving an Equation

1. **Select the Equation and Variable:**
   - Visually select the equation and specify the variable, e.g., `2x + 4 = 10, x`.

2. **Run the Command:**
   - Execute `:TungstenSolve`.

3. **View the Solution:**
   - The solution (`x = 3.`) will be appended below your selection.


## Roadmap

We are committed to continuously enhancing **Tungsten** to provide a comprehensive mathematical toolset within Neovim. Below is our roadmap outlining upcoming features, prioritized based on user feedback and impact.


### Ongoing

1. **Expanding Documentation and Providing Tutorials**
    - We are constantly striving towards providing better documentation and in the near future thorough tutorials for each command will be published.

2. **Bugfixes**
    - **Plot Functionality:** The plotting-functionality is currently experiencing a bug that means that no plot is generated when running the command.


### Q1 2025

3. **Solutions of PDEs and ODEs**
    - Implement handling of numeric and symbolic solving of Partial Differential Equations (PDEs) and Ordinary Differential Equations (ODEs).

4. **Root-finding**
    - Implement root-finding algorithms such as Newton's method and the secant method for root finding of complicated functions.

5. **Plot-customization**
    - **Axis Titles and Grid Settings:** Allow users to add and customize axis titles, labels, and grid lines.
    - **Adding points to plots:** Enable the addition of specific data points to existing plots for better visualization

6. **Unit Support and Conversion**
    - **Parsing units:** Automatically parse strings formatted with `\qty{value}{unit}`
    - **Minimal Unit Processing:** Handle basic unit conversions and calculations.
    - **Calculation:** Perform calculations involving units.
    - **Output with Units:** Display results with units in `\qty{value}{unit}`.
    - **Unit Conversion:** Convert from one unit to another both in `\qty{value}{unit}`-syntax.

7. **Factorization**
    - Enable polynomial and algebraic expression factorization within the editor.

8. **Matrix Operations**
    - **Addition & Subtraction:** Perform basic matrix addition and subtraction.
    - **Multiplication:** Support matrix multiplication.
    - **Inverse:** Calculate matrix inverses.
    - **Eigenvalues:** Compute eigenvalues and eigenvectors.
    - **Matrix Decomposition:** Provide various matrix decomposition techniques.

9. **Vector Calculus**
    - Incorporate operations such as gradient, divergence, and curl for vector fields.


### Q2 2025

10. **Fourier and Laplace Transforms**
   - Add functionalities to compute Fourier and Laplace transforms for complex signal processing tasks.

11. **Partial Fraction Decomposition**
    - Implement methods to decompose rational functions into partial fractions.

12. **Tensor Algebra**
    - Support tensor operations for advanced mathematical modeling.

13. **Data Import and Export**
    - **Data Analysis Toolbox:** Integrate tools for data analysis directly within Neovim.
    - **Formats Supported:** Enable import and export of `.JSON` and `.CSV` files for data manipulation.

14. **Custom Options**
    - **Custom Functions:** Allow users to define and use custom mathematical functions.
    - **Custom Replacements:** Enable custom string replacements for tailored workflows.
    - **Custom Syntax:** Support user-defined syntax for enhanced flexibility.
    - **Custom Unit Settings:** Provide options to customize unit handling and display settings.


## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. **Fork the Repository:** Click the "Fork" button at the top of the repository page.

2. **Clone Your Fork:**
```bash
git clone https://github.com/your-username/Tungsten.git
```    

3. **Create a New Branch:**
```bash
git checkout -b feature/YourFeatureName
```

4. **Make Your Changes:** Implement your feature or bug fix.

5. **Commit Your Changes:**
```bash
git commit -m "Add feature: YourFeatureName"
```

6. **Push to Your Fork:**
```bash
git push origin feature/YourFeatureName
```

7. **Submit a Pull Request:** Navigate to the original repository and click "Compare & pull request."


Please ensure your code follows the project's coding standards and includes appropriate tests.




## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For any questions or suggestions, feel free to open an issue or contact [B1gum](https://github.com/B1gum).

