# 分支相关

实际小组项目中，每个人从 main 拉一个分支。

## 查看分支结构

```bash
git log --oneline --graph --all
```

## 创建分支

更新并对齐 origin/main

```bash
git fetch origin
git switch main
git pull --rebase origin main
```

创建一个分支

```bash
git switch -c <feature-branch>
```

推送到 GitHub：

```bash
git push -u origin <feature-branch>
```

## 切换到某个历史版本查看

使用版本号

```bash
git checkout <commit-id>
```

看完历史版本后回到主分支

```bash
git switch main
```

## PR 规范流程

确认当前分支

```bash
git switch <feature-branch>
git branch
```

抓取 GitHub 上最新的 main（这一步不会改你的代码，只是更新本地记录里的 origin/main）

```bash
git fetch origin
```

把最新 main 合并进你的 feature 分支

```bash
git merge origin/main
```

处理冲突，然后

```bash
git add .
git commit -m "..."
git push origin <feature-branch>
```

去 GitHub 提交 PR，填写标题 & 描述

```
feat: ...
```

合并到 main 后记得 pull
