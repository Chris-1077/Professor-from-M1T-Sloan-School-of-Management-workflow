# MIT Private Teaching Workflow <sub>v1.1</sub>

> **"好学近乎知，力行近乎仁，知耻近乎勇乎"** — *The Doctrine of the Mean*
> **"夫子循循然善诱人，博我以文，约我以礼"** — *The Analects*

Turn Claude Code into an MIT Sloan Adjunct Dean who teaches you one-on-one using the Socratic method. **Two teaching modes, one professor.**

## What Is This

A complete three-stage learning workflow built for Claude Code:

```
📖 Pre-class Prep       🎓 Interactive Class       📝 Post-class Notes
  Source material  →    Role-play teaching    →    HTML notebook
  (PDF/Word)            (MIT Dean Socratic)        (classroom transcript style)
```

### Two Modes for Different Learning Goals

| | Basic Mode (基础) | Advanced Mode (进阶·精讲深研) |
|---|---|---|
| **Passphrase** | 好学近乎知，力行近乎仁，知耻近乎勇乎 | 夫子循循然善诱人，博我以文，约我以礼 |
| **Style** | Survey Course — broad, fast, hit the highlights | Graduate Seminar — every knowledge block taught to mastery |
| **Interaction** | 2-5 Socratic Q&A per chapter | ~3x density: Teach → Student Summarize → Professor Evaluate & Correct |
| **Student role** | Answer questions, reason through concepts | Reconstruct knowledge in your own words after every block |
| **Best for** | Quick overviews, non-critical chapters, first pass | Deep mastery, foundational material, exam prep |

Switch between modes anytime — say either passphrase, or "切换到基础模式" / "切换到进阶模式".

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

### 3. Speak a Passphrase

In Claude Code, type either:

> **好学近乎知，力行近乎仁，知耻近乎勇乎**

for quick survey mode, or:

> **夫子循循然善诱人，博我以文，约我以礼**

for deep immersion mode. The Adjunct Dean walks into the classroom. Class begins.

## Commands

| You say | What happens |
|---------|-------------|
| `好学近乎知，力行近乎仁，知耻近乎勇乎` | Activate basic mode |
| `夫子循循然善诱人，博我以文，约我以礼` | Activate advanced deep-immersion mode |
| `切换到基础模式` | Switch from advanced to basic, keep current progress |
| `切换到进阶模式` | Switch from basic to advanced, dive deeper from current block |
| `教我第四章` / "Teach me Chapter 4" | Start teaching from that chapter |
| `继续讲` / `老师好` | Resume class |
| `帮我整理笔记` / "Generate notes" | Generate an HTML notebook for the current chapter |
| `下课` / "Class dismissed" | Pause class, keep the role |

## Customization

This workflow is **subject-agnostic**. The AI builds a knowledge map dynamically from whatever source material you provide (PDF, textbook, slides, etc.) — no pre-loaded content to swap out.

If you want to personalize the teaching persona:
- Edit the **persona** section in `SKILL.md` (Section 1) — change Prof. Chen's name, field, or personality
- The Socratic rhythm and interaction pattern are universal — no changes needed

## Dependencies (optional)

Only needed for the Word document extraction feature:
```bash
pip install python-docx PyMuPDF pdfplumber
```

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | The brain: persona, teaching protocol, knowledge map, dual-mode spec |
| `笔记模板.html` | HTML notebook template |
| `build_word.py` | PDF → structured Word document |
| `.claude/skills/mit-teaching.md` | Skill registration |
| `示例笔记.html` | Full example: Chapter 3 class notes |
| `分享指南.md` | Installation guide for colleagues |

## License

MIT License — take it, modify it, share it.

---

# MIT 私教授课工作流 <sub>v1.1</sub>

> **"好学近乎知，力行近乎仁，知耻近乎勇乎"** —《中庸》
> **"夫子循循然善诱人，博我以文，约我以礼"** —《论语·子罕》

让 Claude Code 化身为 MIT 斯隆编外院长，用苏格拉底追问法进行一对一互动教学。**双暗号，双模式，同一个教授。**

## 这是什么

一个完整的三阶段学习工作流，专为 Claude Code 打造：

```
📖 课前梳理         🎓 互动课堂          📝 课后笔记
  源材料      →     角色扮演       →     HTML 笔记本
  (PDF/Word)       (MIT 院长追问)        (课堂实录风格)
```

### 两种模式，按需选择

| | 基础模式 | 进阶模式·精讲深研 |
|---|---|---|
| **暗号** | 好学近乎知，力行近乎仁，知耻近乎勇乎 | 夫子循循然善诱人，博我以文，约我以礼 |
| **定位** | 导论课——快速建立框架认知 | 研究生研讨课——每个知识块讲到彻底掌握 |
| **互动密度** | 每章 2-5 轮苏格拉底追问 | 约 3 倍：讲授 → 学生用自己的话梳理 → 教授四维评判修正 |
| **学生角色** | 回答提问，推理思考 | 每小节自己重构知识脉络，接受教授严格评审 |
| **适用场景** | 快速概览、非重点章节、初次扫读 | 深度掌握、重点章节、备考复习 |

两种模式可随时切换——说出对应暗号即可，或直接说"切换到基础模式"/"切换到进阶模式"。

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

进入基础导览模式。或者：

> **夫子循循然善诱人，博我以文，约我以礼**

进入精讲深研模式。编外院长走进教室。开始上课。

## 可用指令

| 你说 | 发生什么 |
|------|---------|
| `好学近乎知，力行近乎仁，知耻近乎勇乎` | 激活基础模式 |
| `夫子循循然善诱人，博我以文，约我以礼` | 激活进阶精讲深研模式 |
| `切换到基础模式` | 从进阶切回基础，保持当前进度 |
| `切换到进阶模式` | 从基础切入进阶，从当前知识块开始深度教学 |
| `教我第四章` | 从该章节开始授课 |
| `继续讲` / `老师好` | 继续上课 |
| `帮我整理笔记` | 生成当前章节的 HTML 课堂笔记 |
| `下课` | 暂停课堂，保持角色 |

## 自定义

本工作流**不限定学科**。AI 会从你提供的任何源材料（PDF、教材、幻灯片等）中动态构建知识地图，无需预置内容。

如果想个性化教学角色：
- 编辑 `SKILL.md` 里的**角色设定**（第一节）——把 Prof. Chen 的名字、领域改成你自己的
- 教学节奏和互动模式是通用框架，不用改

## 依赖（可选）

仅 Word 梳理功能需要：
```bash
pip install python-docx PyMuPDF pdfplumber
```

## 文件说明

| 文件 | 用途 |
|------|------|
| `SKILL.md` | 核心大脑：角色设定、教学规范、动态知识提取流程、双模式规范 |
| `笔记模板.html` | 课后笔记的 HTML 骨架模板 |
| `build_word.py` | PDF → 结构化 Word 梳理文档 |
| `.claude/skills/mit-teaching.md` | Skill 注册文件 |
| `示例笔记.html` | 第三章课堂笔记的完整示例 |
| `分享指南.md` | 给同事的安装说明书 |

## 许可

MIT License — 拿去用，拿去改，拿去分享。
