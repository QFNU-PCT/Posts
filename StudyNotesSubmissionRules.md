---
title: 学习笔记提交规范
date: 2025-11-01 00:28:18
tags: 公告
---

为统一管理学习笔记，即日起所有笔记需通过 Pull Request (PR) 提交至指定仓库。

# 一、文件命名规则

文件名：必须为您的10位数字学号。

学号格式：以  2025413 开头，例如： 2025413047.md 。

## 二、文件格式要求

文件必须为纯文本格式。

文件后缀必须为  .md （Markdown 格式）。

### 三、文件内容规范

文件开头必须包含以下 YAML Front Matter 元数据块，格式如下：

```yaml
---
title: 您的笔记标题
date: 2025-10-31 17:43:20 # 请填写实际提交时间
tags: 笔记
copyright_author: 您的昵称 # 例如：Alice
---
```

示例：
```yaml
---
title: 动态规划算法入门
date: 2025-10-31 17:43:20
tags: 笔记
copyright_author: Alice
---
```
注意： date 字段请按  年-月-日 时:分:秒 格式填写实际时间， copyright_author 请填写您的昵称

