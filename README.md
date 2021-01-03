# mac 装机

# 下载的软件
- 微信
- [postman](https://www.postman.com/downloads/)
- [vscode](https://code.visualstudio.com/download)
- [iterm zsh](https://iterm2.com/downloads.html)
- [idea2020.1.3](https://www.jetbrains.com/idea/download/other.html)
- [utools](https://u.tools/)
- [snipaste截图](https://zh.snipaste.com/)
- [docker-desktop](https://www.docker.com/products/docker-desktop)

# 系统配置

1. iterm2和zsh配置 =>[配置教程](https://vincef0ng.cn/post/iterm2-for-mac-tutorial/#%E6%95%88%E6%9E%9C)
    ```
    # 安装zsh
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    # 安装语法高亮
    brew install zsh-syntax-highlighting
    #主题
    git clone https://github.com/dracula/iterm

    # 如果出现Insecure completion-dependent directories detected:提示执行如下代码
    chmod 755 /usr/local/share/zsh
    chmod 755 /usr/local/share/zsh/site-functions

    ```

2. brew 更新[清华源](https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/)

    ```
    # macOS 用户，请使用以下两句命令
    export HOMEBREW_CORE_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git"
    export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles"

    # 也可从 GitHub 获取官方安装脚本，修改其中的仓库源，运行以安装 Homebrew/Linuxbrew

    /bin/bash -c "$(
        curl -fsSL https://github.com/Homebrew/install/raw/master/install.sh |
        sed 's|^BREW_REPO=.*$|BREW_REPO="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git"|g'
    )"
    ```

3. pypi设置清华源

    ```shell
    pip3 config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
    ```
4. switchhosts

    ```shell
    brew install --cask switchhosts
    ```
5. [jdk下载](https://github.com/LilithBristol/javajdkforwinx64)

    推荐此处下载[jdk8](https://github.com/frekele/oracle-java/releases)
6. 选装：[gitkraken下载](https://release.axocdn.com/darwin/GitKraken-v6.5.1.zip) 一个git客户化管理工具，必须增加下面的hosts防止升级

    ```
    127.0.0.1 release.gitkraken.com
    ```
7. node 和 npm配置

    ```
    brew install node
    npm config set registry=http://registry.npm.taobao.org
    ```

8. 生成sshkey

    ```
    ssh -t rsa -C youemail@xx.com
    ```
