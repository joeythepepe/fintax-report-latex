# FinTax 报告 LaTeX 中文工程

本工程从英文版 FinTax-Report-LaTeX 独立复制，保留相同的文件名、章节拆分、封面布局和黑白线框表格。正文和表格依据英文稿翻译，为待审校的中文排版初稿；未与官网中文原稿核对。地图及申请表截图仍为英文原图。

## 编译

安装完整 TeX Live 或 MacTeX（含 XeLaTeX、latexmk、ctex 和 Fandol 字体），进入工程根目录执行：

```sh
make release
```

输出：`output/pdf/FinTax_AI_Data_Center_Tax_Incentives_ZH.pdf`。
编辑器需选用 **XeLaTeX**，不要使用 pdfLaTeX。所有 TeX 文件均为 UTF-8。
中文字体使用 TeX Live 自带的 Fandol，英文字体使用 TeX Gyre Termes / Heros，无 macOS 专属字体及绝对路径依赖。复制或从 GitHub 拉取到另一台安装完整 TeX Live 的电脑后，可用相同命令编译；其他电脑尚未实测。

## 文件管理

- `main.tex`：中文文档类、目录说明和 `\input` 顺序。
- `preamble.tex`：中文与英文字体、A4 页边距、行距、首行缩进、标题、图注、页眉页脚、共享表格样式。
- `metadata.tex`：中文标题、日期、发布方、英文原文链接及 PDF 元数据。
- `sections/`：封面、五个编号正文 section，以及来源说明；文件名与英文工程相同。
- `tables/`：三张可编辑的中文黑白细线框表格。
- `assets/`：原图与矢量 logo，原始表格图片保留用于核对。
- `sources/`：英文网页快照、来源记录和中文翻译说明。
- `references.bib`：沿用英文版的空参考文献文件；原文没有独立文献表。
- `build/`：本地编译记录、辅助文件及 SyncTeX。
- `output/pdf/`：可供发布的 PDF。

## 后续上传 GitHub

`.gitignore` 已排除 build 内的编译产物、SyncTeX 和 `.DS_Store`，保留源码、素材、来源说明和 output/pdf 内的成品。不需要上传临时预览图片或本地环境文件。本工程与英文版一并收录在仓库的 ZH/ 目录。

英文工程保持独立，修改中文工程不会同步修改英文版。以后更新正文时，应同时审校两种语言；两种语言分别维护和编译。

## 内容边界

中文稿保留英文版的章节和数据，税务论述保持2026年8月25日原报告的发表语境，未新增法规核查。表2的共同要求仍合并展示一次并注明适用于两类项目。发布前请审校翻译及专业用语。
