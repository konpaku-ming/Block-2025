# 分块算法经典例题讲解 (Block Algorithm Lecture Notes)

本仓库包含四道分块算法经典例题的LaTeX讲义，适合作为PPT使用。

## 文件说明

- `Q1.md` - `Q4.md`: 四道例题的原始题目描述
- `block_lecture.tex`: LaTeX源文件
- `block_lecture.pdf`: 编译后的PDF讲义（23页）

## 例题内容

### 例题1：区间乘法、区间加法与单点查询
- 解法：分块 + 懒标记
- 复杂度：O(n√n)

### 例题2：区间查询与区间赋值
- 解法：分块 + 区间赋值标记
- 复杂度：O(n√n)（均摊）

### 例题3：区间开方与区间求和
- 解法：分块 + 区间和维护
- 复杂度：O(n√n log log V)

### 例题4：区间生长与区间计数
- 解法：分块 + 懒标记 + 块内排序
- 复杂度：O(q√n log n)

## 讲义特点

- ✅ 每道题分3页呈现：题目陈述、解法说明、复杂度分析
- ✅ 使用TikZ绘制可视化图表
- ✅ 大字体，适合PPT演示
- ✅ 支持中文排版

## 如何编译

需要安装XeLaTeX和相关中文字体支持：

```bash
# Ubuntu/Debian
sudo apt-get install texlive-xetex texlive-latex-extra texlive-lang-chinese texlive-fonts-recommended

# 编译
xelatex block_lecture.tex
```

或者直接使用已生成的 `block_lecture.pdf` 文件。

## 页面布局

- 第1页：封面
- 第2-4页：例题1（题目、解法、复杂度）
- 第5-7页：例题2（题目、解法、复杂度）
- 第8-10页：例题3（题目、解法、复杂度）
- 第11-13页：例题4（题目、解法、复杂度）
- 其余页面：每道题的详细解法和可视化
