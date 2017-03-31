# git引用子工程的办法
git引入其它工程示例：
git-test1 引用 git-test
```
 git submodule add https://github.com/carlvine500/git-test.git subtree-git-test
//之后所有子模块修改执行：
 git submodule update --recursive --remote

```

另一种方法采用subtree比较麻烦：
 ，取个别名叫subtree-git-test:
```git clone https://github.com/carlvine500/git-test1.git
cd git-test1
git remote add -f remote-git-test https://github.com/carlvine500/git-test.git
git subtree add -P subtree-git-test remote-git-test master
git push 
```

