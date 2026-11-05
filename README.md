# FinTax Report LaTeX / 中英文报告排版工程

同一篇 FinTax 报告的英文与简体中文 LaTeX 工程，供团队共同修改排版。

报告：**Crypto Miners Pivot to AI Data Centers: U.S. State Tax Incentives and Key Considerations** / **加密矿企转型 AI 数据中心：美国各州税收优惠与关键考量**。

原文发布日期：2026-08-25。[FinTax 英文原文](https://www.fintax.tech/reports/crypto-miners-pivot-to-ai-data-centers-u-s-state-tax-incentives-and-key-considerations)。

## 查看 PDF

- [English PDF](EN/output/pdf/FinTax_AI_Data_Center_Tax_Incentives_EN.pdf)
- [中文 PDF](ZH/output/pdf/FinTax_AI_Data_Center_Tax_Incentives_ZH.pdf)

## 目录

```text
EN/                 English project / pdfLaTeX
ZH/                 简体中文工程 / XeLaTeX
  main.tex          文档顺序
  metadata.tex      标题、日期和 PDF 信息
  preamble.tex      字体、边距、行距、标题及黑白表格样式
  sections/         封面、编号章节和来源说明
  tables/           三张可编辑的黑白线框表格
  assets/           原始图片与矢量 logo
  sources/          网页快照和版本来源
  output/pdf/       成品 PDF
```

EN/ 和 ZH/ 均有相同的文件组织方式；更详细的修改位置见各自 README。

## 编译

安装完整 TeX Live 或 MacTeX，需包含 latexmk、pdfLaTeX、XeLaTeX、ctex、Fandol 和 TeX Gyre 字体。从仓库根目录执行：

```sh
make -C EN release
make -C ZH release
```

两份 PDF 分别写入 EN/output/pdf/ 和 ZH/output/pdf/。中文稿使用 TeX Live 自带字体，不依赖 macOS 专属字体。

修改 sections/ 中的正文或 tables/ 中的数据后，在对应语言目录重新运行 make release，并一起提交源码和更新的 PDF。build/ 中的编译文件已忽略。

## 内容状态

中文稿为依据英文稿翻译的排版初稿，尚未与官网中文原稿核对，发布前需审校。地图及申请表截图保留英文原图。政策论述保持原报告发表时的语境，未另外更新法规。

这两个工程分别维护，没有自动同步翻译。仓库公开可读；直接推送修改仍需要仓库写权限。报告及品牌素材的权利归相应权利人，本仓库未另行授予开源许可。
