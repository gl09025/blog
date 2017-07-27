

# 如何建立一個沒有 Parent 的獨立 Git branch

### 方法一 ([source](http://madduck.net/blog/2007.07.11:creating-a-git-branch-without-ancestry/))

因為 git branch 預設是從 HEAD 分支，所以可以這樣 Hack HEAD：

```
echo ref: refs/heads/newbranch > .git/HEAD
git rm -rf .   # 砍掉所有檔案重來
.....   # 加新檔案
git add .
git commit -m 'create new branch'

```

### 方法二([source](https://git.wiki.kernel.org/index.php/GitTips#How_to_create_a_new_branch_that_has_no_ancestor))

Git 1.7.2 之後版本有支援 –orphan 參數：

```
git checkout --orphan newbranch
git rm -rf .    # 砍掉所有檔案重來
...  # 加新檔案
git add .
git commit -m 'create new branch'

```

### 方法三([source](http://pages.github.com/))

```
git symbolic-ref HEAD refs/heads/newbranch
rm .git/index
git clean -fdx
...  # 加新檔案
git add .
git commit -m 'create new branch'
```