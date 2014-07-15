comt_2
==============

This is the directory of ncml and metadata documents for the 2nd IOOS Coastal Ocean Modeling Testbed (COMT1).  These NcML files are used to turn collections of model output netCDF files into CF and UGRID compliant aggregated datasets.   The NcML in this repo may be useful for others who wish to see how to handle collections of ADCIRC, SELFE or FVCOM output files. 

This repo was using this recipe:
* create an empty repo on the ioos github called `comt_2` using the github web interface 
* Log into `comt.sura.org` as user `testbed`
* Change directory to the head of the testbed 2 data and create a gitignore prior to adding files:

```
cd /data/comt_2
git init
vi .gitignore
```
with the .gitignore file set to ignore all files except subdirectories and files with .ncml,.doc,.docx and .csv:
```
more .gitignore
*
!*/
!*.ncml
!*.doc
!*.docx
!*.csv
!README.txt
```
* add, commit and push to github:
```
git add .
git commit -m 'added ncml,doc and csv files from dirs'
git remote add origin git@github.com:ioos/comt_2.git
git push --set-upstream origin master
```
I also did this to allow easy rollback of last commit:
```
git config --global alias.undo-commit 'reset --soft HEAD^' 
```
Then just type 
```
git undo-commit
```
as needed. 
