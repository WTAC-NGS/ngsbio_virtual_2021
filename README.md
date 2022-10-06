# NGS Bioinformatics Virtual 2021

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)

This is the repository for the NGS Bioinformatics Virtual 2021 course.

## Cloning the repository
To checkout a repository made up of submodules please use

git clone https://github.com/WTAC-NGS/ngsbio_virtual_2021 --recursive

## Adding modules to the course respository as submodules
To add a submodule to the repository use

   `git submodule add https://github.com/WTAC-NGS/igv`

By default, the submodule will be added into a directory named the same as the repository i.e. igv

To use a different directory name for example module_igv use

   `git submodule add https://github.com/WTAC-NGS/igv module_igv`

This will create a new folder named igv/module_igv which contains a full clone of the source repository and a new .gitmodules file. 

The .gitmodules configuration file stores the mapping between the project’s URL and the local subdirectory you’ve pulled it into:

     `[submodule "igv"]`
      
      `path = igv`
      
      `url = https://github.com/WTAC-NGS/igv`

By default this new submodule will be tracking HEAD of the master branch. If you want your submodule to point to a specific tagged release use

  `cd igv`
  
  `git checkout ngs_2020`
  
  `cd ..`

Then you will need to commit the changes and push them

   `git add .`
   
   `git commit -m "Added submodule igv"`
   
   `git push origin main`
