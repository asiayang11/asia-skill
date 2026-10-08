# asia-skill

维护我自己生成和使用的 AI skills，通过 GitHub 托管。按用途分类，通过下方索引查找。

## Skill 索引

| 分类 | Skill | 中文名称 | 用途 | 关键词 |
| --- | --- | --- | --- | --- |
| [视觉设计](skills/visual-design/) | [draw-cozy-explainers](skills/visual-design/draw-cozy-explainers/SKILL.md) | 暖纸手绘说明图 | 制作中文科普、流程、对比和结构说明图；支持成图、提示词、版式方案及可编辑文件 | 暖纸、手绘、手账、信息图、粉蓝配色 |
| [视觉设计](skills/visual-design/) | [draw-tech-explainers](skills/visual-design/draw-tech-explainers/SKILL.md) | 蓝紫科技卡片说明图 | 制作科技简报、发布会摘要、产品全景、架构、流程和方案对比图；支持成图、提示词、版式方案及可编辑 SVG/HTML/PDF | 科技风、蓝紫渐变、信息卡片、架构图、发布摘要 |

## 目录结构

```text
asia-skill/
├── README.md                         # 分类与检索索引
├── AGENTS.md                         # 仓库维护约定
└── skills/
    └── visual-design/                # 视觉设计
        ├── draw-cozy-explainers/
        │   ├── SKILL.md              # 技能入口
        │   ├── agents/openai.yaml    # 展示与调用配置
        │   ├── assets/               # 图标与风格参考图
        │   └── references/           # 风格规范与提示词参考
        └── draw-tech-explainers/
            ├── SKILL.md              # 技能入口
            ├── agents/openai.yaml    # 展示与调用配置
            ├── assets/               # 图标与风格参考图
            └── references/           # 风格规范与提示词参考
```

按主要用途设置一级分类，每个 skill 保持独立目录。当前只有「视觉设计」；后续按实际需要增加分类，不预建空目录。

## 使用示例

在支持 skill 的工具中导入所需 skill 的完整目录，保留其中的参考文档和素材，然后调用。

### 暖纸手绘说明图

```text
使用 $draw-cozy-explainers，把下面的内容制作成暖纸手绘风格的中文说明图。
```

```text
使用 $draw-cozy-explainers 解释 HyperLogLog，只给提示词，不生成图片。
```

查看 [风格参考图](skills/visual-design/draw-cozy-explainers/assets/style-reference.png)、[风格规范](skills/visual-design/draw-cozy-explainers/references/style-guide.md) 和 [构图与提示词](skills/visual-design/draw-cozy-explainers/references/prompt-patterns.md)。

### 蓝紫科技卡片说明图

```text
使用 $draw-tech-explainers，将这份发布会笔记做成竖版科技摘要长图，只使用笔记里的信息。
```

```text
使用 $draw-tech-explainers，解释 agent、loop、harness 的关系，只给提示词。
```

查看 [风格参考图](skills/visual-design/draw-tech-explainers/assets/style-reference.png)、[视觉规范](skills/visual-design/draw-tech-explainers/references/style-guide.md) 和 [构图与提示词](skills/visual-design/draw-tech-explainers/references/prompt-patterns.md)。

## 维护约定

- 新增 skill 放入 `skills/<分类>/<skill-name>/`；目录名与 `SKILL.md` 中的 `name` 一致。
- 导入已有 skill 时保留完整内容和所需资源；不另写一个同名版本替代原包。
- 新增、改名、移动或删除 skill 时，同步更新索引、目录结构和相关链接。
- 每个 skill 只放在一个主要分类中，通过中文名称、用途和关键词补充检索。
- 提交前核对 skill 格式、内部引用和 README 链接，避免收录缺失素材或未完成的占位内容。
- 新增 skill 完成并校验通过后，直接 commit 本次相关变更。
