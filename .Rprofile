source("renv/activate.R")

# To avoid the "This probably means that Tcl wasn't installed properly." error
# that arises when rendering qmd files with R and Python code and plots in each.
# See https://github.com/rstudio/rstudio/issues/13840.
if (Sys.info()["machine"] == "x86-64") {
  user_name <- Sys.info()["user"]
  tcl_path <- paste0("C:/Users/", user_name, "/AppData/Local/r-reticulate/r-reticulate/pyenv/pyenv-win/versions/3.10.11/tcl/tcl8.6")
  Sys.setenv(TCL_LIBRARY = tcl_path)
}
