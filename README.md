# 慵懒男生 IP｜六格文章配图工作流

> 把中文文章转化为一张统一画布中的 6 格手绘编辑插画。主角始终是用户提供的慵懒男生 IP；每篇文章默认只调用一次图像生成，尽量节省生图额度。

## 目标

这是基于 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) 的工作流思路进行的个人化改造：保留“提炼文章认知锚点、用角色参与概念动作、用原创视觉隐喻解释观点”的方法；将角色替换为用户自己的慵懒男生 IP，并将逐张生成改为一次生成整张六格画布。

## 固定视觉 DNA

- **主角**：蓬松凌乱的黑色中短发、侧分刘海、半眯眼、轻微胡茬。
- **服装**：中灰色宽松连帽卫衣、深色抽绳、宽松黑裤、白色运动鞋。
- **性格**：慵懒、淡定、略带厌世感、冷幽默；不是可爱吉祥物。
- **画风**：干净白底、黑色手绘墨线、轻微不规则笔触、灰阶马克笔／铅笔铺色、留白充足；少量橙黄作为重点标注和箭头。可按文章需要极少量红蓝辅助色，但默认以黑白灰＋橙黄为主。
- **一致性**：六格必须是同一个角色，脸型、发型、眼睛、胡茬、衣服、头身比例和鞋型保持一致。
- **画布**：默认横向 3 列 × 2 行，共 6 格；统一画布、单次生成、格间留白均匀、每格可单独裁切；无标题、无序号；通常 2–3 格使用少量手写中文短句，其余格子以视觉叙事为主。

## 快速开始

### 用于 Codex / 支持 Agent Skill 的工具

把目录 `lazy-ip-article-illustrations/` 复制到你的 Skill 目录，例如：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./lazy-ip-article-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

然后提供文章正文并调用：

```text
Use $lazy-ip-article-illustrations 为下面这篇文章生成配图。
严格遵循 Skill：默认 6 格、3 列 × 2 行、一张完整画布、一次图像生成。
请先提炼观点并规划六格，但不要等待我确认；随后一次性生成整张图。
[粘贴文章]
```

如果你的 Agent 不支持 Skill 调用，直接复制 `lazy-ip-article-illustrations/SKILL.md` 中的主提示词模板即可。

## 目录结构

```text
.
├── README.md
├── NOTICE.md
├── LICENSE
├── assets/
│   └── references/
│       ├── character-sheet.png
│       ├── character-poses.png
│       └── article-style-reference.png
├── examples/
│   └── prompt-examples.md
└── lazy-ip-article-illustrations/
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── references/
    │   ├── style-dna.md
    │   ├── personal-ip.md
    │   ├── composition-patterns.md
    │   ├── prompt-template.md
    │   └── qa-checklist.md
    └── assets/references/README.md
```

## 每次执行的流程

1. 阅读文章或用户提供的主题。
2. 提炼主论点、因果链、冲突、转折和结论。
3. 规划 6 个互不重复的画格。
4. 让角色在每格中参与核心动作，不只是摆姿势。
5. 使用一条完整提示词一次性生成整张画布。
6. 检查画风、角色一致性、网格分隔、事实准确性和裁切空间。

## 重要限制

- 一次生图能降低调用次数，但不能保证每格中文字完全准确。不要把大段文字、复杂表格或关键数据完全交给图像模型绘制。
- 本工作流只承诺生成**一张六格整版图**，不自动声称已裁切成 6 个文件。需要单图时可在后续用图像工具按网格裁切。
- 若只有文章链接且当前环境无法读取正文，应明确请求用户粘贴正文，不得假装已阅读。
- 附带的用户参考图只用于固定角色外观与风格，不要直接复制参考图中的具体构图。

## 文件说明

- `lazy-ip-article-illustrations/SKILL.md`：完整执行规范。
- `references/style-dna.md`：画风和配色。
- `references/personal-ip.md`：人物设定。
- `references/composition-patterns.md`：六格叙事和原创隐喻。
- `references/prompt-template.md`：可复制的一次性生图提示词。
- `references/qa-checklist.md`：质量检查清单。
- `assets/references/`：用户提供的人物设定图和文章配图参考。
