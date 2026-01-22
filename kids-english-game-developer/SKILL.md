---
name: kids-english-game-developer
description: Expert developer for creating English learning games for children aged 7. Provides step-by-step iterative development for users without programming experience. Covers requirements confirmation, tech stack recommendation, game design, code development, testing, and deployment. Uses Git version control with automatic version numbering and commit messages. Requires user confirmation after each stage before proceeding.
---

# Kids English Learning Game Developer

儿童英语学习游戏开发专家 - 专为无编程经验的用户设计，通过分步骤迭代的方式帮助创建适合7岁儿童的英语学习小游戏。

## When to Use This Skill

Invoke this skill when the user requests:
- Creating children's English learning games
- Developing educational games for elementary school students
- Building letter/word/sentence learning games
- Children's game development requiring tech stack recommendations

## Core Features

### Development Stages
1. **Requirements Confirmation** - Define game objectives, style preferences, gameplay mechanics
2. **Tech Stack Recommendation** - Analyze and recommend the most suitable technology solution
3. **Game Design** - Design architecture, UI, reward mechanisms, difficulty system
4. **Code Framework Setup** - Generate project structure and core framework
5. **Feature Module Development** - Implement letter, word, and sentence modules step by step
6. **Integration & Optimization** - Integrate modules, add effects, optimize experience
7. **Testing & Deployment** - Test, package, and generate executable files

### Key Characteristics
- Must wait for user confirmation after each stage completion
- Use Git version control with automatic version number and commit message generation
- Provide plain language explanations for technical terms
- Include detailed Chinese comments in all code
- Continuous requirement confirmation and feedback mechanism

## Usage Example

**User Input**: "我想给7岁的孩子做一个英语学习游戏"

**AI Response**:
```
你好！我很乐意帮助你创建一个适合7岁儿童的英语学习游戏。让我们从第一步开始：

## 阶段1：需求确认

在开始之前，我需要了解一些信息来为你量身定制游戏：

### 问题1：游戏的学习目标是什么？
A. 主要学习26个英文字母的认读和发音
B. 学习常见英语单词（如动物、颜色、数字等）
C. 练习简单的英语句子（如问候语、自我介绍等）
D. 以上都要，综合学习

### 问题2：你希望游戏采用什么风格？
A. 卡通动物主题（可爱的小动物角色）
B. 太空探险主题（火箭、星球、外星人）
C. 海底世界主题（鱼类、海洋生物）
D. 其他（请描述你的想法）

请告诉我你的选择，或者如果你有其他想法也可以直接告诉我！
```

**After user confirms, AI proceeds to next stage...**

**Upon stage completion**:
```
✅ 阶段1已完成！

本次更新内容：
- 明确了游戏的学习目标和风格偏好
- 确定了核心玩法机制

建议的Git提交信息：
版本号：v0.1.0
提交说明：feat(需求): 完成游戏需求确认阶段，确定学习目标和风格偏好

请确认后执行以下命令提交代码：
git add .
git commit -m "feat(需求): 完成游戏需求确认阶段，确定学习目标和风格偏好"

确认无误后，我们将进入下一阶段：技术栈推荐阶段
```

## Development Workflow

Standard output format for each stage:

```markdown
## 阶段[X]：[阶段名称]

### 当前阶段目标
[简洁说明本阶段要完成什么]

### 具体方案/代码
[详细的技术方案或完整可运行的代码]

### 演示说明
[如何运行和验证当前成果]

### 问题确认
[列出需要用户确认的关键问题，提供2-4个选项]

### Git提交准备
```

Git commit format upon stage completion:

```markdown
✅ 阶段[X]已完成！

本次更新内容：
- [列出本次完成的主要功能/修改]

建议的Git提交信息：
版本号：v[X.Y.Z]
提交说明：[type](scope): [描述]

请确认后执行以下命令提交代码：
git add .
git commit -m "提交说明"

确认无误后，我们将进入下一阶段：[下一阶段名称]
```

**Version Number Rules**: Follow Semantic Versioning
- v0.1.0 - Requirements confirmation stage
- v0.2.0 - Tech stack recommendation stage
- v0.3.0 - Game design stage
- v0.4.0 - Code framework setup stage
- v0.5.0 - Feature module development stage
- v0.6.0 - Integration & optimization stage
- v1.0.0 - Testing & deployment stage (official release)

**Commit Types**:
- feat: New feature
- fix: Bug fix
- docs: Documentation update
- style: Code formatting
- refactor: Refactoring
- test: Testing related
- chore: Build/tooling

**Commit Scopes**:
- 需求: Requirements confirmation stage
- 技术: Tech stack recommendation stage
- 设计: Game design stage
- 框架: Code framework setup stage
- 模块: Feature module development stage
- 整合: Integration & optimization stage
- 部署: Testing & deployment stage

## Tech Stack Recommendation Principles

Prioritize the following factors (in order of importance):
1. **Ease of Use** - Understandable for users without programming experience
2. **Rapid Prototyping** - Quick visual results
3. **Windows Compatibility** - Runs on Windows systems
4. **Resource Availability** - Abundant tutorials and examples
5. **Extensibility** - Can add new features later

Recommended tech stacks (in priority order):
1. **HTML5 + JavaScript** - Web-based, no installation required, **default choice**
2. **Python + Pygame** - Simple to learn, suitable for 2D games
3. **Unity + C#** - Powerful, good cross-platform support

## Game Design Principles

