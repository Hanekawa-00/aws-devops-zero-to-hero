# AWS DevOps Zero to Hero 中文翻译计划

## 项目概述

将 `aws-devops-zero-to-hero` 项目翻译为中文版本。

**仓库地址:**
- Origin: `Hanekawa-00/aws-devops-zero-to-hero` (你的 fork)
- Upstream: `iam-veeramalla/aws-devops-zero-to-hero` (原仓库)
- 分支: `chinese-translation`

---

## 翻译范围统计

| 类别 | 目录数 | 文件数 |
|------|--------|--------|
| 根目录文件 | - | 3 |
| Day 目录 | 18 | ~32 |
| interview-questions | 1 | 26 |
| scripts | 1 | 2 |
| **总计** | 20 | **~63** |

---

## 工作流程 (每个 Day)

```
┌─────────────────────────────────────────────────────────┐
│  Day X 翻译流程                                          │
├─────────────────────────────────────────────────────────┤
│  1. 查看目录结构，识别需要翻译的文件                      │
│  2. 翻译所有 .md 文件 (README, 笔记等)                   │
│  3. 翻译 .sh/.py 脚本中的注释                            │
│  4. 启动子agent审查翻译质量                              │
│  5. 根据审查报告修正问题                                  │
│  6. git add + commit + push                             │
└─────────────────────────────────────────────────────────┘
```

---

## 详细任务列表

### 步骤 0: 根目录文件
**文件:**
- `README.md` - 项目主说明文档
- `LICENSE` - Apache 2.0 许可证 (翻译说明部分)
- `appspec.yml` - CodeDeploy 配置文件 (翻译注释)

**流程:** 翻译 → 审查 → commit → push

---

### Day 目录翻译任务

| 顺序 | Day | 文件数 | 主要内容 |
|------|-----|--------|----------|
| 1 | day-2 | 1 | AWS 基础入门 |
| 2 | day-3 | 1 | AWS CLI |
| 3 | day-4 | 1 | IAM 用户管理 |
| 4 | day-5 | 1 | IAM 策略 |
| 5 | day-6 | 1 | VPC 基础 |
| 6 | day-7 | 0 | (空目录) |
| 7 | day-8 | 0 | (空目录) |
| 8 | day-9 | 1 | EC2 基础 |
| 9 | day-14 | 7 | Lambda/无服务器 |
| 10 | day-16 | 4 | S3 存储 |
| 11 | day-17 | 1 | CloudFormation |
| 12 | day-18 | 2 | CloudWatch |
| 13 | day-19 | 1 | 参数存储 |
| 14 | day-20 | 1 | Secrets Manager |
| 15 | day-21 | 4 | CodePipeline |
| 16 | day-22 | 7 | CodeDeploy |
| 17 | day-24 | 2 | Docker |
| 18 | day-25 | 3 | Kubernetes |

---

### 步骤 19: interview-questions (26文件)
面试题目录，包含 AWS DevOps 相关问答。

**流程:** 批量翻译 → 审查 → commit → push

---

### 步骤 20: scripts (2文件)
脚本文件目录。

**流程:** 翻译脚本注释 → 审查 → commit → push

---

## 审查标准

每次翻译完成后，启动 `delegate_task` 进行审查：

```
delegate_task(
  goal="审查翻译文件的准确性和完整性",
  context="原文: [file], 译文: [file_CN]",
  toolsets=["file", "terminal"]
)
```

**检查项:**
- ✅ 段落数量一致
- ✅ 代码块未翻译
- ✅ 链接完整
- ✅ Markdown 格式正确
- ✅ AWS 术语规范

---

## 翻译规范

### 保持原样的内容
- AWS 服务名称: EC2, S3, VPC, IAM, Lambda, CloudFormation 等
- 命令和代码块
- 文件路径和 URL
- 配置文件键名

### 需翻译的内容
- 说明文字和教程内容
- 步骤描述
- 注释 (代码注释翻译为中文)
- 标题和列表项

### 术语对照
参考 `translation-review` 技能中的术语表。

---

## Git 提交格式

每个 Day 完成后使用统一提交格式：

```bash
git add .
git commit -m "翻译: Day X - [主题] 完成

- 翻译文件: [文件列表]
- 审查状态: 通过
- 审查报告: [评分]"
git push origin chinese-translation
```

---

## 最终步骤

全部翻译完成后：
1. 检查所有文件完整性
2. 更新 README 添加中文版本说明
3. 创建 Pull Request 到 upstream (可选)
4. 通知用户完成

---

## 开始执行

准备好后，开始执行步骤 0 (根目录文件翻译)。