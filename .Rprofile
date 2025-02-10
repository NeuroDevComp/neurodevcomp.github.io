source("renv/activate.R")

render <- function() {
  if (dir.exists("docs")) {
    unlink("docs", recursive = TRUE, force = TRUE)
  }
  babelquarto::render_website(".")

  invisible({
    file.copy("static/fonts/", "docs/static/",
      overwrite = TRUE, recursive = TRUE,
    )
    file.copy("static/img/background.svg", "docs/static/img/",
      overwrite = TRUE, recursive = TRUE,
    )
  })
}
