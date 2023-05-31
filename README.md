# Minimal Example of Tutorial in Quarto with R and System Requirements

[`index.qmd`](index.qmd) show all the **required** metadata used by Methods Hub.

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