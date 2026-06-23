# Ogden 基础英语 850 词 · 中文背诵版

一个单文件 HTML 学习工具，用于帮助中文母语者系统背诵 C. K. Ogden 提出的 850 词 Basic English 词表。

## 这是什么

1930 年，英国学者 Charles Kay Ogden 提出 **Basic English**——一套仅用 850 个英文单词构成的受控语言，理论上足以表达日常与多数书面内容。这份词表至今仍是 ESL/EFL 教学中最常被引用的核心词表之一。

本项目把 Ogden 的 850 词重新整理成一份适合中文学习者背诵的交互页面，每个词配有：词性 · 音标 · 英文简义 · 中文简义 · 一键发音 · OED 词典直达链接。

## 词表来源与分类

词表来源于 Ogden 原始字母序 850 词 PDF，按 Ogden 官方 **5 大类** 重新分组（来源：Simple English Wikipedia 的 ordered wordlist）：

| 类别 | 英文名 | 词数 | 类别色 |
|---|---|---:|---|
| 操作词 | Operations | 100 | 蓝 |
| 通用事物 | Things — General | 400 | 橙 |
| 象形事物 | Things — Picturable | 200 | 绿 |
| 通用品质 | Qualities — General | 100 | 紫 |
| 反义品质 | Qualities — Opposites | 50 | 红 |
| **合计** |  | **850** |  |

- 词性 · 音标 · 英文简义：参考 Ogden「互释」精神 + 朗文 / 牛津风格简明释义
- 中文简义：精炼翻译，多义词用顿号分隔主要义项
- 每张卡片链接到 `oed.com` 对应词条页（OED 全文需订阅，链接便于随时深查历史释义）

## 使用方法

直接双击 `Ogden_850_背诵版.html` 在任意现代浏览器中打开即可，**无需联网、无需安装**。发音调用浏览器自带的 Web Speech API。

### 主要功能

- **类别筛选**：顶部 5 个分类 Tab + 「全部」
- **A–Z 字母索引**：快速跳转到指定字母开头的词
- **全文搜索**：支持英文单词、中文释义、英文释义、词性、音标模糊匹配
- **背诵 + 掌握 双 checkbox**：每张卡片可分别标记「已背诵」（蓝）与「已掌握」（绿），进度自动保存在浏览器 `localStorage` 中，刷新不丢
- **顶部进度条**：蓝色段=已背诵但未掌握，绿色段=已掌握，直观看到推进
- **随机抽背模式**：点「随机抽背」进入全屏 Flashcard
  - 按「未背 > 已背 > 已掌握」3:2:1 加权抽取，越不熟的词越可能出现
  - 默认**自动跳过已掌握**的词（可勾选「包含已掌握」反转）
  - 快捷键：`空格`/`回车` 翻面 · `→` 下一个 · `←` 跳过 · `Y` 掌握 · `N` 不熟 · `Esc` 退出
- **一键发音**：每张卡片左下角的喇叭按钮
- **暗色模式**：自动跟随系统
- **响应式**：桌面 / 平板 / 手机自适应

## 项目结构

```
.
├── Ogden_27s_20Basic_20English_20Words_20List_20alphabetic.pdf  # 原始词表 PDF
├── Ogden_850_背诵版.html                                          # 最终学习页面（单文件）
└── README.md
```

## 数据完整性

850 个单词均经过脚本验证：

- 5 大类词数与官方期望值 `100 / 400 / 200 / 100 / 50` 完全一致
- 类别内无重复词
- 跨类别无重复词
- 全部 850 词字段（词性 / 音标 / 英文 / 中文）齐备

## 相关链接

- [Basic English — Wikipedia](https://en.wikipedia.org/wiki/Basic_English)
- [Wikipedia:Basic English ordered wordlist](https://simple.wikipedia.org/wiki/Wikipedia:Basic_English_ordered_wordlist)
- [Oxford English Dictionary (OED)](https://www.oed.com/) — 用于查阅每个词的权威历史释义
- Charles Kay Ogden. *Basic English: A General Introduction with Rules and Grammar*. London: Paul, Trench, Trubner & Co., 1930.

## License

词表本身为 Ogden 公开发表的历史资料（1930 年初版）；本仓库的整理工作（HTML 页面、中文释义、交互设计）按 [MIT License](LICENSE) 发布，欢迎自由使用、修改、分发。
