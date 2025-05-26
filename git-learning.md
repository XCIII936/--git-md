# 完整 Git 命令手册

## 1. 基础配置
```
git config --global user.name "lms"
git config --global user.email "lms3082@outlook.com"
git config --list  # 查看所有配置
```

## 2. 仓库操作
```
git init  # 初始化新仓库
git clone git@github.com:user/repo.git  # 克隆仓库(SSH)
git clone https://github.com/user/repo.git  # 克隆仓库(HTTPS)
```
## 3. 文件管理

```
git status  # 查看状态
git add .  # 添加所有修改
git add file.txt  # 添加特定文件
git restore file.txt  # 放弃工作区修改
git commit -m "message"  # 提交更改
```
## 4. 分支管理

```
git branch  # 查看分支
git branch new-feature  # 创建分支
git checkout main  # 切换分支
git merge feature  # 合并分支
git branch -d old-feature  # 删除分支
```
## 5.远程操作
```
git remote add origin git@github.com:user/repo.git  # 添加远程(SSH)
git push -u origin main  # 首次推送
git pull  # 拉取远程更新
git fetch  # 获取远程变更不合并
git remote set-url origin git@github.com:你的用户名/新仓库名.git #更换远程仓库
git remote -v #验证是否修改成功
```
## 6.历史查看
```
git log  # 查看提交历史
git log --oneline --graph  # 简洁图形化历史
git diff  # 查看工作区修改
git diff --staged  # 查看暂存区修改
```
## 7.SSH配置
```
ssh-keygen -t rsa -b 4096 -C "your.email@example.com"  # 生成SSH密钥
cat ~/.ssh/id_rsa.pub  # 查看公钥(复制到GitHub)
ssh -T git@github.com  # 测试SSH连接
```