# 临高文档贡献指南

无论你是热爱临高的临高人，还是擅长书面表达的语言爱好者，亦或是纯粹想帮 临高 改进文档的热心小伙伴，都欢迎来为 临高 文档做贡献，一起打造更加易用友好的 临高 文档！

如果你不了解Git，可以直接将你想修改，或者想了解的内容，发邮件给 hainanlingao@protonmail.com

## 可贡献的内容

欢迎任何对提升 临高 文档质量、易用性、维护效率的贡献，比如，你可以在以下方面进行贡献：

- [改进文档](#改进文档)
- [提供有关临高的资料](#提供有关临高的资料)

下面主要介绍了如何为前两项做出贡献。

### 改进文档

你可从以下任一方面入手：

- 修复文档格式（如标点、空格、缩进、代码块等）和错别字
- 修改过时或不当的内容描述
- 增加缺失的文档内容
- 回复或解决 [issue](https://github.com/hainan-lingao/main/issues) 并提 PR 更新相关文档
- 其它改进

### 提供有关临高的资料

通过Pull Request将资料提供到仓库 https://github.com/hainan-lingao/data

或者将资料发邮件给 hainanlingao@protonmail.com

## 快速上手资源

最常见的贡献方式就是提 Pull Request 了，那么提交流程是怎样的，又需要遵守哪些规范呢？我们已准备好齐全的快速上手指南，你也可以查阅 [main 现有的 Pull Request](https://github.com/hainan-lingao/main/pulls) 作为参考


- [必须遵循的 Markdown 规范](#必须遵循的-markdown-规范)


## Pull Request 提交流程

临高 文档的修改需要遵循一定的流程，具体如下。考虑到有些小伙伴是纯语言背景，命令行的流程掌握起来可能需要花些时间，之后我们也会提供更适合小白上手的 GitHub Desktop 客户端版提交流程（在添加至这里之前，可暂时参考 [lilin90](https://github.com/lilin90) 撰写的[小白上手流程](https://zhuanlan.zhihu.com/p/64880410)）。

### 第 1 步：Fork 本仓库

1. 打开 hainan-lingao/main 项目[仓库](https://help.github.com/articles/github-glossary/#repository)：<https://github.com/hainan-lingao/main>
2. 点击右上角的 [**Fork**](https://help.github.com/articles/github-glossary/#fork) 按钮，等待 Fork 完成即可。

### 第 2 步：将 Fork 的仓库克隆至本地

```
cd $working_dir # 将 $working_dir 替换为你想放置 repo 的目录。例如，`cd ~/Documents/GitHub`
git clone git@github.com:$user/main.git # 将 `$user` 替换为你的 GitHub ID

cd $working_dir/main
git remote add upstream git@github.com:hainan-lingao/main.git # 添加上游仓库
git remote -v
```

### 第 3 步：新建一个 Branch

1. 确保本地 master branch 与 upstream/master 保持最新。

    ```
    cd $working_dir/main
    git fetch upstream
    git checkout master
    git rebase upstream/master
    ```

2. 基于 master branch 新建一个 branch，名称格式为：aaa-bbb-ccc。

    ```
    git checkout -b new-branch-name
    ```

### 第 4 步：编辑文档进行增删或修改

在建好的 `new-branch-name` branch 上进行编辑，可使用 Markdown 编辑器（如 Visual Studio Code）打开 main repo，对相应文档进行增、删，或修改，并保存你的修改。

### 第 5 步：提交你的修改

```
git status
git add <file> ... # 如果你想提交所有的文档修改，可直接使用 `git add .`
git commit -m "commit-message: update the xx"
```

### 第 6 步：保持新建 branch 与 upstream/master 一致

```
# 在新建 branch 上
git fetch upstream
git rebase upstream/master
```

### 第 7 步：将你的修改推至远程

```
git push -u origin new-branch-name
```

### 第 8 步：创建一个 Pull Request

1. 打开你 Fork 的仓库：<https://github.com/$user/main>（将 `$user` 替换为你的 GitHub ID）
2. 点击 `Compare & pull request` 按钮即可创建 PR。


## 必须遵循的 Markdown 规范

临高 文档使用 Markdown 语言进行编写，为了保证文档质量和格式规范，你修改的文档需要遵循一定的 Markdown 规则

## 联系我们

查看 [关于我们](about-us)

## 来源

本贡献指南改编自[TiDB 文档贡献指南](https://github.com/hainan-lingao/main/blob/2ae07994e25d32b90e3d9b5f7114a482e8c51274/CONTRIBUTING.md)