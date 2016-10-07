
```
git辅助插件:
http://folioformac.com/
```
**osx使用git**

```
廖雪峰git官网：
http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013744142037508cf42e51debf49668810645e02887691000

git config --global user.name "Your Name"
 git config --global user.email "email@example.com"
ssh -T git@github.com 是否连上 github
mkdir 创建目录
psd  显示目录信息
cd   进入目录
open 打开文件夹
git init  把这个目录变成git的仓库
git add   告诉git 把文件添加到参考
git commit  告诉git 把文件提交到参考 加-m “” 本次提交说明 便于维护
git status  查看仓库当前状态
git diff    查看不同 
git log    显示最近到最远的提交日志 --pretty=oneline 查看具体版本信息
git reset  git中用head表示版本 git reset --hard HEAD~100 
git reflog  记录每一次版本命令 回到那个版本都ok
git reset --hard XXXX回到指定版本
git checkout -- readme.txt 丢弃工作区修改
git reset HEAD readme.txt 暂存区的修改撤销掉
rm 把没用的文件删除掉
git checkout --test.txt 恢复提交区删除文件
git clone git@github.com:mark--young/Testgit.git 克隆仓库到本地

git branch 查看分支
git branch <name> 创建分支
git checkout <name> 切换分支
git checkout -b <name> 创建+切换分支
git merge< name> 合并某分支到当前分支
git branch -d <name> 删除分支
pull：远程到本地
push:本地 到远程

git remote add origin git@server-name:path/repo-name.git；要关联一个远程库，使用命令

git push -u origin master第一次推送master分支的所有内容；

git push origin master 推送最新修改；

```
**git工作原理**
git add 实际上就是要把要提交的所有修改fang'dao放到暂存区（Stage），然后执行git commit 就可以一次把暂存区的所有修改提交到分支。


![image](http://note.youdao.com/yws/public/resource/f2b6bcbdc61af782b9239e4a1f8f902e/10CF5ACAD182461AA31D0FE0C90A1BFE)



**删除项目**
在工程页面 点击设置  最下面 delete  输入工程名 确认删除