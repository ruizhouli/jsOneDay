### git 与 github

> git 版本控制工具

    SVN：集中式 弊端：版本控制必须要网络支持 一般SVN都是局域网，只能是公司内部人员使用；外部人员很难使用；但是中央服务器不一定稳定

    git为分布式   不需要网络支持 就能进行版本控制，只要能上网还有开发权限都能参与开发 就算远程仓库出事，本地计算机也有历史记录。

    GITHUB:程序员交友网站 远程仓库 帮助学习

>GIT的三大区域：
-  工作区(本地)

-  暂存区(保护工作区和版本区)

-  版本区(版本库、历史记录)  只有形成版本才能进行版本控制

形成版本
- git  git config --global  user.name "ruizhouli" 

- 创建版本仓库：git init (想控制哪个)

- 查看状态 git status 

- 工作区到暂存区
   -git add 文件名
   -git add . (快速把工作区所有的文件放到暂存区)

- 暂存区到版本区
    -git commit -m "取个自己能够识别的名字"

- 查看版本 
    - git log
    - git reflog 查看多有的历史记录（包括历史区回滚）

- 回滚
     - git reset --hard commit码

- 快速从工作区到版本区
    - git commit -a -m "版本名"

- 过滤不需要上传的文件
  -touch .gitignore  在gitignore文件中写要过滤的

- 查看各大区域之间的区别
   - 工作区和暂存区 git diff
   - 工作区和版本区 git diff master
   - 暂存区和版本区 git diff --cached
- 上传github
    设置秘钥：SSH-keygen -t rsa -C "邮箱" 
