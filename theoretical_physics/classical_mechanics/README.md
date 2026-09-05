# 中文 LaTeX 书籍项目

这是一个中文 LaTeX 书籍示例项目，包含数学公式和 TikZ 绘图。

## 编译

推荐使用 `xelatex`，因为它对中文字体支持较好：

```bash
cd /home/licheng/Documents/note/classical_mechanics
make
```

如果没有 `make`，可以直接运行：

```bash
xelatex main.tex
xelatex main.tex
```

## 主要文件

- `main.tex` - 主文档，使用 `ctex`、`amsmath` 和 `tikz`。
- `Makefile` - 简单编译脚本。

## 清理临时文件

```bash
make clean
```
