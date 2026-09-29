# 生物医药论文汇报 Skill

按论文的生物学问题组织组会汇报，保留完整证据，用具体例子解释算法，并同步可直接讲述的讲稿。

这份指南来自实际论文汇报的多轮修改偏好。它规定内容组织与视觉取舍，不是把所有论文套成同一个页数或同一组算法的PPT生成器。

## 默认风格

- 沿原文Results划分小章节，用简短纯文字页帮助听众切换注意力。
- 同一问题的证据合在一起讲，保留所有正文、扩展和补充图的小面板。每节小结前再看完整大图。
- 算法随结果出现，交代为什么选、输入什么、怎样训练/计算、输出什么及其局限。用同一小例子穿插公式基础。
- 中文学术汇报，低饱和表格、白底深蓝、平面排版。默认参考HKBU视觉，但不冒称官方模板。
- 全文技术路线和新生成的科学示意图用英文标签，机制准确优先。漫画、动画、配音不作为默认产物。
- 页面控制密度，完整推导放在备注与逐页讲稿。图太密时保留单页，不为减少页数牺牲可读性。

## 使用

在支持Codex skills的环境里，将本仓库放到 `$CODEX_HOME/skills/biomedical-presentation-skill`；未配置 `CODEX_HOME` 时通常为 `~/.codex/skills/biomedical-presentation-skill`。不要覆盖同名已有skill。

也可以将仓库保存在数据盘，并在上述发现目录建立指向仓库的目录链接。依赖数据盘的链接需在数据盘可用时使用。Windows可用目录联接，其他系统可用符号链接。

在新会话中调用：

```text
使用 $biomedical-presentation-skill，阅读这个文件夹的正文、补充材料和源码，制作中文组会PPT及讲稿。
```

```text
按 $biomedical-presentation-skill 优化现有PPT：合并同一问题的小图，保持全部图版覆盖，并把难懂的算法用例子讲清楚。
```

```text
使用 $biomedical-presentation-skill，解释这篇论文如何把新患者的数据变成预测结果，纳入相应结果页和讲稿。
```

自动选择已启用，但具体能否自动加载取决于宿主；显式调用最直接。其他支持 `SKILL.md` 的代理可按各自安装方式使用，界面元数据位于 `agents/openai.yaml`。

## 文件

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 核心流程和用户默认偏好 |
| [叙事与图版](references/narrative-and-figures.md) | 章节、合并、整图回顾、重要表格、讲稿 |
| [方法与复现](references/methods-and-reproducibility.md) | 算法与公式解释、比较边界、代码数据核验 |
| [视觉与交付](references/visual-and-delivery.md) | 模板、英文科学图、可读性与文件交付 |
| [验收清单](references/quality-checklist.md) | 科学、覆盖、排版和配套材料检查 |
| [章节模板](templates/chapter-plan.md) | 建立原文与汇报的对应关系 |
| [图版覆盖表](templates/figure-coverage.csv) | 逐个面板与重要表格登记 |

如环境提供 `presentations:Presentations`，搭配其PPTX实现与导出规范使用。本仓库没有内置渲染器，也不包含HKBU官方PPT模板或任何学校授权声明。

## 内容范围

仓库只发布自写指南、示例和空模板，不含论文全文、论文图、汇报文件、聊天记录、私人数据或本机路径。教学数字不是任何文章的研究结果。使用者需从自己的授权材料中获取原图和内容。

新论文的事实、参数、算法版本及作者背景需要重新核验。这个skill不授予上传或公开发布汇报材料的权限。

采用 [MIT License](LICENSE)，适用于本仓库原创内容，不授予第三方论文、商标或图像的使用权。
