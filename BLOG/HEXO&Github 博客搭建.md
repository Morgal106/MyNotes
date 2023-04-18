---
title : HEXO&Github博客搭建
tags : [ HEXO , Github , BLOG ]
---

## 1 安装所需环境Node.js&Git&HEXO

访问[Node.js (nodejs.org)](https://nodejs.org/en/)下载并安装 Node.js ，访问[Git (git-scm.com)](https://git-scm.com/)下载并安装Git 。
打开终端，检查是否安装成功

```bash
node -v
npm -v
git -v
```

若返回版本号，则安装成功。

安装HEXO

```bash
npm install hexo -g
```
同样，使用
```bash
hexo -v
```
检查是否安装成功，若返回版本号，则安装成功。

## 2 新建 GitHub 仓库

1. 打开[GitHub](https://github.com/)，可使用[Watt Toolkit(Steam++)](https://steampp.net/)进行加速
2. 新建仓库，仓库名称为`XXX.github.io`其中`XXX`必须为 Github 用户名

## 3 生成 SSH keys

1. 打开终端，检查 SSH 版本

```bash
ssh
```

2. 生成 SSH key

```bash
ssh-keygen -t rsa -C "EMAIL"
```

命令中 `EMAIL` 替换为 GitHub 的 EMAIL，输入命令后一直按回车直到结束

3. 打开`C:\USERS\[用户名]\.ssh\id_rsa.pub`，复制其中内容
4. 打开 Github，点击右上角头像，点击 Settings，找到 `SSH and GPG keys`，点击 `New SSH key`，key type 选择 `Authentication Keys`，将第三步复制的内容粘贴到 key 文本框中，点击 Add SSH key 。

## 4 本地生成博客

1. hexo 初始化，在选定的博客文件夹中打开终端，执行如下命令，此命令将 GitHub 上的 hexo 库 clone 到本地，若出现 `access "https://github.com/...." fialed` 错误，百度 GitHub 镜像。

```bash
hexo init
```

2. 生成 hexo 初始博客

```bash
hexo g
```

3. 部署本地服务器，本步骤可跳过。

```bash
hexo s
```

## 5 发布博客到网络
1. 安装 `hexo-deployer-git`

```bash
npm install hexo-deployer-git --save
```

2. 修改博客根目录下的 `_config.yml` 文件，将文件末尾的 `deploy` 下的内容改为如下形式，库的 SSH 链接可从 GitHub 获取。

```yml
deploy:
	type: git
	repository: [ 库的SSH链接 ]
	branch: main
```

3. 重新生成博客内容

```bash
hexo g
```

4. 发布到网络

```bash
hexo d
```

5. 打开 `[用户名].github.io` 即可访问你的博客