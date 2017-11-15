# my-gitflow
git flow deep study

a. 创建develop分支

git branch develop
git push -u origin develop    
b. 开始新Feature开发

git checkout -b some-feature develop
# Optionally, push branch to origin:
git push -u origin some-feature    

# 做一些改动    
git status
git add some-file
git commit    
