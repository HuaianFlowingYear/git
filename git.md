# git

git init 目录->仓库

 \* 1、新入库的文件

 \* (u未跟踪的) ——> git add <filename>  （filename——>文件名或通配符（.））——>A(已添加索引)

 \* 2、对新入库且已添加完索引的文件再次修改

 \* A(已添加索引) ——> M(已修改)

 \* 3、保存版本（仓库内所以文件当时的状态）快照 [UAM都会消失，表示现在在稳定的状态]

 \* git commit -m <版本的快照描述> (前提条件：所有文件是A)

 \* 后续的工作 

 \* 1、对上一次"备份"好的文件更新/修改

 \* commit(备份)——> M(绿色:再次修改文件) ——> M(黄色:在次修改索引) ——> commit(备份1) （对已经备份好的文件进行二次修改再备份） 

 \* 2、新增文件备份

 \*  U ——> A ——> commit 



PS D:\软件位置\Pictures\学习\12月学习\code\git> git add .
fatal: not a git repository (or any of the parent directories): .git

不是git仓库（这是致命错误），我们得使用git init 初始化一下，一个仓库

文件后有U 代表被跟踪

使用git add . 后，这是添加进仓库内了，所以文件后变成了A  

.gitignore  git的配置文件（专门写忽略文件），也就是可以在里面写需要忽略的文件

在以后这个代码的状态就是我想退回来的状态就是要 git commit（重要的节点）

git log 查看你备份的版本

git checkout 加上 6位数以上的commit 的id 就可以切换到你想要的版本

git reset HEAD（当前的版本） 当前的上一个版本 HEAD^  当前的一百个版本 HEAD^~~100    --soft 回撤

默认参数 mast     git reset HEAD^

git reset HEAD^ --hard   回退到上一个版本

新建分支  git branch feat-4

git merge feat-4  没有分歧的时候，合并分支



git branch -d feat-4   删除分支

git branch -D feat-4 彻底删除分支

git checkout -b feat_4  创建这个分支并进入这个分支 