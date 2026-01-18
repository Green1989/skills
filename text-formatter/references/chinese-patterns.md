# Chinese Text Patterns Reference

## Common Section Markers (Chinese)

### Chapter/Section Numbers

**Traditional Chinese numbering**:
- 一、二、三、四、五、六、七、八、九、十
- （一）（二）（三）
- 1. 2. 3. 4. 5.
- (1) (2) (3) (4)

**Formal chapter markers**:
- 第一章、第二章、第三章
- 第一节、第二节、第三节
- Part I, Part II, Part III

**Hierarchy indicators**:
- Level 1: 一、 / 1. / 第一章
- Level 2: （一） / 1.1 / 第一节
- Level 3: 1) / 1.1.1
- Level 4: (1) / 1.1.1.1

### Common Section Keywords

**Paper structure**:
- 摘要 / Abstract
- 引言 / Introduction / 前言
- 背景 / Background
- 文献综述 / Literature Review
- 方法 / Methodology / 方法论
- 结果 / Results
- 讨论 / Discussion
- 结论 / Conclusion
- 总结 / Summary
- 参考文献 / References

**Report structure**:
- 概述 / Overview
- 现状分析 / Current Situation
- 问题分析 / Problem Analysis
- 解决方案 / Solution
- 建议 / Recommendations
- 附录 / Appendix

**Book structure**:
- 序言 / Preface
- 目录 / Contents
- 正文 / Main Text
- 后记 / Postscript
- 索引 / Index

### Emphasis Indicators

**Explicit emphasis markers**:
- **注意**
- **重要**
- **关键**
- **核心**
- **必须**
- **务必**

**Warning patterns**:
- 警告、注意、请勿、避免、防止
- Warning, Caution, Important

**Question patterns**:
- ? 、？、如何、怎么、为什么、What、How、Why

### Common Formatting Issues in Chinese Text

**Line wrapping issues**:
- English words broken across lines: `informa-` `tion` → `information`
- Hyphens at line endings: `处理-` `方法` → `处理方法`
- Sentence fragments: Fixed by joining with context

**Spacing issues**:
- Missing space between Chinese and English: `方法使用Python` → `方法使用 Python`
- Inconsistent spacing around punctuation
- Multiple consecutive spaces

**Punctuation patterns**:
- Full-width punctuation: 。 ， ： ； ！ ？ （）
- Half-width punctuation: . , : ; ! ? ()
- Should preserve original punctuation style in most cases

### List Patterns

**Bullet indicators**:
- • · ○ ● ▪ ■
- - (dash)
- * (asterisk)

**Number patterns**:
- 1) 2) 3)
- (1) (2) (3)
- ① ② ③
- ⚪ ⚫
- ✓ ✗

**Chinese list markers**:
- 首先、其次、再次、最后
- 第一、第二、第三
- 一是、二是、三是
- 其一、其二、其三

### Quote and Citation Patterns

**Direct quote indicators**:
- "..." （中文引号）
- '...' （单引号）
- 「...」 （直角引号）
- 『...』 （双直角引号）

**Citation patterns**:
- [1], [2], [3]
- (Author, Year)
- （作者，年份）
- 参考文献[1]指出...

### Technical Content Patterns

**Code indicators**:
- Monospace fonts (if detectable)
- Keywords: import, function, return, class, def
- File extensions: .py, .js, .json, .txt
- Paths: /path/to/file, C:\path\to\file

**Command patterns**:
- Lines starting with $ (command prompt)
- Lines starting with > (prompt)
- Lines containing / or \ (paths)
- Keywords: npm, pip, python, node, git

**Data patterns**:
- Numbers with units: 100MB, 3.5GHz, 1920x1080
- Percentages: 50%, 85.6%
- Dates: 2024-01-01, 2024年1月1日
- Times: 14:30, 2:30 PM

### Table Detection Patterns

**Tabular data indicators**:
- Repeated separator characters: =, -, _, │
- Aligned columns
- Repeated patterns across lines
- Headers followed by separators
- Key-value pairs: Name | Value

### Separator Patterns

**Horizontal rules**:
- Three or more: ---, ===, ___, ***
- Space characters: (multiple blank lines)
- Page breaks: (form feed character or page numbers)

## Content Type Detection

### Article/Paper characteristics:
- Clear section structure
- Abstract and conclusion sections
- References or citations
- Formal tone
- Technical terminology

### Report characteristics:
- Executive summary
- Data and statistics
- Recommendations section
- Tables and figures references
- Business/technical focus

### Tutorial/Guide characteristics:
- Step-by-step instructions
- Code examples
- Command outputs
- "How to" language
- Screenshots references

### Meeting Notes characteristics:
- Date/time headers
- Attendees list
- Action items
- Discussion summaries
- Bullet points
- Time markers

## Pattern Priority

When multiple patterns conflict, prioritize:
1. Explicit numbering (一、, 1., 第一章)
2. Section keywords (引言, 结论, Introduction)
3. Standalone lines with content indicators
4. Formatting (centering, all caps, font size in rich text)

## Non-Patterns to Avoid

**Don't confuse as titles**:
- Sentence beginnings that happen to be numbered
- List items (should be lists, not titles)
- Dates or timestamps
- Page numbers or headers
- Repeated emphasis phrases
