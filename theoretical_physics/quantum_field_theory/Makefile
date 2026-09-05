# 定义变量
TEX = xelatex
BIBTEX = bibtex
TARGET = 量子场论笔记# 你的主文件名（不带 .tex）

all: $(TARGET).pdf

# 生成最终PDF的规则
$(TARGET).pdf: $(TARGET).tex
	$(TEX) $(TARGET).tex   # 第一次编译，生成 .aux 等辅助文件
	$(BIBTEX)  $(TARGET).aux       # 处理参考文献，生成 .bbl 文件
	$(TEX) $(TARGET).tex   # 第二次编译，引入参考文献
	$(TEX) $(TARGET).tex   # 第三次编译，修正所有交叉引用

# 清理辅助文件
clean:
	rm -f *.aux *.log *.toc *.out *.gz *.fls *.fdb_latexmk *.synctex\(busy\) *.bbl *.blg *.acn *.acr *.alg *.glg *.glo *.gls *.ist *.lof *.lot *.maf *.mtc* *.nav *.snm *.vrb