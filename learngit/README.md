## 教你如何使用git -_-

### 几个命令：

  * **ls** 显示当前文件夹
  * **cd** 进入文件夹
  * **touch** 新建文件夹
  * **git init** 添加到仓库
  * **git add -A** 把当前文件夹所有文件添加到暂存区 -A代表所有文件
  * **git status**  查看当前状态
  * **git commi**t 是把暂存区的文件提交到本地仓库，后面最好跟一个-m ""  来说明版本变更原因
  * **git log** 是查看提交历史
  * **git reflog** 可以查看命令历史
  * **git reset --hard HEAD^** 版本回退
  * **git reset --hard 3628164** 撤销回退，后面那个是版本ID

  * **git checkout -- filename** 是撤销一次修改或者退回上一个状态。可以把添加到暂存区的给弄出来
  * **git checkout** 其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

  * **git rm** 删除一个文件


###几个名词：

  * 工作区：是你电脑上的目录，你可以看到它。
  * 暂存区：隐藏在.git里面，git add到这个里面叫暂存区。
###注意：
   **git commit只提交暂存区的文件**

   在GitHub官网上新建一个仓库。并且复制最下面的两行 

   * 来为仓库添加远程地址。
   * 将本地资源推送到远程服务器上。

   之后本地再做了git commit 提交之后就 直接 git push origin master 



###几个坑：

  * 在执行 **$ git remote addorigin git@github.com:defnngj/hello-world.git** 时

  	出现错误提示：*fatal: remote origin already exists.*

  	解决办法：**$ git remote rm origin**
	
	然后再执行：$ git remote add origin git@github.com:defnngj/hello-world.git 就不会报错误了

 

  * 在执行 **$ git push origin master** 时
  
	出现错误提示： *error:failed to push som refs to.......*
  
	解决办法： **$ git pull origin master** // 先把远程服务器github上面的文件拉下来，再push 上去。