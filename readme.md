
# GIT 使用

工作区 - 暂存区 - 本地仓库

1. 在电脑上创建一个文件夹作为工作区
2. 打开文件夹右键 git base here 进入当前目录
3. 工作区持有项目的实际文件
4. 暂存区和本地仓库，不需要我们操作

## readme 文档
1. readme文件可以是txt文档，也可以是md文档
2. 一般和项目放在一起，作为项目的说明文档

## 全局配置
1. 配置用户名： git  config --global user.name "github用户名"
2. 配置用户邮箱： git config --global user.email "github验证邮箱"
3. 一台电脑配置一次就行
4. 查看配置信息 git config --list

## 初始化
1. 命令 git init 初始化版本库
2. 单钱目录路劲有（master）代表初始化成功
3. 在当前目录下会生成一个隐藏文件 .git 代表这是一个版本库
4. 千万别操作 .git文件

## 工作区内容提交到本地仓库
1. 执行命令 git add 文件名 将工作区的内容提交到暂存区
2. 命令 git add . 将所有变动（新增、修改、删除）提交到暂存区
3. 从暂存区提交到本地仓库 git commit -m "提交注释"

## 版本回退
1. git reset --hard HEAD^ 回退到上一个版本（一个^表示上一个版本）
2. git reset --hard 版本号的哈希值   回退到指定的版本

## 辅助命令
1. 命令 git status 查看当前目录下的操作状态
2.  git log 查看日志
3. git reflog 查看简版日志

## 将本地仓库提交到远程仓库
1. 在github创建一个远程仓库 git2010
2. 本地工作区先提交到本地仓库
3. git remote add origin 远程仓库地址 本地仓库和远程仓库关联
4. git remote -v 查看本地仓库关联的远程仓库
5. git push -u origin master 第一次执行
    git push 把本地仓库推送到远程仓库
    -u origin master 设置默认提交master分支到origin
6. git push -u -f origin master 强制推送到远程，不推荐！！