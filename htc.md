# 如何参与

本页面的内容来自于 [如何参与 - OI Wiki](https://oi-wiki.org/intro/htc/)，并根据本仓库实际情况做了精简与修改。因为操作流程相似，所以该链接的内容可以作为参考。

在您的更改被合并到主分支之前，您对本仓库所作出的修改均不会影响本仓库，所以无需担心您的修改会破坏本仓库已有的内容。

## 在 GitHub 上编辑

参与本仓库的编写 **需要** 一个 GitHub 账号（可以前往 [GitHub 的账号注册页面](https://github.com/signup) 页面注册），但 **不需要** 高超的 GitHub 技巧，即使您是一名新手，只要按照下面所述的步骤操作，也能够 **非常出色** 地完成编辑。

可以查看 [GitHub 的官方教程](https://skills.github.com/) 获取更多信息。

### 编辑单个文件的内容

1.  在本仓库中找到对应文件。
2.  点击右侧的铅笔图标。
3.  在编辑框内执行修改
4.  修改完成后点击右上方的 「Commit changes...」 按钮，按  点击按钮后按 [Commit 与 Pull Request 信息格式规范](#commit-与-pull-request-信息格式规范) 填写 Commit message，之后点击 「Propose changes」 。
5.  此时页面上方会显示一个绿色的 **Create pull request** 按钮，点击后 GitHub 会跳转到一个创建 Pull Request 页面。向下滚动检查自己所作出的修改没有错误后，按照 [Commit 与 Pull Request 信息格式规范](#commit-与-pull-request-信息格式规范) 书写 Pull Request 描述，然后点击页面上的绿色的 **Create pull request** 按钮创建 Pull Request。
6.  不出意外的话，您的 Pull Request 就顺利提交到仓库，等待合并到主仓库即可。

### 向 Pull Request 追加更改

1.  打开 [Pull Request 列表](https://github.com/LZUPAT/ACM/pulls)，找到您的 Pull Request 并点击。
2.  Pull Request 页面的标题下方将会有一段例如 `<您的ID> wants to merge x commits into ACM:main from <您的ID>:<您的分支名>` 的文字，点击 `<您的ID>:<您的分支名>` 部分。
3.  您应该会被重定向到您的分支仓库中，而且文件列表左上角的分支名称是您提交 Pull Request 的分支名称。
4.  进行您需要的更改，您的更改会被自动追加到您的 Pull Request 中。

## 使用 Git 在本地进行编辑

对于较为复杂的操作，推荐使用 Git 在本地进行编辑。

大致流程如下：

1.  将主仓库 fork 到自己的仓库中；
2.  将 fork 后的分支仓库 clone 到本地；
3.  在本地进行修改后 commit 这些更改；
4.  将这些更改 push 到您克隆的分支仓库；
5.  提交 Pull Request 至主仓库。

详细的操作方式可以参考 [Git - OI Wiki](https://oi-wiki.org/tools/git/)。

### 向 Pull Request 追加更改

在 clone 下来的本地分支仓库中继续进行修改，并 commit 以及 push 这些更改即可。您的更改会被自动追加在 Pull Request 中。

## Commit 与 Pull Request 信息格式规范

对于提交时需要填写的 commit 信息，请遵守以下几点基本要求：

1.  commit 摘要请简要描述这一次 commit 改动的内容。注意 commit 摘要的长度不要超过 50 字符，超出的部分会自动置于正文中。
2.  如果需要进一步描述本次 commit 内容，请在正文中详细说明。

对于 Pull Request，请遵守以下几点要求：

1.  标题请写明本次 Pull Request 的目的（做了 **什么** 工作，修复了 **什么** 问题）。
2.  内容请简要叙述修改的内容。如果该 Pull Request 完全解决了一个 issue，请在描述中添加 `fix #xxxx`、`reslove #xxxx` 或 `close #xxxx`，其中 `xxxx` 代表 issue 的编号，推荐查阅 <https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue> 了解相关机制。

对于 Pull Request 的标题和 commit 的摘要，推荐使用如下格式书写：

```plain
<修改类型>(<文件名>): <修改的内容>
```

修改类型分为如下几类：

-   `feat`：用于添加内容的情况。
-   `fix`：用于修正现有内容错误的情况。
-   `refactor`：用于对一个页面进行重构（较大规模的更改）的情况。
-   `revert`：用于回退之前更改的情况。

示例：

-   `fix(ds/persistent-seg): 修改代码注释使描述更清晰`
-   `feat(math/poly/fft): better proof`
-   `refactor(ds/stack): 整理页面内容`
