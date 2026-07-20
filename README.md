## iterative Random Forests (iRF)

The R package `iRF` implements iterative Random Forests, a method for
iteratively growing ensemble of weighted decision trees, and detecting
high-order feature interactions by analyzing feature usage on decision paths.
This version uses source codes from the R package `randomForest` by Andy Liaw
and Matthew Weiner and the original Fortran codes by Leo Breiman and Adele
Cutler.

### versions
| | github/website | owner | language | installation | note |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **iRF** | [karlkumbier/iRF](https://github.com/karlkumbier/iRF) | karlkumbier | R | `devtools::install_github("karlkumbier/iRF")` ||
| **iRF2.0** | [sumbose/iRF: iterative](https://github.com/sumbose/iRF) | sumbose | R | `devtools::install_github("karlkumbier/iRF2.0")` | from the instruction, it's installed from karlkumbier/iRF2.0 which is redirected to karlkumbier/iRF; <br>️ <mark>no plotInt()</mark> |
| **iRF3.0** | [sumbose/iRF: Iterative](https://rdrr.io/github/sumbose/iRF/) | sumbose | R | `remotes::install_github("sumbose/iRF")` | installed from the repository； has plotInt() |
| **iRF** | [Yu Bin](https://binyu.stat.berkeley.edu/)<br>[Yu-Group/iterative-Random-Forest](https://github.com/Yu-Group/iterative-Random-Forest) | Yu-Group | Python | pip install | before installation, rename readme.md to <mark>README.md</mark> due to Ln12 in setup.py |

