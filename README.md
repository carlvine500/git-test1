# git引用子工程的办法

git引入其它工程示例：
git-test1 引用 git-test ，取个别名叫subtree-git-test:
```git clone https://github.com/carlvine500/git-test1.git
cd git-test1
git remote add -f remote-git-test https://github.com/carlvine500/git-test.git
git subtree add -P subtree-git-test remote-git-test master
git push 
```
此时github里subtree-git-test文件夹就是个软链接，两边修改更新都操作同一个原始存储
