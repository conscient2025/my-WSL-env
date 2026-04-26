把已经被跟踪的文件/目录从索引中移除：

```bash
git rm -r --cached <dir/file>
```

查看代码差异

```bash
git diff
```

查看提交历史

```bash
git log --oneline
```

查看分支结构

```bash
git log --oneline --graph --all
```

更新并对齐 origin/main

```bash
git fetch origin
git switch main
git pull --rebase origin main
```