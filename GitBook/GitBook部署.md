# GitBook部署

记录下GitBook的部署方法

---

我采用的是Linux来部署，因为Windows下的安装配环境变量等过于麻烦，而且gitbook的配置需要特定版本的nodejs，所以采用Linux来部署。





## 使用nvm安装Node.js和npm

1.安装npm

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

然后，添加nvm到你的shell配置文件中（例如`.bashrc`，`.zshrc`等）。

```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

使配置文件生效：

```bash
source ~/.bashrc
```

2.安装node.js（推荐10.24.1版本）

```bash
nvm install 10.24.1
```

## 安装GitBook CLI

现在，你可以使用npm安装GitBook CLI：

```bash
npm install -g gitbook-cli
```

然后建一个GitBook文件夹，

```bash
gitbook init
```

即可开始安装，注意开梯子，下载需要几分钟。



## 生成部署

在项目根目录下

生成:

```bash
gitbook build
```

部署:

```
gitbook serve
```



访问`http://localhost:4000`即可