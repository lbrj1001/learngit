本文章是学习廖雪峰git教程的命令总结：
廖雪峰git教程地址：https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

初始化一个Git仓库，使用git init命令。
添加文件到Git仓库，分两步：
    1、使用命令git add <file>，注意，可反复多次使用，添加多个文件；
    2、使用命令git commit -m <message>，完成。
要随时掌握工作区的状态，使用git status命令。
如果git status告诉你有文件被修改过，用git diff可以查看修改内容。



HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

ssh-keygen -t rsa -C "youremail@example.com"  生成秘钥给远程仓库使用
git clone git@github.com:michaelliao/gitskills.git

第一次和远程空仓库关联 git remote add origin git@github.com:michaelliao/learngit.git
第一次提交并且关联分支：git push -u origin master
之后的提交：git push origin master