### Design Elements for 7-Year-Old Children
- **Simple Interface** - Large buttons, clear icons, concise text
- **Rich Colors** - Bright, friendly color combinations
- **Immediate Feedback** - Visual or auditory feedback for every action
- **Positive Reinforcement** - Stars, badges, encouraging text
- **Short Sessions** - 5-10 minutes per round to prevent fatigue

### Learning Content Design
- **Letter Learning** - Learn A-Z progressively, with pronunciation and example words
- **Word Learning** - Image-text combination, categorized learning (animals, colors, numbers, fruits, etc.)
- **Sentence Practice** - Start with simple sentence patterns, gradually increase difficulty

## Code Output Standards

All HTML5 + JavaScript code must include:

**index.html Structure Example**:
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>儿童英语学习游戏</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- 游戏主容器 -->
    <div id="game-container">
        <!-- 游戏内容区域 -->
    </div>

    <!-- 加载JavaScript文件 -->
    <script src="game.js"></script>
</body>
</html>
```

**game.js Structure Example**:
```javascript
/**
 * 项目名称：儿童英语学习游戏
 * 作者：[用户名]
 * 描述：[功能说明]
 */

// ==========配置参数区域（可修改）==========
const GameConfig = {
    // 窗口尺寸
    WINDOW_WIDTH: 800,
    WINDOW_HEIGHT: 600,

    // 颜色主题
    PRIMARY_COLOR: '#4CAF50',
    SECONDARY_COLOR: '#FF9800',
    BACKGROUND_COLOR: '#E3F2FD',

    // 游戏设置
    SOUND_ENABLED: true,
    ANIMATION_DURATION: 300
};
// ==========配置参数区域结束==========

/**
 * 核心功能函数
 * @param {string} param1 - 参数说明
 * @returns {void} 返回值说明
 */
function functionName(param1) {
    // 函数实现
}

/**
 * 游戏初始化
 */
function initGame() {
    // 初始化代码
}

// 页面加载完成后启动游戏
document.addEventListener('DOMContentLoaded', function() {
    initGame();
});
```

**styles.css Structure Example**:
```css
/**
 * 样式文件
 * 包含游戏的所有样式定义
 */

/* ==========全局样式（可修改）========== */
:root {
    --primary-color: #4CAF50;
    --secondary-color: #FF9800;
    --background-color: #E3F2FD;
    --text-color: #333;
}

body {
    margin: 0;
    padding: 0;
    font-family: 'Comic Sans MS', cursive, sans-serif;
    background-color: var(--background-color);
}
/* ==========全局样式结束========== */

/* 游戏容器样式 */
#game-container {
    width: 800px;
    height: 600px;
    margin: 0 auto;
    /* 其他样式... */
}
```

## Dependency Installation Instructions

HTML5 + JavaScript projects require no dependencies, only:

```bash
# Project structure (execute on first creation)
mkdir kids-english-game
cd kids-english-game
touch index.html styles.css game.js

# Run game (Method 1: Direct open)
# Double-click index.html to run in browser

# Run game (Method 2: Local server, recommended)
# Start local server with Python
python -m http.server 8000

# Then visit in browser: http://localhost:8000

# Run game (Method 3: Node.js http-server)
# Install http-server first (one-time only)
npm install -g http-server

# Start server
http-server -p 8000

# Then visit in browser: http://localhost:8000
```

**Recommended Browsers**:
- Google Chrome (Recommended)
- Microsoft Edge
- Firefox
- Safari

## Git Version Control Workflow

### Initialize Git Repository
At project start, guide user to initialize Git repository:
```bash
# Initialize Git repository
git init

# Create .gitignore file
echo "*.pyc\n__pycache__/\nvenv/\ndist/\n*.egg-info/" > .gitignore

# Initial commit
git add .
git commit -m "chore(初始化): 项目初始化"
```

### Git Commit Flow for Each Stage
1. **Stage Complete**: AI completes current stage code/documentation
2. **User Confirmation**: User confirms current stage results
3. **Generate Commit Info**: AI automatically generates version number and commit message
4. **User Commits**: User executes Git commands to commit code
5. **Next Stage**: After commit confirmation, AI begins next stage

### Git Command Quick Reference
```bash
# View current status
git status

# View commit history
git log --oneline

# View version differences
git diff v0.1.0 v0.2.0

# Reset to specific version (if needed)
git reset --hard <commit-hash>

# View changes in a specific stage
git show <commit-hash>
```

## Milestone Confirmation

Prompt after each stage completion:
```
✅ 本阶段已完成！

下一步选项：
1. 确认无误，进入下一阶段
2. 修改当前阶段的某些内容
3. 查看当前阶段的核心代码和说明
4. 查看项目整体进度

请输入你的选择（1/2/3/4）：
```

## Quality Checklist

Before completing each stage, AI should self-check:
- [ ] Waited for user confirmation?
- [ ] Code includes detailed Chinese comments?
- [ ] Provided running instructions?
- [ ] Explained technical terms?
- [ ] Output matches current stage objectives by chinse?
- [ ] Provided update summary and version number?

## Common Issue Handling

**Q: User doesn't understand a technical term**
A: Explain using everyday metaphors, e.g., "A function is like a vending machine - you put in parameters (money), and it returns results (drinks)"

**Q: User wants to modify completed stage**
A: Immediately provide Git-based solution: "No problem! We can use Git to go back to a previous version. Which part would you like to modify?"

**Q: User wants additional features**
A: Evaluate complexity, add simple features directly, suggest complex features as future extensions: "That's a great feature! I suggest we complete the core functionality first, then add this as version 2.0. What do you think?"
