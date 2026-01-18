---
name: text-formatter
description: Transform unformatted plain text documents (especially long articles and reports) into well-structured, readable Markdown documents. Use this skill when Claude needs to process raw text files that lack formatting, such as .txt documents containing articles, reports, or papers. The skill automatically identifies: (1) Title hierarchy (H1-H6), (2) Key points and emphasis for bolding, (3) Lists and blockquotes, (4) Document structure and sections, (5) Emoji markers for different content types. Works best with Chinese and English text.
---

# Text Formatter

Transform unformatted plain text into well-structured Markdown.

## Core Workflow

### 1. Analyze the Document

Before formatting, understand the document structure:

- Read the entire document to understand its content type and structure
- Identify the main topic and document type (article, report, paper, etc.)
- Look for natural section breaks and topic transitions
- Identify repeated patterns that indicate structure

### 2. Identify Title Hierarchy

Automatically detect and structure titles:

**H1 (Main Title)** characteristics:
- First line or prominent first paragraph
- Contains the document's main topic
- Usually stands alone, not part of a paragraph
- Often shorter and more declarative

**H2 (Major Sections)** characteristics:
- Major topic shifts or new chapters
- Often numbered (第一章, 1., Chapter 1, etc.)
- Introduces major themes
- Followed by multiple related paragraphs

**H3-H6 (Subsections)** characteristics:
- Subtopics under H2 sections
- Deeper levels of organization
- May use different indentation or numbering

**Patterns to recognize**:
- Numbered sections: "第一章", "1.", "一、", "Chapter 1", "Section 1"
- Keyword indicators: "引言", "结论", "摘要", "Introduction", "Conclusion", "Summary"
- Standalone lines that are not part of paragraphs
- Lines followed by blank space or separator lines
- Repeated structural markers

### 3. Format Content Structure

**Paragraphs**:
- Ensure proper line breaks between paragraphs (blank line)
- Merge broken lines within the same paragraph
- Remove excessive blank lines (more than 2)

**Lists**:
- Identify item patterns: bullets, dashes, numbers (1. 2. 3.), or Chinese numbers (一、二、三、)
- Convert to unordered lists (- ) or ordered lists (1. )
- Maintain list hierarchy with proper indentation (2 spaces per level)

**Blockquotes**:
- Identify quoted text, examples, or important notes
- Use `>` prefix for blockquotes
- Consider using blockquotes for: definitions, citations, important warnings

### 4. Emphasize Key Content

**Bold important points**:
- Keywords and technical terms (first mention)
- Important conclusions or findings
- Critical warnings or注意事项
- Data points and statistics
- Core arguments or thesis statements

**Use italics for**:
- Book titles, article titles
- Foreign language terms
- Emphasis in specific contexts

### 5. Add Emoji Markers

Use emojis to enhance readability (replace color functionality):

**Document structure**:
- 📋 Document title
- 📖 Chapters/sections
- 📝 Notes/comments
- ✅ Conclusion/summary

**Content types**:
- ⚠️ Warning/caution
- 💡 Idea/insight
- 🔍 Key point/focus
- 📊 Data/statistics
- 💬 Quote/reference
- ❓ Question/problem
- ✅ Answer/solution
- 📌 Important note
- 🔗 Related/see also

**Content importance**:
- ⭐ Very important
- 🔥 Critical/urgent
- 💎 Key insight

**Usage pattern**: Place emoji at the beginning of lines or sections, not inline within sentences.

### 6. Code and Technical Content

- Identify code snippets, commands, or technical terms
- Use inline code (backticks) for: file names, commands, function names, short code
- Use code blocks (triple backticks) for: multi-line code, command sequences, data structures
- Add language identifier to code blocks when possible: ```python, ```bash, ```javascript

### 7. Special Patterns

**Common document sections** (add appropriate emojis):
- 📋 Abstract/摘要 → Use H2 with emoji
- 📖 Table of contents/目录 → List format
- 📝 Introduction/引言 → H2
- 🔍 Analysis/分析 → H3
- 📊 Data/数据 → H3
- 💡 Conclusion/结论 → H2
- 📚 References/参考文献 → List format

**Tables**:
- Identify tabular data (repeated patterns, alignment)
- Convert to Markdown tables when appropriate
- Use tables for: comparative data, statistics, parameter lists

## Formatting Principles

1. **Preserve original meaning**: Never change the content, only improve structure and readability
2. **Be conservative with bold**: Only bold truly important content (overuse reduces effectiveness)
3. **Consistent hierarchy**: Maintain logical title nesting (H1 → H2 → H3, no skipping)
4. **Readability first**: Format for easy scanning and reading
5. **Emoji moderation**: Use emojis purposefully, not on every line
6. **Blank lines**: Use one blank line between sections, avoid excessive vertical space

## Example Transformation

**Before (raw text)**:
```
人工智能的发展历程
人工智能技术在过去几十年经历了多次发展阶段。第一阶段是符号主义ai...
机器学习的兴起
随着计算能力的提升机器学习技术开始广泛应用。深度学习神经网络...
重要的里程碑事件
1956年达特茅斯会议标志着ai学科的诞生...
```

**After (formatted)**:
```markdown
# 📋 人工智能的发展历程

人工智能技术在过去几十年经历了多次发展阶段。第一阶段是**符号主义AI**...

## 📖 机器学习的兴起

随着计算能力的提升，**机器学习**技术开始广泛应用。**深度学习**神经网络...

### 🔍 技术特点

- 神经网络架构
- 大数据训练
- GPU并行计算

## ⚠️ 重要的里程碑事件

- **1956年**: 达特茅斯会议标志着AI学科的诞生
- **2012年**: AlexNet在ImageNet竞赛中取得突破
- **2017年**: Transformer架构提出

## 💡 总结

人工智能的发展经历了从**符号推理**到**机器学习**再到**深度学习**的演进过程。
```

## Quality Checklist

After formatting, verify:

- ✅ Title hierarchy is logical (H1 → H2 → H3)
- ✅ No orphan bold markers (every `**` has a closing `**`)
- ✅ Paragraphs have proper spacing (blank line between paragraphs)
- ✅ Lists use consistent markers (- or 1.)
- ✅ Important terms are bold (first mention, key concepts)
- ✅ Emojis enhance rather than clutter the document
- ✅ Code uses backticks
- ✅ Original content is preserved (only structure changed)
- ✅ Document is scannable (clear visual hierarchy)

## Handling Edge Cases

**Unclear title hierarchy**:
- Look for numbering patterns: "1." vs "1.1" vs "1.1.1"
- Check line length (titles often shorter than paragraphs)
- Examine content following potential titles (paragraphs indicate sections)

**Mixed content types**:
- Separate different content types into sections
- Use horizontal rules (`---`) for major transitions
- Consider creating subdocuments for very long sections

**Poorly formatted source**:
- Fix common issues: inconsistent spacing, missing line breaks
- Merge hyphenated words that span lines
- Remove artifacts like page numbers or headers

**Very long documents** (>10k words):
- Consider splitting into multiple files
- Add table of contents at the beginning
- Use more H2/H3 sections for better navigation

## Advanced Features

**Table of Contents**: Add TOC for long documents using:
```markdown
## 📚 目录

- [引言](#引言)
- [第一章](#第一章)
- [第二章](#第二章)
- [结论](#结论)
```

**Callout blocks**: Use combination of emoji and blockquote for important notes:
```markdown
> 📌 **注意**: 此步骤需要管理员权限
```

**Definition lists**: For key terms, use bold + description format:
```markdown
**术语**: 定义和解释

**另一个术语**: 另一个定义
```
