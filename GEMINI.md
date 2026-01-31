# Project Overview

This is a Jekyll-based personal resume website. It is designed to be hosted on GitHub Pages. The project uses Jekyll to generate a static website from data files and templates. The content of the resume, such as experience, education, and projects, is stored in YAML files in the `_data` directory. This separation of content and presentation makes it easy to update the resume information.

The website has two different views: a web view and a print view. The web view is a simple, clean resume website. The print view is a more traditional resume layout, suitable for printing on paper. This is achieved using CSS media queries.

**Key Technologies:**

*   **Jekyll**: A static site generator written in Ruby.
*   **Ruby**: The programming language used by Jekyll.
*   **Liquid**: A templating language used by Jekyll.
*   **Sass**: A CSS preprocessor used for styling.
*   **YAML**: A data serialization language used for the resume content.

**Architecture:**

*   `_config.yml`: The main configuration file for the Jekyll site. It contains personal information and settings for the resume.
*   `_data`: This directory contains the resume content in YAML files. Each file corresponds to a section of the resume (e.g., `experience.yml`, `education.yml`).
*   `_layouts`: This directory contains the main layout for the resume, `resume.html`.
*   `_sass`: This directory contains the Sass files for styling the website. It includes a separate style for printing.
*   `index.html`: The main entry point for the website.
*   `Gemfile`: Specifies the Ruby gems required for the project, including Jekyll.

# Building and Running

To work on this project locally, you need to have Ruby and Bundler installed.

1.  **Install dependencies:**
    ```bash
    bundle install
    ```

2.  **Run the Jekyll server:**
    ```bash
    bundle exec jekyll serve
    ```

This will start a local web server at `http://localhost:4000`. The server will automatically regenerate the website whenever you make changes to the files.

# Development Conventions

*   **Content**: All resume content should be edited in the YAML files in the `_data` directory.
*   **Settings**: General settings, such as your name, email, and which sections to display, are configured in `_config.yml`.
*   **Styling**: Styles are written in Sass in the `_sass` directory. The main stylesheet is `css/main.scss`, which imports all the other Sass files.
*   **Print Styles**: To change the print layout, edit the `@media print` section in `_sass/_resume.scss`.

---
## Gemini CLI Session Summary (Ongoing)

**Overall Goal:** Convert the Jekyll-based resume project into a simple, static website using only HTML, CSS, and JavaScript, while preserving the web and print layouts.

**Current Status:** Completed. The project has been converted into a static HTML, CSS, and JavaScript website.

**Approach Taken:**
1.  **SASS Compilation:** Successfully compiled `_sass` files into `css/main.css` using a pure JavaScript SASS compiler.
2.  **Python Scripting (Abandoned):** Multiple attempts were made to create Python scripts to parse Liquid templates and YAML data. These scripts encountered persistent issues with Liquid tag parsing, conditional logic, and handling of various data structures, ultimately failing to produce a clean, fully converted `index.html`.
3.  **Manual HTML Cleanup:** Due to the complexities and failures of the Python scripting approach, a manual strategy was adopted involving direct modification and cleanup of the `index.html` file.

**Key Actions Performed:**
*   Fixed the page title in `index.html`.
*   Removed empty social media `<li>` tags and their associated SVG icons from the main content area.
*   Populated project names within their respective `<a>` tags in the "Projects" section using data from `_data/projects.yml`.
*   Removed the empty paragraph tag for the education summary.
*   Removed empty social media `<li>` tags from the print-specific social links section.
*   Removed all remaining HTML comments and any lingering Liquid tags from the `index.html` file.
*   Removed all `itemprop`, `itemscope`, and `itemtype` attributes from `index.html`.
*   Removed all Jekyll-related files (`_config.yml`, `Gemfile`, `Gemfile.lock`, `resume.html`), Python scripting artifacts (`converter.py`, `converter.v2.py`, `final_converter.py`, `the_real_final_converter.py`, `the_very_final_converter.py`), and temporary directories (`_assets/`, `_data/`, `_includes/`, `_layouts/`, `_sass/`, `_vendor/`, `.venv/`).
*   The `CNAME` file was also removed.
*   The `.git/` folder was preserved as requested by the user.
*   The `GEMINI.md` file was updated to reflect the completed work.

**Task State:**
1.  [DONE] Compile SASS into a static `main.css` file.
2.  [DONE] Manually clean up `index.html` to remove all remaining comments and Liquid tags, and unnecessary attributes.
3.  [DONE] Clean up the directory by removing all Jekyll-related files, Python scripts, and temporary build artifacts.

**Next Steps:**
The conversion to a static website is complete. The remaining files are `index.html`, `css/main.css`, `favicon.png`, `images/`, `LICENSE`, `README.md`, and the `.git/` directory.