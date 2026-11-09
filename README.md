

I use Chinese, so some descriptions may be inaccurate after translation. When submitting files, you do not need to use your native language, and you do not need to translate them into English before submitting (because I cannot read anything except Chinese, so there is no need to do so).
# Minecraft Block JSON Generator / 我的世界方块 JSON 生成器

A lightweight, web-based tool to quickly generate Minecraft resource pack JSON files for **Walls**, **Fences**, and **Fence Gates**.
一个轻量级的网页工具，用于快速生成**围墙**、**栅栏**和**栅栏门**的 Minecraft 资源包 JSON 文件。

## ✨ Features / 功能特性

- 🧱 **Supports 3 Types**: Wall, Fence, and Fence Gate. / **支持三种类型**：围墙、栅栏、栅栏门。
- 📦 **Batch Generation**: Input multiple names separated by commas or newlines (e.g., `oak, spruce`). / **批量生成**：使用逗号或换行符分隔输入多个名称。
- 🗂️ **Custom Directories**: Choose to generate only `blockstates`, `models`, `items`, or all of them. / **自定义目录**：可选择只生成 `blockstates`、`models`、`items` 或全部。
- 📥 **Download Tracking**: Real-time download counters prevent you from downloading the same file twice. / **下载追踪**：实时记录下载次数，防止重复下载。
- 🖥️ **Widescreen UI**: Adaptive grid layout perfectly fits your PC monitor. / **宽屏界面**：自适应网格布局，完美适配电脑屏幕。
- 🧹 **Auto Formatting**: Automatically removes duplicate suffixes (like `_fence`) and converts spaces to underscores. / **自动格式化**：自动去除重复后缀，并将空格转为下划线。

## 🚀 How to Use / 如何使用

1. **Download/Clone** this repository. / **下载或克隆**本仓库。
2. Open `index.html` in any modern web browser. / 在任何现代浏览器中打开 `index.html`。
3. Enter the base block material name (e.g., `oak`). / 输入基础方块材质名称（如 `oak`）。
4. Select the generation type (Wall / Fence / Fence Gate) and the directories you need. / 选择生成类型和需要的目录。
5. Click **Generate Files**. You can preview and download the JSON files. / 点击 **Generate Files**，预览并下载 JSON 文件。

## 📂 File Structure / 文件结构说明

When you download the files, place them in your resource pack as follows:
下载文件后，请按以下结构放入资源包：

- **Blockstates**: `assets/minecraft/blockstates/`
- **Models**: `assets/minecraft/models/block/wall/` or `assets/minecraft/models/block/fence/`
- **Items**: `assets/minecraft/items/`
- **Textures (Note)**: / **纹理说明**
  - **Wall**: Textures expect a subfolder: `assets/minecraft/textures/block/wall/<name>/`
  - **Fence/Gate**: Textures are flat in `assets/minecraft/textures/block/fence/` (e.g., `fence_oak_side.png`)

## 🛠️ Built With / 技术栈

- HTML5 / CSS3 / Vanilla JavaScript
- No external libraries, no backend required, runs 100% locally in your browser. / 无外部依赖，无需后端，100% 本地运行。



