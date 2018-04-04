https://learngitbranching.js.org
# Git基础语法
## 主要
### 基础篇
* git commit  
提交
* git branch A  
创建名为A的branch
* git checkout A   
切换到新分支A上
* git checkout -b A   
创建并切换至A分支上
* git merge A  
将A分支合并至master分支上（当前所在分支为master）
* git rebase master  
将bugFix分支（当前所在分支）移至master分支  
### 高级篇
* git checkout C4  
将HEAD指向哈希值为C4的版本
* git checkout A^  
将HEAD指向A分支倒数第二个版本
* git checkout HEAD~3  
将HEAD标记至A分支上面的第三个版本
* git branch -f A HEAD~3  
将分支A强制指向HEAD的第3级父提交
* git branch -f A C6  
将分支A强制指向C6版本
* git reset HEAD^  
向上移动分支，并撤销最后一次提交
* git revert HEAD  
再次提交，生成HEAD‘版本，内容同HEAD^ 版本一致  
* git branch -f branchname HEAD^  
切换分支至branchname的上一个版本  
* git branch -f master C4'  
切换master分支至C4‘版本  
### 移动提交记录
* git cherry-pick <提交号>...  
将部分选中提交复制到当前所在位置下
* git rebase -i HEAD~4  
将HEAD之前的连续4（包括HEAD）个版本再次排序  
### 杂项
* git commit --amend  
修改branch上最顶端的commit
* git tag v1 C1  
为C1版本贴标签v1  
* git describe  
用来描述离你最近的锚点（标签）  
* git checkout master^2  
将HEAD指向master的非直系父节点  
## 远程
### Git远程仓库
### Git远程仓库高级操作
* git clone  
在远程仓库建立本地仓库的副本  
* o/master（origin）  
远程分支，自动分离HEAD  
* git fetch  
从远程仓库中下载本地仓库中缺失的提交记录  
更新远程分支指针（o/master）  
使用http或git协议与远程残酷通信  
不会更新本地仓库的状态  
不会更新你的master分支  
不会修改你磁盘上的文件
* git pull  
等于git fetch 和git merge o/master两部操作  
* git fakeTeamwork 
默认操作为在远程分支上做一次提交
* git fakeTeamwork foo 3  
指定在foo分支上做了3次提交  
* git push  
将你的变更上传到指定的远程仓库
* git pull --rebase  
是fetch和rebase的简写
* git push <remote> <place>    
切到本地仓库中的<place>分支，获取所有的提交，再到远程仓库<remote>中找到<place>分支，将远程仓库中没有的提交记录都添加上去  
* git push origin <source>:<destination>  
本地的<source>分支推送到远程仓库中的<destination>分支  
* git fetch origin foo  
Git 会到远程仓库的 foo 分支上，然后获取所有本地不存在的提交，放到本地的 o/foo 上  
* git push origin :bar  
删除o/bar分支  
* git fetch origin :bar  
新建bar分支  
* git pull origin master:foo  
在本地创建了一个叫 foo 的分支，从远程仓库中的 master 分支中下载提交记录，并合并到 foo，然后再 merge 到我们的当前检出的分支 bar 上  

## 实用篇  
### 仓库初始化  
> echo "# group" >> README.md  
> git init  
> git add README.md  
> git commit -m "first commit"  
> git remote add origin git@github.com:CandyLee0201/group.git  
> git push -u origin master    

### 提交
> git diff README.md  
> git add README.md  
> git status  
> git commit -m 'text'  
> git push  



