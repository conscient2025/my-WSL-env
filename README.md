# my-WSL-env

创建本地仓库：

```bash
git init
git status
git add .
git commit -m "initial commit"
```

把本地仓库关联到 GitHub private 仓库：

```bash
git remote add origin git@github.com:conscient2025/<repo-name>.git
```

检查是否关联成功：

```bash
git remote -v
```

把本地分支改成 main：

```bash
git branch -M main
```

第一次推送到远程 private 仓库

```bash
git push -u origin main
```

这里 -u 很重要，它会建立本地 main 和远程 origin/main 的跟踪关系。以后你就可以直接用：

```bash
git push
git pull
```
