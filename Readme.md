# The course repo: aef_environment

This repo initializes an RStudio project and `renv` package management system for the course *Advanced Empirical Finance: Topics and Data Science* so that you can start working immediately.

## How to use this repository

1. Install [R](https://cran.r-project.org/) and [RStudio.](https://posit.co/download/rstudio-desktop/)
1. Install the newest version of [Quarto](https://quarto.org/docs/download/)
2. Open the terminal in RStudio. The terminal is in the tab next to the R console pane in RStudio. Install/Update `TinyTeX` for PDFs with `quarto install tool tinytex`

1. Clone the [course environment repository](https://github.com/advanced-empirical-finance/aef_environment.git) directly in RStudio by clicking on `File/New Project` and selecting `Version Control`. Then, click `Git` and provide the repository address [https://github.com/advanced-empirical-finance/aef_environment.git](https://github.com/advanced-empirical-finance/aef_environment.git). RStudio will then automatically open the project in the new environment.

1. In the console of RStudio, install the `reticulate` R package: `install.packages("reticulate")`.
1. Use `reticulate` to install Python: `reticulate::install_python(version = "3.10.11", force = TRUE)`.
1. Tell `renv` to use Python: `renv::use_python("PATH")`.

    - `"PATH"` on Mac: `"~/.pyenv/versions/3.10.11/bin/python"`.
    - `"PATH"` on Windows: `"C:/Users/<User>/AppData/Local/r-reticulate/ r-reticulate/pyenv/pyenv-win/versions/3.10.11/python.exe"` where `<User>` is your user name.
1. Tell `renv` to install all required packages: `renv::restore()`.

Now, you are ready to execute all code found in this repository and every code chunk from this course.
Whenever you install a new package (e.g., `tidymodel`), do as you would typically do (`install.packages("tidymodels")`) and update your package management system at the end of the session by running `renv::snapshot()`. Should you share the `renv.lock` files with your peers, they must run `renv::init()` to replicate your exact package environment.

## Further content

- You find an (empty) folder, `data`. All data required to solve the exercise and assignments in this course is available in the files `tidy_finance_r.sqlite` and ` `tidy_finance_python.sqlite` on Absalon. You can download the file and include it in the data folder. That way, we have an identical folder structure, so you can run every code chunk from my slides without changing paths. It is **not** allowed to share the `sqlite` files publicly; thus, neither you nor I are allowed to push the file to a public repo.
- The folder `mandatory_assignments` contains a file `MA_template.qmd`, which you can use to understand the inner workings of `quarto` files. The file automatically generates .pdf documents, which comply with the formatting standards of this course. 
