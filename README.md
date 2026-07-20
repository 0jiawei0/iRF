## iterative Random Forests (iRF)

The R package `iRF` implements iterative Random Forests, a method for
iteratively growing ensemble of weighted decision trees, and detecting
high-order feature interactions by analyzing feature usage on decision paths.
This version uses source codes from the R package `randomForest` by Andy Liaw
and Matthew Weiner and the original Fortran codes by Leo Breiman and Adele
Cutler.

### versions
| | github/website | language | installation | note |
| :--- | :--- | :--- | :--- | :--- |
| **iRF** | [karlkumbier/iRF](https://github.com/karlkumbier/iRF) |R | `devtools::install_github("karlkumbier/iRF")` ||
| **iRF2.0** | [sumbose/iRF: iterative](https://github.com/sumbose/iRF) | R | `devtools::install_github("karlkumbier/iRF2.0")` | from the instruction, it's installed from karlkumbier/iRF2.0 which is redirected to karlkumbier/iRF; <br>️ <mark>no plotInt()</mark> |
| **iRF3.0** | [sumbose/iRF: Iterative](https://rdrr.io/github/sumbose/iRF/) | R | `remotes::install_github("sumbose/iRF")` | installed from the repository； has plotInt() |
| **iRF** | [Yu Bin](https://binyu.stat.berkeley.edu/)<br>[Yu-Group/iterative-Random-Forest](https://github.com/Yu-Group/iterative-Random-Forest) | Python | pip install | before installation, rename readme.md to <mark>README.md</mark> due to Ln12 in setup.py |

### note
This repository is forked from `sumbose/iRF` by adding missing R headers in [classTree.c](src/classTree.c), [regTree.c](src/regTree.c), and [rfutils.c](src/rfutils.c) to resolve fatal compilation errors (`implicit declaration of function`) when compiling on Windows.

> 🛑 **Windows & Rtools Compatibility Notice (R 4.5+):**
> Modern C standards enforcement in newer compiler toolchains causes the original repository to fail during installation on Windows. 
> * **For R 4.5:** The required **Rtools45** utilizes GCC 14, which strictly blocks compilation due to these missing implicit declarations.
> * **For R 4.6+:** Since there is currently no Rtools46 available for the upcoming R 4.6 generation, and future Rtools versions will enforce even stricter compilation standards, the original `iRF` repository may remain <mark>**uninstallable on Windows**</mark> without these header fixes.
