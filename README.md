# dsh-agent-teams-release

DSH Agent Teams 控制面板的**发布仓库**。这里只放打包产物，不放源码。

## 这是什么

这个仓库由 [Agent Teams 控制面板](https://github.com/v1b0w) 的「一键发布」按钮自动写入。
每次发布会产生一个 Release，包含两个资产：

- `dsh-agent-teams-console-<version>.tar.gz` —— 面板安装包（index.js / client.js / package.json / cordis.patch.yml / version.json / icon.svg / README.md）
- `manifest.json` —— 版本清单，面板靠它判断有没有新版本

## 固定更新地址

面板的「诊断」页 → 「面板更新」里填这个地址，填一次以后不用再改：

```
https://github.com/v1b0w/dsh-agent-teams-release/releases/latest/download/manifest.json
```

`releases/latest` 是 GitHub 的永久重定向，会始终指向最新一次发布。

## 安全

面板拉取更新前会校验 `sha256`，不匹配就拒绝安装。更新功能默认**关闭**，需要在诊断页手动打开。

---

本文件由自动流程创建。请勿手动编辑。
