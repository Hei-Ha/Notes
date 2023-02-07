## git 常用命令

### 合并commit 为一个
```js
// 合并指定版本号（不包含此版本）
git rebase -i [commitid]

:%s/pick/s/g 全局替换 pick 为 s
```

### 拉取远程分支到本地
```js
git checkout -b 本地新建的分支名 origin/远程分支名
```