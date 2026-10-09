# whitebox-prompt-skill

用于从白模、clay、proxy、previs、Blender 或 Unreal 参考视频编写和审计模型中立的视频生成提示词。

白模视频提供动作、空间、镜头和时间证据；已经提供的外观参考图负责其明确绑定的外观属性。提示词采用六段式结构：主体定义、内容概述、保留与替换要求、详细分镜描述、整体声景、画外配乐。

当前内容版本：**3.1.0**。Skill 名称及调用方式统一为 **`whitebox-prompt-skill`**。

## 安装到 Codex

克隆本仓库并复制 skill 文件：

```bash
git clone https://github.com/spinning888/Whitebox_prompt.git
cd Whitebox_prompt
mkdir -p "$HOME/.codex/skills/whitebox-prompt-skill"
cp -R SKILL.md agents references "$HOME/.codex/skills/whitebox-prompt-skill/"
```

安装完成后开启新的 Codex 对话，使用：

```text
用 $whitebox-prompt-skill 分析这段白模视频，写出模型中立的六段式提示词。
```

提供原始视频；如有角色外观参考图，请说明每张图对应哪个角色及需要保留的属性。

## 内容

- `SKILL.md`：技能入口、写作流程与输出要求。
- `agents/openai.yaml`：Codex 显示名称与默认调用提示。
- `references/`：白模分析流程、场景记录、视觉目标、示例、比较协议和来源说明。

该 skill 编写与审计语义提示词。实际视频输入支持和生成结果遵循情况，需要在具体模型运行中验证。
