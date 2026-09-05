# 轻爽课表

轻爽课表是一个单文件版课表生成器，面向班级、教师和家长日常制作课程表使用。项目不依赖后端服务，也不需要安装软件，打开网页即可填写、调整、打印或保存为 PDF。

## 成品展示

在线访问地址将在 GitHub Pages 开启后生效：

https://excelov.github.io/qingshuang-kebiao/

本地预览可以直接打开：

`index.html`

页面提供班级与学期填写、课程定义、上下晚节次数调整、作息时间自动推算、课程格点选填入、配色切换、打印和导出 PDF 等功能。

## 版权与使用许可

Copyright (c) 2026 轻爽课表项目组. All rights reserved.

本仓库公开用于项目展示、版本管理和在线访问，不代表授予复制、修改、再发布或商业使用许可。未经版权所有者书面许可，不得直接复制本项目的源代码、页面文案、视觉设计、配色方案或品牌标识。详细条款见仓库根目录的 [`LICENSE`](LICENSE) 文件。

## 主要功能

- 单文件运行：全部 HTML、CSS、JavaScript 集成在 `index.html` 中。
- 课表编辑：选择课程后点击课表格即可填入，也可以清除单元格。
- 作息配置：支持设置上午开始时间、每节课时长、课间、午休和晚休。
- 节次数调整：可分别调整上午、下午、晚上节数。
- 星期范围：可切换周一至周五、周一至周六或周一至周日。
- 课程颜色：每门课程可单独选择颜色，未自定义时使用当前古典配色。
- 本地保存：浏览器会通过 `localStorage` 保存已填写内容。
- 打印输出：可直接打印，也可通过浏览器打印功能保存为 PDF。
- 配色切换：内置多套中国古典配色方案。
- 移动端：手机上可在课表、编辑面板和课程库之间分段切换。

## 使用方法

1. 打开网页后填写班级、学期。
2. 在左侧设置作息时间和节次数。
3. 在编辑面板选择星期范围，并在课程库定义课程和颜色。
4. 点击课表中的格子填入课程。
5. 使用“打印 / 存 PDF”输出最终课表。

## 维护指南

本项目采用单文件结构，日常维护只需要修改 `index.html`。

常见维护位置：

- 页面样式：修改 `<style>` 标签内 CSS。
- 默认课程：修改 JavaScript 中的 `DEFAULT.courses`。
- 默认课表：修改 JavaScript 中的 `DEFAULT.grid`。
- 默认作息：修改 JavaScript 中的 `DEFAULT.time` 和 `DEFAULT.counts`。
- 配色方案：修改 JavaScript 中的 `SCHEMES`。
- 本地存储键名：修改 `KEY`，更换后会相当于清空旧浏览器缓存数据。

维护建议：

- 每次修改前先复制一份 `index.html` 作为备份。
- 修改后用 Chrome 或 Edge 打开本地文件检查页面是否正常。
- 重点检查课程填写、清除、节次数调整、打印预览和移动端显示。
- 如果发布到 GitHub Pages，只需要更新仓库根目录的 `index.html`。

## 文件结构

```text
.
├── index.html   # 轻爽课表主程序
├── README.md    # 项目说明与维护指南
└── .nojekyll    # GitHub Pages 静态发布标记
```

## 发布说明

仓库推送后，在 GitHub 仓库中进入 `Settings -> Pages`，选择：

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/ (root)`

保存后等待 GitHub Actions/Pages 构建完成，即可通过 `https://excelov.github.io/qingshuang-kebiao/` 访问。
