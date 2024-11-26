# Minimal Tool Template in Quarto with R and System Requirements

[`index.qmd`](index.qmd)  contains the sample structure for the Kodaqs_Toobox, it illustrates all the **required** metadata used by [`andrew`](https://github.com/GESIS-Methods-Hub/andrew).

[`quarto_features.qmd`](quarto_features.qmd) shows how to use code junks and other features.

This repository uses [`install.R`](install.R) and [`apt.txt`](apt.txt) as [configuration file](https://mybinder.readthedocs.io/en/latest/using/config_files.html).
[`apt.txt`](apt.txt) is required because of the system requirements of the [units R package](https://cran.r-project.org/web/packages/units/index.html).
Without the [`apt.txt`](apt.txt), the rendering of [`index.qmd`](index.qmd) will raise a error similar to

```
Quitting from lines 31-38 (index.qmd) 
Error: package or namespace load failed for 'units' in dyn.load(file, DLLpath = DLLpath, ...):
 unable to load shared object '/srv/rlibs/units/libs/units.so':
  libudunits2.so.0: cannot open shared object file: No such file or directory
In addition: Warning message:
In do_once((if (is_R_CMD_check()) stop else warning)("The function xfun::isFALSE() will be deprecated in the future. Please ",  :
  The function xfun::isFALSE() will be deprecated in the future. Please consider using base::isFALSE(x) or identical(x, FALSE) instead.

Execution halted
```

## Metadata

| Markdown YAML front matter key | Required | Note |
| --- | --- | --- |
| title | ‼️ | |
| subtitle | | |
| author | ‼️ | |
| image | | Preferable as 900×600 pixels. |
| image-alt | | |

Please note that the citation field is not supported as metadata. Instead a [CITATION.cff](https://citation-file-format.github.io/) file should be used

## Supported Features

| Feature                                                                   | [`andrew`](https://github.com/GESIS-Methods-Hub/andrew) | Notes                                                                       |
|---------------------------------------------------------------------------|---------------------------------------------------------|-----------------------------------------------------------------------------|
| [Pandoc’s Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)      | 👍                                                      |                                                                             |
| Images                                                                    | 👍                                                      | As part of Pandoc’s Markdown                                                |
| Tables                                                                    | 👍                                                      | As part of Pandoc’s Markdown                                                |
| Citations and Bibliographies                                              | 👍                                                      | As part of Pandoc’s Markdown                                                |
| Footnotes                                                                 | 👍                                                      | As part of Pandoc’s Markdown                                                |
| Math                                                                      | 👍                                                      | Powered by [MathJax](https://www.mathjax.org/) as part of Pandoc’s Markdown |
| Callout Blocks                                                            | 😥                                                      | See https://github.com/GESIS-Methods-Hub/andrew/issues/149                  |
| HTML Features                                                             | 😥                                                      | We want to render to pdf, so pure quarto is required                        |
| Citation Metadata                                                             | 😥                                                      | See https://github.com/GESIS-Methods-Hub/andrew/issues/220                        |
| Cross References                                                          | 👍                                                      |                                                                             |
| Computation of [Inline Code](https://rmarkdown.rstudio.com/lesson-4.html) | 👍                                                      |                                                                             |
| Computation of [Code Chunks](https://rmarkdown.rstudio.com/lesson-3.html) | 👍                                                      |                                                                             |
| [Code Annotation](https://quarto.org/docs/authoring/code-annotation.html) | 👍                                                      | Requires Quarto >= 1.3                                                      |
| [Title Blocks](https://quarto.org/docs/authoring/title-blocks.html)       | 👍                                                      | Generated by Quarto based on YAML header                                    |
| How to cite in the appendix                                               | 👍                                                      | Generated by Quarto based on YAML header                                    |

## Binder

The link to Binder will launch [RStudio IDE](https://posit.co/products/open-source/rstudio-server/).
