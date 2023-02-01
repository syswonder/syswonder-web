# 如何用git协作

假定:

- 你的github账号为 panda

- 要贡献的代码库为 https://github.com/syswonder/syswonder-web.git

**1. Fork repo**

在浏览器中打开 https://github.com/syswonder/syswonder-web

点击右上角的"Fork" 按钮

**2. Clone repo**

从Fork得到的个人空间 repo 中 clone到本地

```
git clone https://github.com/panda/syswonder-web
```

!> 请记得将panda替换为您自己的用户名


```
# 设置 upstream
git remote add upstream https://github.com/syswonder/syswonder-web.git
# 禁止直接向 upstream 推送代码
git remote set-url --push upstream no_push
```

**3. work, commit & push**

为本次工作创建一个分支，命名为 `dev`

```
git checkout -b dev
```

此时就可以在该分支下工作了, 不断修改代码，不断 commit

```
git add .

git commit -m "your commit message"
```

如果经过测试，觉得在本地完成了代码工作，就可以将代码推送到自己的服
务器端的仓库中了。

```
git push origin develop
```

push到自己的服务器端库中后，就可以准备创建`合并请求(Pull Request)`了。

**4. pull request**

同步upstream

```
git fetch upstream
git merge upstream/main
```

此时请确保本地位于工作分支。如果合并过程有冲突，要负责解决冲突，并提交。

将消解了冲突的最新本地代码，推送到个人服务器端仓库的dev分支。

```
git push origin dev
```

到自己个人服务器端仓库的首页, 准备 **Pull Request** , 

base repo 选择 syswonder/syswonder-web main

head repo 选择 panda/syswonder-web dev

提交即可。

**5. sync origin main**

```
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```
