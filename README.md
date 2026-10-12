# Course Review Coach · 课程复习教练

A reusable Codex skill for step-by-step course review, short quizzes, evidence-based feedback, and persistent learning records.

把课程笔记和练习题组织成可以持续推进、跨聊天接续的复习过程：

**一个小知识点 → 一道短小测 → 等待作答 → 批改补漏 → 后续独立复测。**

## 核心做法

- 从课程材料建立来源索引与学习路线，区分资料覆盖和正式考试范围。
- 默认中文从零解释，保留英文术语；可按学生要求调整语言与节奏。
- 一次讲一个小知识点，给一道短题后等待回答。
- 按真实作答记录状态，区分独立完成、提示后完成和看过解答。
- 在课程项目中维护一份学习记录，通过简短的 `AGENTS.md` 入口恢复进度。
- 支持补先修、跳题、直接看答案、考前速记与考后收尾。

## 安装

将本仓库复制到个人 Codex skills 目录中的 `course-review-coach` 文件夹。默认目录为 `~/.codex/skills`；设置了 `CODEX_HOME` 时使用该目录下的 `skills`。

首次安装、目标目录尚不存在时，可运行：

```bash
git clone https://github.com/Obitlyy/course-review-coach.git "${CODEX_HOME:-$HOME/.codex}/skills/course-review-coach"
```

若已有同名 Skill，请先检查现有内容，避免覆盖自己的修改。

## 使用

在课程项目中放入笔记、讲义或练习题，然后发送：

```text
用 $course-review-coach 带我复习这门课。先查看课程材料和已有学习记录，从当前进度继续。
```

也可以指定：

```text
我基础很弱，用中文从零讲，保留英文术语。每次一个知识点，讲完给一道短题，等我回答后再继续。
```

## 文件

| 文件 | 用途 |
|---|---|
| `SKILL.md` | 辅导流程、批改规则与学习记录维护方式 |
| `agents/openai.yaml` | Skill 的名称、简介与默认调用提示 |
| `assets/review-guide-template.md` | 新课程的持续学习记录模板 |

学习记录保存在各自的课程项目里。本仓库提供通用方法与空白模板，不包含课程讲义、学生作答或私人学习记录。
