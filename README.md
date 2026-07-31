# KOReader Tools

一组面向 Kindle 与 KOReader 用户的实用小工具，来自日常阅读中的真实需求，并通过 AI 辅助的 Vibe Coding 方式持续开发和改进。

目前包含：

1. **Kindle 漫画助手**：处理 EPUB 漫画，使其通过 Send to Kindle 传输后更容易被识别为漫画。
2. **KOReader 竖排字体转换器**：生成可与原字体并存的竖排字体，在保留 KOReader 原生阅读功能的同时实现间接竖排阅读。

> [English version](#english)

> [!IMPORTANT]
> 本项目是个人制作的非官方工具，与 Amazon、Kindle 或 KOReader 官方无关。使用前请备份原始文件。

## 1. Kindle 漫画助手

用于处理 EPUB 漫画的格式与相关信息，使文件通过 **Send to Kindle** 传输后能够以漫画形式识别。

### 主要功能

- 处理 EPUB 漫画文件
- 改善 Kindle 对漫画格式的识别
- 简化 Send to Kindle 传输前的准备工作

### 使用方法

1. 备份原始 EPUB 漫画。
2. 打开 Kindle 漫画助手。
3. 选择需要处理的 EPUB 文件和输出位置。
4. 开始转换并等待完成。
5. 使用 Send to Kindle 上传转换后的文件。
6. 在 Kindle 上下载并检查阅读效果。

> [!WARNING]
> Send to Kindle 仍可能压缩图片，因此转换工具无法保证原始画质被完整保留。对画质要求较高时，请同时保留未经转换的原文件。

<img width="2560" height="1388" alt="Kindle 漫画助手" src="https://github.com/user-attachments/assets/310cfba2-7208-4299-9487-52fbe107bf29" />

## 2. KOReader 竖排字体转换器 v1

该工具将普通字体转换为适合间接竖排阅读的独立字体。KOReader 仍然使用原生 TXT/EPUB 阅读器，因此脚注链接、选词、字典、批注、书签、搜索和阅读进度等功能可以继续保留。

### 快速使用

1. 双击 `KOReader-Vertical-Font-Converter-v1.exe`。
2. 选择原来的 `.ttf` 字体。
3. 保持默认后缀 `Vertical`，点击“生成独立竖排字体”。
4. 将生成的新字体复制到 `koreader/fonts/`。
5. 完全重启 KOReader。
6. 打开 TXT 或 EPUB，选择新字体，例如“仓耳今楷 Vertical”。
7. 将 KOReader 屏幕顺时针旋转 90°。

生成字体的内部名称会被重写，因此原字体与竖排字体可以同时出现在 KOReader 的字体列表中，不会互相替换。转换器不会原地修改原字体。

### 支持范围

- `.ttf` 字体
- 使用 TrueType `glyf` 轮廓的 `.otf` 字体
- 常见中文、日文竖排标点替换（原字体包含相应竖排字形时）

暂不支持：

- CFF/CFF2 轮廓的 OTF 字体
- 可变字体
- 彩色字体及位图字体的彩色或位图层

遇到不支持的字体时，转换器会停止并给出提示，不会改动原文件。

### 命令行用法

```powershell
KOReader-Vertical-Font-Converter-v1.exe 原字体.ttf 输出字体.ttf
```

如果准备在 KOReader 中逆时针旋转屏幕：

```powershell
KOReader-Vertical-Font-Converter-v1.exe 原字体.ttf 输出字体.ttf --screen-rotation counterclockwise
```

<img width="899" height="548" alt="KOReader 竖排字体转换器" src="https://github.com/user-attachments/assets/6c0b1e19-a2d7-4255-ade7-f3e55a6af720" />

<img width="1680" height="1264" alt="KOReader 竖排阅读效果" src="https://github.com/user-attachments/assets/dd6705dd-c10e-42d1-b67a-865be20f0061" />

## 使用提醒

- 操作前请备份原始电子书和字体文件。
- 只转换你有权修改和自用的字体；部分商业字体许可证禁止修改或重新分发。
- Kindle、KOReader 或系统版本更新后，实际效果可能发生变化。
- 本项目仍在持续改进，欢迎通过 Issues 提交问题和建议。

---

<a id="english"></a>

# English

A small collection of practical utilities for Kindle and KOReader users. These tools grew out of real reading needs and are being developed and improved through AI-assisted vibe coding.

The repository currently includes:

1. **Kindle Manga Assistant** — processes EPUB manga so that files sent through Send to Kindle are more likely to be recognized as comics.
2. **KOReader Vertical Font Converter** — creates a separate vertical-reading font while preserving KOReader's native reading features.

> [!IMPORTANT]
> This is an unofficial personal project and is not affiliated with Amazon, Kindle, or the KOReader project. Back up your original files before using any tool.

## 1. Kindle Manga Assistant

This tool processes EPUB manga and related information so that files transferred through **Send to Kindle** can be recognized as comics.

### Features

- Processes EPUB manga files
- Improves comic-format recognition on Kindle
- Simplifies preparation before using Send to Kindle

### Usage

1. Back up the original EPUB manga.
2. Open Kindle Manga Assistant.
3. Select the EPUB file and an output location.
4. Start the conversion and wait for it to finish.
5. Upload the converted file with Send to Kindle.
6. Download it on your Kindle and check the result.

> [!WARNING]
> Send to Kindle may still compress images. This tool cannot guarantee that the original image quality will be fully preserved. Keep an unmodified copy when image quality matters.

<img width="2560" height="1388" alt="Kindle Manga Assistant" src="https://github.com/user-attachments/assets/310cfba2-7208-4299-9487-52fbe107bf29" />

## 2. KOReader Vertical Font Converter v1

This tool converts a regular font into a separate font intended for an indirect vertical-reading setup. KOReader continues to use its native TXT/EPUB reader, so footnote links, text selection, dictionaries, annotations, bookmarks, search, and reading progress remain available.

### Quick start

1. Run `KOReader-Vertical-Font-Converter-v1.exe`.
2. Select the original `.ttf` font.
3. Keep the default `Vertical` suffix and click the button to generate a separate vertical font.
4. Copy the generated font to `koreader/fonts/`.
5. Restart KOReader completely.
6. Open a TXT or EPUB book and select the new font, such as “LXGW WenKai Vertical”.
7. Rotate the KOReader screen 90° clockwise.

The converter rewrites the font's internal names, allowing the original and converted fonts to coexist in KOReader's font list. It never modifies the original font in place.

### Supported fonts

- `.ttf` fonts
- `.otf` fonts using TrueType `glyf` outlines
- Common Chinese and Japanese vertical punctuation substitutions when the source font contains the corresponding glyphs

Currently unsupported:

- OTF fonts using CFF/CFF2 outlines
- Variable fonts
- Color or bitmap layers in color and bitmap fonts

When an unsupported font is detected, the converter stops with a message and leaves the original file unchanged.

### Command-line usage

```powershell
KOReader-Vertical-Font-Converter-v1.exe input-font.ttf output-font.ttf
```

If you plan to rotate the KOReader screen counterclockwise:

```powershell
KOReader-Vertical-Font-Converter-v1.exe input-font.ttf output-font.ttf --screen-rotation counterclockwise
```

<img width="899" height="548" alt="KOReader Vertical Font Converter" src="https://github.com/user-attachments/assets/6c0b1e19-a2d7-4255-ade7-f3e55a6af720" />

<img width="1680" height="1264" alt="Vertical reading in KOReader" src="https://github.com/user-attachments/assets/dd6705dd-c10e-42d1-b67a-865be20f0061" />

## Notes

- Back up original books and font files before conversion.
- Only convert fonts that you are licensed to modify and use. Some commercial font licenses prohibit modification or redistribution.
- Results may change after Kindle, KOReader, or operating-system updates.
- The project is still evolving. Issues and suggestions are welcome through GitHub Issues.
这个库里添加的是我在使用kindle和koreader的过程中结合需求vibecoding的一些软件。
1.kindle漫画助手
  转换漫画格式，是epub漫画使用sendtokindle传输的时候可以被识别为漫画格式，但是需要注意的是，使用sendtokindle仍然会压缩画质。
<img width="2560" height="1388" alt="image" src="https://github.com/user-attachments/assets/310cfba2-7208-4299-9487-52fbe107bf29" />
2.Vertical-Font-Converter-v1
  可以进行任意字体转换，在koreader上实现间接竖排。
<img width="899" height="548" alt="image" src="https://github.com/user-attachments/assets/6c0b1e19-a2d7-4255-ade7-f3e55a6af720" />

<img width="1680" height="1264" alt="Reader_红楼梦脂评汇校本-繁体竖排版 (BookDNA经典复刻_ (z-library sk, 1lib sk, z-lib sk) epub_p45_2026-07-31_113845" src="https://github.com/user-attachments/assets/dd6705dd-c10e-42d1-b67a-865be20f0061" />
