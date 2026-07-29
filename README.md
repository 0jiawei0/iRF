## iterative Random Forests (iRF)

The R package `iRF` implements iterative Random Forests, a method for
iteratively growing ensemble of weighted decision trees, and detecting
high-order feature interactions by analyzing feature usage on decision paths.
This version uses source codes from the R package `randomForest` by Andy Liaw
and Matthew Weiner and the original Fortran codes by Leo Breiman and Adele
Cutler.

### installation
To download and install the package, use `remotes`
```r
install.packages("remotes")
remotes::install_github("0jiawei0/iRF")
```

### versions
| | github/website | language | installation | note |
| :--- | :--- | :--- | :--- | :--- |
| **iRF** | [karlkumbier/iRF](https://github.com/karlkumbier/iRF) |R | `devtools::install_github("karlkumbier/iRF")` ||
| **iRF2.0** | [sumbose/iRF: iterative](https://github.com/sumbose/iRF) | R | `devtools::install_github("karlkumbier/iRF2.0")` | from the instruction, it's installed from karlkumbier/iRF2.0 which is redirected to karlkumbier/iRF; <br>️ <mark>no plotInt()</mark> |
| **iRF3.0** | [sumbose/iRF: Iterative](https://rdrr.io/github/sumbose/iRF/) | R | `remotes::install_github("sumbose/iRF")` | installed from the repository； has plotInt() |
| **iRF** | [Yu Bin](https://binyu.stat.berkeley.edu/)<br>[Yu-Group/iterative-Random-Forest](https://github.com/Yu-Group/iterative-Random-Forest) | Python | pip install | before installation, rename readme.md to <mark>README.md</mark> due to Ln12 in setup.py |

### note
This repository is forked from `sumbose/iRF` by adding missing R headers in [classTree.c](src/classTree.c), [regTree.c](src/regTree.c), and [rfutils.c](src/rfutils.c) to resolve fatal compilation errors (`implicit declaration of function`) when compiling on Windows.

> 🛑 **Windows & Rtools45 Compatibility Notice (R 4.5 & R 4.6+):**
> According to the official CRAN [documentation](https://cran.r-project.org/bin/windows/base/howto-R-4.6.html), both **R 4.5** and the upcoming **R 4.6** generations utilize the **Rtools45** compiler toolchain on Windows.
> 
> Because Rtools45 introduces **GCC 14**, which strictly blocks compilation whenever implicit function declarations are present, the original `sumbose/iRF` repository is <mark>**uninstallable on modern Windows R environments**</mark>. 
> 
> This fork patches the standard R macros directly to guarantee seamless compilation and long-term forward compatibility for Windows R users.
