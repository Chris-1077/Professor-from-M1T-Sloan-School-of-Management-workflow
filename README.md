# MIT Private Teaching Workflow

> **"好学近乎知，力行近乎仁，知耻近乎勇乎"** — *The Doctrine of the Mean*

Turn Claude Code into an MIT Sloan Adjunct Dean who teaches you one-on-one using the Socratic method.

## What Is This

A complete three-stage learning workflow built for Claude Code:

```
📖 Pre-class Prep       🎓 Interactive Class       📝 Post-class Notes
  Source material  →    Role-play teaching    →    HTML notebook
  (PDF/Word)            (MIT Dean Socratic)        (classroom transcript style)
```

## Demo

| Traditional Study | This Workflow |
|-------------------|---------------|
| Read alone, forget fast | Adjunct Dean challenges you with Socratic questioning — you answer before he explains |
| No idea what's important | Key chapters marked ★, tricky concepts turned into trap questions |
| Notes = copy-paste | Notes = classroom transcript, preserving your wrong answers and funny moments |

[View example notes →](./示例笔记.html)

## Quick Start

### 1. Copy the folder

Copy the entire folder into your project root:

```
your-project/
├── MIT私教授课工作流/          ← Copy this folder
│   ├── SKILL.md
│   ├── 笔记模板.html
│   ├── build_word.py
│   ├── .claude/skills/
│   │   └── mit-teaching.md
│   └── ...
```

### 2. Register the Skill

Copy `.claude/skills/mit-teaching.md` into your project's `.claude/skills/`.

If the directory doesn't exist yet:
```bash
mkdir -p .claude/skills
cp MIT私教授课工作流/.claude/skills/mit-teaching.md .claude/skills/
```

### 3. Speak the Passphrase

In Claude Code, type:

> **好学近乎知，力行近乎仁，知耻近乎勇乎**

The Adjunct Dean walks into the classroom. Class begins.

## Commands

| You say | What happens |
|---------|-------------|
| `好学近乎知，力行近乎仁，知耻近乎勇乎` | Activate the Dean, enter class |
| `教我第四章` / "Teach me Chapter 4" | Start teaching from that chapter |
| `继续讲` / `老师好` | Resume class |
| `帮我整理笔记` / "Generate notes" | Generate an HTML notebook for the current chapter |
| `下课` / "Class dismissed" | Pause class, keep the role |

## Customization

Not teaching Consumer Behavior? Edit `SKILL.md`:
- Replace the **knowledge map** (Section 6) with your subject
- Replace the **persona** with your field
- The Socratic rhythm and interaction pattern are universal — no changes needed

## Dependencies (optional)

Only needed for the Word document extraction feature:
```bash
pip install python-docx PyMuPDF pdfplumber
```

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | The brain: persona, teaching protocol, knowledge map |
| `笔记模板.html` | HTML notebook template |
| `build_word.py` | PDF → structured Word document |
| `.claude/skills/mit-teaching.md` | Skill registration |
| `示例笔记.html` | Full example: Chapter 3 class notes |
| `分享指南.md` | Installation guide for colleagues |

## License

MIT License — take it, modify it, share it.

---

# MIT 私教授课工作流

> **"好学近乎知，力行近乎仁，知耻近乎勇乎"** —《中庸》

让 Claude Code 化身为 MIT 斯隆编外院长，用苏格拉底追问法进行一对一互动教学。

## 这是什么

一个完整的三阶段学习工作流，专为 Claude Code 打造：

```
📖 课前梳理         🎓 互动课堂          📝 课后笔记
  源材料      →     角色扮演       →     HTML 笔记本
  (PDF/Word)       (MIT 院长追问)        (课堂实录风格)
```

## 演示效果

| 普通学习 | 本工作流 |
|---------|---------|
| 一个人啃教材，看了就忘 | 编外院长苏格拉底追问，让你先答再讲 |
| 读完不知道重点在哪儿 | 重点章标 ★，易混淆概念设计成陷阱题 |
| 笔记 = 复制粘贴 | 笔记 = 课堂实录，保留你答错和搞笑的名场面 |

[查看示例笔记 →](./示例笔记.html)

## 快速开始

### 1. 复制文件

把整个文件夹复制到你项目的根目录：

```
你的项目/
├── MIT私教授课工作流/          ← 复制这整个文件夹
│   ├── SKILL.md
│   ├── 笔记模板.html
│   ├── build_word.py
│   ├── .claude/skills/
│   │   └── mit-teaching.md
│   └── ...
```

### 2. 注册 Skill

把 `.claude/skills/mit-teaching.md` 复制到你项目的 `.claude/skills/` 下。

如果还没有 `.claude/skills/` 目录，先创建：
```bash
mkdir -p .claude/skills
cp MIT私教授课工作流/.claude/skills/mit-teaching.md .claude/skills/
```

### 3. 说暗号

在 Claude Code 里输入：

> **好学近乎知，力行近乎仁，知耻近乎勇乎**

编外院长走进教室。开始上课。

## 可用指令

| 你说 | 发生什么 |
|------|---------|
| `好学近乎知，力行近乎仁，知耻近乎勇乎` | 激活院长，进入课堂 |
| `教我第四章` | 从该章节开始授课 |
| `继续讲` / `老师好` | 继续上课 |
| `帮我整理笔记` | 生成当前章节的 HTML 课堂笔记 |
| `下课` | 暂停课堂，保持角色 |

## 自定义

教的不是消费者行为学？编辑 `SKILL.md`：
- 替换**知识地图**（第六章）为你教的科目
- 替换**角色设定**为你的领域
- 教学节奏和互动模式是通用框架，不用改

## 依赖（可选）

仅 Word 梳理功能需要：
```bash
pip install python-docx PyMuPDF pdfplumber
```

## 文件说明

| 文件 | 用途 |
|------|------|
| `SKILL.md` | 核心大脑：角色设定、教学规范、14章知识地图 |
| `笔记模板.html` | 课后笔记的 HTML 骨架模板 |
| `build_word.py` | PDF → 结构化 Word 梳理文档 |
| `.claude/skills/mit-teaching.md` | Skill 注册文件 |
| `示例笔记.html` | 第三章课堂笔记的完整示例 |
| `分享指南.md` | 给同事的安装说明书 |

## 许可

MIT License — 拿去用，拿去改，拿去分享。
