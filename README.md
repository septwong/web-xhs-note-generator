# 小红书图文生成器

一个纯静态的 HTML 应用，用于快速生成小红书笔记图文和封面图片。支持 Markdown 编辑、多主题风格、图片管理与批量导出。

## 在线使用

直接在浏览器中打开 `index.html` 即可使用，无需任何服务器或构建工具。

## 功能特性

### 📝 图文生成器
- **Markdown 编辑** - 支持标准 Markdown 语法，实时预览
- **多主题风格** - 4 种预设主题（极简、衬线、酸性、科技）
- **智能分页** - `@---` 分隔符支持多页内容自动分页
- **图片管理** - 拖拽粘贴上传、本地图片引用、图片库管理
- **批量导出** - 支持单张/批量导出高质量 JPG/PNG
- **状态持久化** - 自动保存草稿至 localStorage

### 🎨 封面生成器
- **爆款模板** - 4 种小红书爆款封面模板
- **自定义配置** - 支持图片、标题、日期、作者信息定制
- **高清导出** - 2x 像素比例，保证输出质量

## 项目结构

```
web-xhs-note-generator/
├── index.html              # 入口页面（工具导航）
├── views/
│   ├── note.html          # 图文编辑器（三栏布局）
│   └── cover.html         # 封面生成器
├── fonts/
│   ├── fonts.css          # 字体定义文件
│   ├── Inter-Regular.ttf  # Inter 字体Regular
│   ├── Inter-Bold.ttf     # Inter 字体Bold
│   ├── NotoSansSC-Regular.ttf  # 思源黑体Regular
│   └── NotoSansSC-Bold.ttf     # 思源黑体Bold
├── favicon.svg
└── README.md
```

## 技术栈

- **纯原生 HTML/CSS/JS** - 无构建工具，零依赖
- **Marked.js** - Markdown 解析
- **html-to-image** - 图片导出
- **JSZip + FileSaver** - 批量打包下载
- **Tailwind CSS** - UI 样式（通过 CDN）

## 使用说明

### 快速开始

```bash
# 直接在浏览器中打开
open index.html
# 或者在任意浏览器中打开 index.html 文件
```

### Markdown 语法

- `# 标题` - 一级标题
- `## 副标题` - 二级标题
- `文本内容` - 正文段落
- `![img](img:{id})` - 引用已上传的图片
- `@---` - 分页符（用于多页内容）

### 图片管理

1. **上传图片**：点击右侧面板的"选择图片"按钮，或粘贴图片（Ctrl+V）
2. **引用图片**：在 Markdown 中使用 `![img](img:{id})` 格式
3. **管理图片**：右侧面板的图片管理区域可预览、删除已上传图片

## 主题预览

| 主题 | 说明 |
|------|------|
| **minimal** | 柔和的蓝白配色，适合清新风格 |
| **serif** | 衬线字体排版，适合文艺风格 |
| **acid** | 高对比度酸性绿，适合个性风格 |
| **tech** | 深色网格背景，适合科技风格 |

## 浏览器支持

- Chrome / Edge（推荐）
- Firefox
- Safari
- Opera

## 开源协议

MIT License

## 相关链接

- [小红书官网](https://www.xiaohongshu.com)
