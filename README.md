# What's This?

This branch holds all the config files for my blog, which can be useful when I have to reimplement it.

该分支负责备份本博客的配置文件，在最小化修改的前提下，加速博客迁移速度。

In order to keep this branch as simple as possible, I won't take all fancy stuff, but remain extreme clear.

也正是因为上述原因，这个分支不会加上很多花里胡哨的改动，以极简风格为主。

And this blog is HEAVILY based on Hexo & NexT, as a result, it has no compatibility to other platforms.

该博客是用 Hexo 部署的，主题选用了 NexT（Mist），并且会很难在其他平台上复现，也没有这样的打算。

# Get Started

复现本博客，你需要以下步骤：
1. 正确安装 Hexo，具体步骤[点这里](https://hexo.io/zh-cn/)，**请先不要创建博客文件夹**
2. 在`$HOME`目录打开终端，执行 `git clone -b backup git@github.com:cnLevi/cnLevi.github.io backup`
3. 此时，**创建你的博客文件夹**，注意文件夹名字应当遵循：`<username>.github.io`
4. [安装 Next 主题](https://theme-next.org/docs/getting-started/)，`git clone -b v7.0.1 https://github.com/theme-next/hexo-theme-next themes/next`
5. 我的配置中，`package.json` 包含需要的插件列表，拷贝过去，并在博客文件夹根目录执行安装 `npm install`
6. 然后，拷贝剩下的配置文件到你的文件夹，全部合并（或替换），但不要拷贝我的 `.git` 文件夹
7. 接下来测试，在博客根目录执行 `hexo s` ，此时你会看到一篇博文，请检查图片、公式是否正确显示
8. 当测试通过，你需要修改 `_config.yml` 中关于 Git 部署的设置，**这一步很重要**

# Features

1. Fixed image links in markdown file, via `hexo-asset-image`
2. Fixed mathjax replace syntax
3. Surpport RSS/Feed, via `hexo-generator-feed`
4. Surpport search, via `hexo-generator-searchdb`
5. Social links now surrport Zhihu and Douban respectively
6. Some customized icons as examples
7. Misc that I may forgot...

# Limitations

1. 为了支持同时支持原生MD图片语法与独立链接（abbrlink），博文图片文件夹的名称必须与博文链接号相同
2. 接上，在站点 `_config.yml` 文件中，必须保持 `post_asset_folder: true`

