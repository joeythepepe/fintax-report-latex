# FinTax 报告 LaTeX 工程

已排版官网英文报告 **Crypto Miners Pivot to AI Data Centers: U.S. State Tax Incentives and Key Considerations**（2026-08-25）。

## 编译

本机已具备 MacTeX（pdflatex、latexmk）。在此目录执行 `make release`。
正式输出：`output/pdf/FinTax_AI_Data_Center_Tax_Incentives_EN.pdf`。
编译记录及 SyncTeX 保留在 `build/`；`make clean` 仅清理编译产物，保留发布 PDF。
所有路径相对此工程，工程移动后可重新编译，无需联网。

## 从哪里修改

- `main.tex`：只管理文档顺序，使用 `\input` 组合编号 section。
- `preamble.tex`：A4 页边距、Times 系字体、11pt 正文（字号在 main.tex）、1.15 倍行距、段首缩进、标题、图注、页眉页脚和 FinTax 颜色。
- `metadata.tex`：报告标题、副标题、日期、发布方、链接及 PDF 元数据。
- `sections/00_cover.tex`：封面。
- `sections/01_*.tex` 至 `05_*.tex`：官网五个正文 section；第三节继续使用 subsection。调整正文无需碰 preamble。
- `sections/06_source_note.tex`：来源及 PDF 版本说明。
- `assets/`：六幅官网原图及 FinTax 矢量 logo；三幅表格原图保留作核对，PDF 中已使用 LaTeX 表格替换。
- `tables/`：三张可编辑的 LaTeX 表格，白底、黑字、0.4pt 细线框；共享样式为 `preamble.tex` 中的 `\ReportTableSetup`。Texas 表中两类项目相同的共同要求合并展示一次。
- `references.bib`：后续加入经核实引用时使用，目前没有编造文献。
- `sources/`：完整网页 Markdown 快照、来源与下载日期、图片 URL，便于逐段核对。

## 排版依据与内容边界

沿用模块化论文工程的章节拆分、Times 系字体、段落规范、A4 和 Makefile 工作流。该报告使用左对齐编号标题，新增 FinTax 封面、目录、页眉页脚，以便用于官网报告下载。

保留官网英文正文和六幅图；未翻译、改写或更新原报告的税务判断。网页没有独立参考文献表，因此没有补造引用。封面、目录和来源说明是本次新增排版内容。三张表格已改为矢量文字和线框；地图与截图仍保留原图。

官网栏目为 https://www.fintax.tech/reports 。本工程位于共享仓库的 EN/ 目录；PDF 可独立下载，官网未修改。
