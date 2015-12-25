# 
HeadHunterSchool homework: 1. Git, task #2
---------

##### 1. Репозиторий, содержащий только frontik/testing
```
git clone https://github.com/hhru/frontik hh_git_2_include
cd hh_git_2_include/
git filter-branch --prune-empty --subdirectory-filter frontik/testing master
git remote set-url origin https://github.com/Iskuskov/hh_git_2_include
git push origin --all
cd ..
```

##### 2. Репозиторий, содержащий все, кроме frontik/testing
```
git clone https://github.com/hhru/frontik hh_git_2_exclude
cd hh_git_2_exclude/
git filter-branch --tree-filter "rm -rf frontik/testing" --prune-empty HEAD
git remote set-url origin https://github.com/Iskuskov/hh_git_2_exclude
git push origin --all
cd ..
```
