# git使用





### 下载git

> https://git-scm.com/ 官网地址

### 初始化 git 仓库

```scss
git init
```

### 本地与github连接

1. 创建一个github账号

2. 本地配置邮箱和用户名

   ```css
   git config --global user.name "用户名"
   git config --global user.email "邮箱号"
   ```

3. 生成ssh key

   ```css
   ssh-keygen -t rsa -C "邮箱号"
    clip < ~/c/User/EDZ/.ssh/id_rsa.pub  //复制刚才生成的ssh key
   ```

4. 回到GitHub 

   > settings --> SSH and GPG keys --> new SSH key  --> 填写title和key值就可以了

5. 连接github仓库

   >git remote add origin 仓库的ssh 地址

6. 首次提交必须进行过一次提交

   > git push --set-upstream origin master





## 代码提交

#### 本地提交到 - > 暂存区域

```csharp
git add 文件名字  //提交单个文件
git add . //提交暂存区所有内容
```

#### 暂存区域提交到 --> 历史记录区

```csharp
git commit -m "描述信息"
```

#### 历史记录区提交 --> 到github上

```csharp
git push
```

#### 查看仓库状态

```csharp
git status
```

#### 查看上一个版本和当前版本的不同

```csharp
git diff
```

#### 查看提交记录

```csharp
git log
git reflog //查看head变更记录
```

#### 回退到上一次commit的版本

```csharp
git checkout -- .
```

#### 版本回退

```csharp
git reset --hard 版本号
```

#### 拉代码

```csharp
git clone 仓库的ssh
```

