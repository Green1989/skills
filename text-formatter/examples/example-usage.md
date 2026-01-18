# Text Formatter Skill - Usage Example

## Example 1: Academic Paper Formatting

### Input (unformatted.txt):
```
深度学习在自然语言处理中的应用研究
摘要
本研究探讨了深度学习技术在自然语言处理领域的应用...
引言
自然语言处理是人工智能的重要分支近年来深度学习技术的发展...
相关工作
传统方法基于规则的方法和统计机器学习方法...
深度学习方法神经网络语言模型卷积神经网络...
实验结果数据集介绍
我们在三个公开数据集上进行了实验...
实验设置
```


### Output (formatted.md):
```markdown
# 📋 深度学习在自然语言处理中的应用研究

## 摘要

本研究探讨了**深度学习**技术在**自然语言处理**领域的应用...

## 📖 引言

**自然语言处理**是人工智能的重要分支。近年来，**深度学习**技术的发展...

## 🔍 相关工作

### 传统方法
- 基于规则的方法
- 统计机器学习方法

### 深度学习方法
- **神经网络语言模型**
- **卷积神经网络**
- **Transformer架构**

## 📊 实验结果

### 数据集介绍
我们在三个公开数据集上进行了实验...

### 实验设置
...
```

---

## Example 2: Technical Report

### Input:
```
系统性能优化报告
系统概述
当前系统存在性能瓶颈主要体现在响应时间长...
问题分析
数据库查询效率低下索引不合理...
网络传输数据包过大...
解决方案
优化数据库索引添加复合索引...
压缩网络传输数据使用gzip...
```

### Output:
```markdown
# 📋 系统性能优化报告

## 📖 系统概述

当前系统存在**性能瓶颈**，主要体现在：
- ⚠️ 响应时间长
- ⚠️ 吞吐量低
- ⚠️ 资源占用高

## 🔍 问题分析

### 数据库问题
- 🐌 查询效率低下
- 🐌 索引不合理

### 网络问题
- 🐌 数据包过大
- 🐌 请求次数过多

## 💡 解决方案

### 数据库优化
- ✅ 添加**复合索引**
- ✅ 优化查询语句
- ✅ 使用连接池

### 网络优化
- ✅ 使用 **gzip** 压缩
- ✅ 减少 HTTP 请求
- ✅ 启用缓存策略

## 📌 预期效果

优化后系统性能提升**50%**，响应时间从平均 **2s** 降低到 **1s**。
```

---

## Example 3: Meeting Notes

### Input:
```
2024年1月15日产品评审会议
参会人员张三李四王五
会议议程
1. 回顾上次会议纪要
2. 讨论新功能设计
3. 确定开发计划
讨论内容
关于用户注册功能需要添加手机验证...
关于支付模块要支持多种支付方式...
行动计划
张三负责设计数据库...
李四负责前端开发...
```

### Output:
```markdown
# 📋 2024年1月15日产品评审会议

## 👥 参会人员
- 张三
- 李四
- 王五

## 📝 会议议程

1. 回顾上次会议纪要
2. 讨论新功能设计
3. 确定开发计划

## 💬 讨论内容

### 用户注册功能
- 💡 需要添加**手机验证**
- ⚠️ 考虑第三方短信服务
- 📊 预计开发时间: 3天

### 支付模块
- 💡 支持**多种支付方式**: 微信、支付宝、银行卡
- ⚠️ 注意支付安全
- 📊 预计开发时间: 5天

## ✅ 行动计划

| 负责人 | 任务 | 截止日期 |
|--------|------|----------|
| 张三 | 设计数据库 | 2024-01-20 |
| 李四 | 前端开发 | 2024-01-25 |
| 王五 | 后端开发 | 2024-01-25 |

## 📌 下次会议

**时间**: 2024年1月22日 14:00
**议题**: 功能进度回顾
```

---

## Common Use Cases

### Triggering the Skill:
- "Format this text file"
- "Convert this txt to markdown"
- "Make this document more readable"
- "Add structure to this unformatted text"
- "Format this report"

### What the Skill Does:
1. Analyzes document structure
2. Identifies titles and sections
3. Formats content (paragraphs, lists, quotes)
4. Emphasizes key points
5. Adds emoji markers for clarity
6. Creates proper markdown syntax

### What the Skill Doesn't Do:
- Change the original content (only structure)
- Translate text
- Summarize or condense content
- Add new information
- Change the author's voice or style
