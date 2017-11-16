# my-gitflow
git flow deep study

##Git Flow代码示例
###a.创建develop分支
```shell
git branch develop
git push -u origin develop
```

###b.开始新Feature开发
```shell
git checkout -b new-feature develop
# Optionally, push branch to origin:
git push -u origin new-feature   
# 做一些改动   
git status
git add some­file
git commit
```
###c.完成Feature
```shell
git pull origin develop
git checkout develop
git merge --no-ff new-feature
git push origin develop
git branch -d new-feature
# If you pushed branch to origin:
git push origin --delete new-feature 
```

###d.开始Release
```shell
git checkout -b release-0.1.0 develop
# Optional: Bump version number, commit
# Prepare release, commit 
```

###e.完成Release
```shell
git checkout master
git merge --no-ff release-0.1.0
git push
git checkout develop
git merge --no-ff release-0.1.0
git push
git branch -d release-0.1.0
# If you pushed branch to origin:
git push origin --delete release-0.1.0  
git tag -a v0.1.0 master
git push --tags
```

###f.开始Hotfix
```shell
git checkout -b hotfix-0.1.1 master 
```

###g.完成Hotfix
```shell
git checkout master
git merge --no-ff hotfix-0.1.1
git push
git checkout develop
git merge --no-ff hotfix-0.1.1
git push
git branch -d hotfix-0.1.1
git tag -a v0.1.1 master
git push --tags 
```
  
