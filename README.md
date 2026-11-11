

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
# ⛏️ MC Font Forge

[English](#english) | [简体中文](#简体中文)

---

## English

A lightweight, pure front-end font conversion tool tailored for Minecraft resource pack creators. No installation required—just open it in your browser and use it immediately.

If you have ever tried to create a Minecraft font pack using bitmap font generators like **SnowB**, you know the pain. You often encounter frustrating errors (e.g., the game fails to load the font, characters are misaligned, or the game crashes). This tool is built to solve these exact problems.

### ✨ Features

*   **🚀 Pure Frontend**: A single HTML file. No server required, no data collection. 100% safe and offline-ready.
*   **🔄 FNT to JSON**: Instantly parses `.fnt` files exported from SnowB, extracts coordinates, and generates the MC-compatible `default.json`.
*   **🛡️ Full Unicode Escaping**: Fixes garbled text by forcing all characters into the standard `\uXXXX` format. It also corrects the "double backslash (`\\u`)" bug caused by JSON serialization.
*   **🧩 Auto-padding `\u0000`**: Minecraft requires the `chars` array to have perfectly equal line lengths. This tool automatically finds the longest line and pads the rest with `\u0000` placeholders to prevent errors and misalignments.
*   **📏 Customizable `height` & `ascent`**: Built-in input fields to freely adjust `height` (font size) and `ascent` (vertical position), supporting decimal values for fine-tuning.
*   **⚠️ Anti-crash Protection**: Automatically detects if `ascent` is greater than `height` (the most common cause of MC font crashes). If it exceeds the limit, it safely caps it at 80% of the height.

### 🛠️ Usage

1.  **Prepare Files**: Use [SnowB](https://snowb.org/) to generate your font atlas (Grid Packing is highly recommended) and export the `.fnt` and `.png` files.
2.  **Open Tool**: Download `index.html` from this repo and double-click to open it in your browser.
3.  **Upload**: Upload your `.fnt` file.
4.  **Set Path**: Enter the relative path of your `.png` file within the resource pack (e.g., `minecraft:font/my_font.png`).
5.  **Adjust Parameters**:
    *   **Height** (default: 11): Controls font size. Increase if it looks too small.
    *   **Ascent** (default: 10): Controls vertical positioning. Increase if it sits too low.
6.  **Generate & Download**: Click generate, verify the output, and download `default.json`.
7.  **Test in Game**: Place the generated `default.json` and your `.png` into the correct resource pack directories, then press `F3 + T` in-game to reload.

### 📂 Resource Pack Structure

```text
Your_Pack_Name/
└── assets/
    └── minecraft/
        ├── font/
        │   ├── default.json       <-- Generated by this tool
        │   └── my_custom_font.png <-- Your font atlas
        └── textures/
            └── font/
                └── my_custom_font.png <-- Physical image file (must match the JSON path)

        ├── font/
        │   ├── default.json       <-- 本工具生成的
        │   └── my_custom_font.png <-- 你的字体图集
        └── textures/
            └── font/
                └── my_custom_font.png <-- 图片实际存放位置(与json中的file路径对应)
🐛 常见问题排查
游戏内提示 Lines in codepoint grid have to be the same length：说明你的 JSON 某行长度不一致。请务必使用本工具生成，不要手动修改 chars 数组。

游戏内提示 Ascent higher than height：ascent 的值超出了 height 的限制，请调低 ascent。

游戏提示 FileNotFoundException：default.json 里面填写的图片路径，与你资源包里的图片实际路径不匹配（注意大小写和文件夹层级）。

🤝 贡献与反馈
如果你在使用中遇到任何 BUG，或者有更好的改进建议，欢迎提交 Issue 或 Pull Request！


