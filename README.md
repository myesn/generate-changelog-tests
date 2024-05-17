# 介绍

自动生成 changelog 测试。

# conventional-changelog

[conventional-changelog](https://github.com/conventional-changelog/conventional-changelog) 是目前最流行的生成 changelog 的方式，但是这个库本身并不是一个 CLI，它是一个更底层的库。

官方的建议：
> 建议您使用高级 [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version) 库，它是 npm version 命令的直接替代品，可处理自动版本碰撞、标记和 CHANGELOG 生成。
> 
> 或者，如果想要将发布过程完全自动化为 CI/CD 的输出，请考虑使用 [semantic-release](https://github.com/semantic-release/semantic-release)。

## commit-and-tag-version

所以我们来试试 [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version)。

首先参考文档，根据自己的需求来安装：[Installing commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version?tab=readme-ov-file#installing-commit-and-tag-version)。

然后，直接看怎么使用：[CLI Usage](https://github.com/absolute-version/commit-and-tag-version?tab=readme-ov-file#cli-usage)。

最简单地尝试：
```bash
yarn global add commit-and-tag-version
commit-and-tag-version --first-release
```
更多的用法，还是看上面的文档。

# vercel/release

使用 https://github.com/vercel/release 生成 changelog，测试失败，会报错啊：
![image](https://github.com/myesn/vercel-release-changelog-tests/assets/18598579/4ad4fa47-ba9d-4c47-8faf-cc5d0d4fec97)

已经有佬提了 issue：https://github.com/vercel/release/issues/186

这错误就像套娃一样，无语了，并且我才发现 latest commit 时间是 `5b434c9 · 2 years ago`，OK 我放弃。

# git

这里有一些直接通过 git 命令查询 commits 消息的方式：
https://stackoverflow.com/questions/3523534/what-are-some-good-ways-to-manage-a-changelog-using-git
