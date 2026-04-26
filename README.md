# WSL 环境 Git 配置

## Start from local

创建本地仓库：

```bash
git init
git status
git add .
git commit -m "initial commit"
```

把本地仓库关联到 GitHub 空仓库：

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

## Start from GitHub

在 GitHub 上 Fork

在本地 Clone 我的 Fork

```bash
git clone git@github.com:conscient2025/<repo-name>.git <dir-name>
```

添加“上游仓库”

```bash
git remote add upstream git@github.com:原作者/repo.git
git remote -v
```

当原仓库更新时同步 upstream

```bash
git fetch upstream
git rebase upstream/main
# 或 git merge upstream/main（更保守）
git push -f   # 如果用了 rebase
```

推送到我的 Fork 后可发起 PR