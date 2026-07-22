# 清华简·《算表》数字化交互矩阵 | Tsinghua Bamboo Slips 'Suanbiao' Digital Matrix

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub](https://img.shields.io/badge/GitHub-dahetech/SUANBIAO-black?logo=github)](https://github.com/dahetech/SUANBIAO)

## 🌟 项目简介 | Project Overview

这是一个**数字人文项目**，旨在用现代网页技术复原约公元前305年、收藏于清华大学的战国时期竹简文物**《算表》**。

本项目以**高度交互式的矩阵动画**展现古代中国数学家如何利用竹简、丝线和位值制原理，实现乘除法、平方与开方运算，是**世界上最早的十进制计算器**的数字化演绎。

**🏅 获吉尼斯世界纪录认证**：最古老的十进制乘法表 (Oldest decimal multiplication table)

---

## 📚 核心特点 | Key Features

### ✨ 交互式古风界面 | Beautiful Ancient-Style UI
- 竹简风格设计，营造真实的历史沉浸感
- 支持中英文双语切换
- 响应式布局，适配桌面和移动设备

### 🧮 完整四则运算演示 | Full Arithmetic Operations
- **乘法** (Multiplication) - 分配律拆解与逐位交叉运算
- **除法** (Division) - 逆向查表与凑数算法  
- **平方** (Square) - 完全对称的朱青双色拉线效果
- **开方** (Square Root) - 对角线十字寻根法

### 🎓 学术严谨性 | Academic Rigor
- 严格遵循文物物理极限 [0.5 ~ 99.5]
- 符合战国楚人的"十进制位值制"原理
- 附带权威学术引用与吉尼斯纪录链接

### 🎨 实时动画演示 | Real-time Animation
- 动态拉线效果展现古人的运算步骤
- 彩色高亮交点与中央弹窗反馈
- 10秒自动关闭的计算结果窗口

---

## 🚀 快速开始 | Quick Start

### 1️⃣ 在线访问（推荐）| Live Demo
直接访问网站，无需本地配置：
```
https://dahetech.github.io/SUANBIAO/
```

### 2️⃣ 本地运行 | Local Setup
```bash
# 克隆仓库
git clone https://github.com/dahetech/SUANBIAO.git

# 进入目录
cd SUANBIAO

# 使用任意 HTTP 服务器打开（例如 Python）
python -m http.server 8000

# 浏览器访问
open http://localhost:8000/index.html
```

### 3️⃣ 一键体验 | Quick Examples
点击页面上的快速示例按钮：
- ✖️ **23 × 18** - 乘法分配律拆解
- ➗ **45 ÷ 15** - 除法逆向推演
- 📐 **12.5²** - 对称平方运算
- 🔍 **√225** - 对角线开方

---

## 📖 项目背景 | Historical Context

### 什么是清华简？| About Tsinghua Bamboo Slips
- **收藏机构**：清华大学
- **收藏时间**：2008年
- **年代**：战国时期（约公元前305年）
- **数量**：近2500支竹简

### 《算表》的意义 | Significance of Suanbiao
《算表》由21支竹简组成，是目前世界发现的**最古老的十进制乘法表**：
- 展现战国时期中国数学的高度发达
- 证明了中国古人在十进制位值制上的卓越理解
- 比西方最早的乘法表早至少1500年

### 权威参考 | Academic References
- **李学勤** 主编：《清华大学藏战国竹简（肆）》，上海辞书出版社，2013年
- **Corey, J.** (2016). *The Tsinghua Calculation Table: Decimal Matrix and Mathematical Thought in Early China*. Journal of Asian Mathematics.
- **吉尼斯世界纪录**：[Oldest decimal multiplication table](https://www.guinnessworldrecords.com/world-records/452049-oldest-decimal-multiplication-table)
- **清华大学官方专题**：[深度解读《算表》](https://www.tsinghua.edu.cn/info/1366/81524.htm)

---

## 🛠️ 技术栈 | Tech Stack

| 组件 | 技术 |
|------|------|
| **前端框架** | 纯 HTML5 + CSS3 + JavaScript（无依赖）|
| **交互动画** | CSS animations + DOM manipulation |
| **样式设计** | 古风渐变、阴影、投影、响应式栅栏 |
| **多语言** | i18n 国际化（中文 + 英文）|
| **部署** | GitHub Pages 静态托管 |

---

## 📁 项目结构 | Project Structure

```
SUANBIAO/
├── index.html              # 主应用文件（包含全部 HTML/CSS/JS）
├── README.md               # 项目文档
└── (无外部依赖)
```

**设计理念**：采用单文件架构，无任何外部依赖，便于部署与维护。

---

## 🧩 核心功能详解 | Core Functions

### 1. 矩阵初始化 `initMatrix()`
生成 19×19 的乘法表矩阵，行列标题分别为：
- **列标题**（乘数）：0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 20, 30, 40, 50, 60, 70, 80, 90
- **行标题**（被乘数）：反向排列

### 2. 数字拆解 `splitNumberCorrected()`
将输入数字按"十进制位值制"规则拆解：
- **例**：23 → [20, 3]
- **例**：12.5 → [10, 2, 0.5]

### 3. 动画渲染 `executeSuanbiaoAnimation()`
- 拉线动画（40ms 间隔）
- 交点高亮与计算
- 结果弹窗展示

### 4. 多语言切换 `switchLanguage()`
支持中英文即时切换，所有界面文本双语化

---

## 📋 使用示例 | Usage Examples

### 示例1：计算 23 × 18
1. 选择"✖️ 乘法模式"
2. 输入 乘数: **23**，被乘数: **18**
3. 点击"拉线运筹"按钮
4. 观察动画：
   - 23 拆为 [20 + 3]
   - 18 拆为 [10 + 8]
   - 4个交点：20×10, 20×8, 3×10, 3×8
   - 结果 = 200 + 160 + 30 + 24 = **414**

### 示例2：计算 √225
1. 选择"🔍 求开方模式"
2. 输入 被开方数: **225**
3. 点击"拉线运筹"按钮
4. 系统在对角线上寻找合适的拆解方案
5. 结果 = **15.0**

---

## ⚠️ 使用限制 | Constraints

根据文物物理特性，本系统有以下限制：

| 运算类型 | 范围限制 | 说明 |
|---------|--------|------|
| 乘法 | 0.5 ~ 99.5 | 整数或 .5 小数 |
| 平方 | 0.5 ~ 99.5 | 同乘法 |
| 除法 | 0.25 ~ 9900.25 | 支持扩展因子 |
| 开方 | 0.25 ~ 9900.25 | 同除法 |

---

## 🌐 交流与讨论 | Community & Discussion

欢迎数学爱好者、数据科学探索者参与学术讨论：

- **GitHub Discussions**：[加入讨论社区](https://github.com/dahetech/SUANBIAO/discussions/1)
- **联系开发者**：suanbiao@outlook.com
- **反馈建议**：欢迎提交 [Issues](https://github.com/dahetech/SUANBIAO/issues)

---

## 👨‍💻 项目信息 | About Developer

- **开发者**：一名热爱中国历史文化的学生
- **项目初衷**：出于对清华简《算表》的好奇，以及对两千年前古人惊人智慧的由衷自豪
- **技术目标**：用现代网页前端技术演绎古代数学智慧，让更多人了解中国数学的辉煌历史

---

## 📜 许可证 | License

本项目采用 **MIT License**。详见 [LICENSE](LICENSE) 文件。

---

## 🙏 致谢 | Acknowledgments

- **清华大学**：感谢收藏与研究《算表》的学术工作
- **李学勤教授**及学术团队：感谢详尽的研究资料
- **吉尼斯世界纪录**：认证《算表》的历史地位
- **开源社区**：灵感来自数字人文项目

---

## 📞 反馈与支持 | Feedback & Support

- 🐛 **发现 Bug**？提交 [Issue](https://github.com/dahetech/SUANBIAO/issues)
- 💡 **有建议**？欢迎讨论
- 📧 **直接邮件**：suanbiao@outlook.com

---

**✨ 简丝编织，数字交汇——让古人的智慧重获生命！**

*Intersecting Threads of Ancient Numbers — Bringing Ancient Wisdom to Digital Life!*
