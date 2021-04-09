# git命令

### 1.主分支提交代码

```cmd
git clone xxx 克隆项目
cd xxx 进入项目
git add . 添加代码
git commit -m 'xx' 提交代码
git push 推送代码
```

### 2.其他分支合并代码到主分支上

```cmd
git branch 查看分支
git branch xx 创建分支名字
git push --set-upstream origin xx  推到远程github上面
git checkout xx 切换分支
git add . 添加代码
git commit -m 'xx' 提交代码
git checkout master 切回到主分支
git merge xx 把分支代码合并到主分支
git push 推送代码
```

### 3.git其他命令

```cmd
git status 查看状态
git log 查看日志
// 代码拉去流程
1.先获取代码
2.提交代码之前，先更新本地代码，并提交
git clone xxx
git pull origin xxx 更新的项目分支名字
其2一样的操作命令

电脑配置：ssh-key不用输入账号和密码
```
