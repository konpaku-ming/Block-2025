# 分块算法经典例题讲解 (Block Algorithm Lecture Notes)

本仓库包含四道分块算法经典例题的LaTeX讲义，适合作为PPT使用。

## 文件说明

- `Q1.md` - `Q4.md`: 四道例题的原始题目描述
- `block_lecture.tex`: LaTeX源文件
- `block_lecture.pdf`: 编译后的PDF讲义（23页）
- `block_lecture.pptx`: PowerPoint演示文稿（13页，由generate_pptx.py自动生成）
- `generate_pptx.py`: 用于从LaTeX内容生成PPTX的Python脚本
- `template.pptx`: 中文风格PPT模板（用于美化演示文稿）
- `Template2.pptx`: 现代专业PPT模板（用于美化演示文稿）
- `beautify_pptx.py`: 使用模板美化PPT的Python脚本
- `block_lecture_beautified_v1.pptx`: 使用template.pptx模板美化后的演示文稿
- `block_lecture_beautified_v2.pptx`: 使用Template2.pptx模板美化后的演示文稿（推荐使用，数学公式使用Unicode符号）
- `convert_math_to_latex.py`: ⚠️ 已弃用 - LaTeX公式在PowerPoint中无法正常渲染
- `block_lecture_beautified_v2_latex.pptx`: ⚠️ 不推荐 - LaTeX格式公式在PowerPoint中显示为纯文本

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

### LaTeX编译
需要安装XeLaTeX和相关中文字体支持：

```bash
# Ubuntu/Debian
sudo apt-get install texlive-xetex texlive-latex-extra texlive-lang-chinese texlive-fonts-recommended

# 编译
xelatex block_lecture.tex
```

或者直接使用已生成的 `block_lecture.pdf` 文件。

### PowerPoint生成
需要安装Python和python-pptx库：

```bash
# 安装依赖
pip install python-pptx

# 生成基础PPTX
python3 generate_pptx.py

# 美化PPTX（使用模板）
python3 beautify_pptx.py
```

或者直接使用已生成的文件：
- `block_lecture.pptx` - 基础版本
- `block_lecture_beautified_v1.pptx` - 使用template.pptx美化（中文风格）
- `block_lecture_beautified_v2.pptx` - 使用Template2.pptx美化（现代专业风格）**[推荐]**

### ⚠️ 关于数学公式显示

**重要提示：PowerPoint使用Unicode数学符号，不使用LaTeX格式**

在PowerPoint中：
- ✅ **正确做法**：使用Unicode数学符号（√、₁、₂、≥ 等），这些符号可以在PowerPoint中正常显示
- ❌ **错误做法**：使用LaTeX格式（如 `$\sqrt{n}$`, `$a_{1}$`, `$\geq$` 等），这些在PowerPoint中会显示为纯文本，无法渲染

`block_lecture_beautified_v2.pptx` 使用Unicode符号，可以在PowerPoint中正常显示数学公式。

⚠️ **注意**：`convert_math_to_latex.py` 脚本已弃用，因为LaTeX格式在PowerPoint中无法正常渲染。请不要使用该脚本。

## 页面布局

### PDF版本（23页）
- 第1页：封面
- 第2-4页：例题1（题目、解法、复杂度）
- 第5-7页：例题2（题目、解法、复杂度）
- 第8-10页：例题3（题目、解法、复杂度）
- 第11-13页：例题4（题目、解法、复杂度）

### PowerPoint版本（13页）
- 第1页：标题页
- 第2-4页：例题1（题目、解法、复杂度）
- 第5-7页：例题2（题目、解法、复杂度）
- 第8-10页：例题3（题目、解法、复杂度）
- 第11-13页：例题4（题目、解法、复杂度）

每道题的3页内容包含完整的题目描述、解法说明（含可视化图表）和复杂度分析。
