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

如果报错 the remote contains work that you do not hint: have locally，执行

```bash
git pull --no-rebase origin main --allow-unrelated-histories
```

先看

```bash
git status
```

修改冲突文件，接着执行

```bash
git add .
git commit -m "..."
git push -u origin main
```

之后就可以直接使用

```bash
git pull
git push
```
