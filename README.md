# GPT input

**简约的 Android 中英文输入法 · A minimal Chinese & English keyboard for Android**

[下载 / Download v2.3.3](https://github.com/claudepara47-dot/gpt-input/releases/tag/v2.3.3) · Android 12+ · GPL-3.0-or-later

## 中文

GPT input 将本地中英文输入与可自行配置的大模型指令结合。默认采用黑灰与橙色界面，支持更换主题色。日常拼音、英文建议及个人词库学习在本机处理；AI 按需连接你配置的服务，不内置共享 API Key。本项目不是 OpenAI 官方应用。

### 主要功能

| 功能 | 说明 |
| --- | --- |
| 中英文输入 | 中文基于 Rime、Trime JNI 与雾凇拼音，支持全拼、简拼、整句候选；英文直接上屏，提供补全和纠错建议 |
| 候选与学习 | 停顿后刷新候选，刷新间隔可调；学习常用词和相邻组合，中英文词库独立管理、编辑 |
| 编辑与剪贴板 | 方向键、选择、复制、剪切、粘贴、清空及短暂撤销；剪贴板采用表格布局 |
| 符号与主题 | 希腊字母、数学符号等分类符号库；主题色可自定义，默认橙色 |
| AI 指令 | 支持 OpenAI 兼容的 Chat Completions 接口、模型列表、可编辑系统提示词及命名指令；安全校验通过后直接替换指令 |
| 回收站 | 手动删除的词条、AI 指令和剪贴板记录保留 15 天，可恢复或永久删除 |

### 快速使用

1. 从发布页下载 **GPT-input-2.3.3.apk** 并安装。打开 App，依次使用 **启用**、**选择输入法**，在系统列表中选择 **GPT input**。
2. 点击键盘上的 **中/英** 切换语言。中文点击候选上屏；英文点击候选替换当前词并追加空格，直接按空格保留原拼写。中文预览仍有内容时，**Enter** 会将预览原样上屏。
3. 英文 Shift 点一次为单字母大写，再点一次锁定；中文 Shift 点一次即锁定，再点解除。
4. 在 App 的 AI 设置中填写 **HTTPS Base URL**（含服务商要求的版本路径，例如 `/v1`）、**API Key** 和**模型**；可获取模型列表并测试连接。提示词与指令页面可编辑系统提示词、指令名称和内容。
5. 在输入框中完整输入以下格式，将光标留在结尾并短暂停顿后自动触发：
   - **已保存指令：** `/今天心情很好/翻译`（需存在名称为“翻译”的指令；不加 `*`）。
   - **临时提示词：** `/今天心情很好/翻译成英文*`（以半角 `*` 结束）。
   生成期间可以继续使用键盘；结果直接替换原指令。若原指令已修改或输入框切换，保护机制可能阻止替换。
6. 在 App 中分别管理中英文词库、主题、候选刷新间隔与回收站。右下角 **AI** 按钮可查看和切换模型。

**升级：** 直接覆盖安装同签名的新 APK。卸载或清除数据会丢失本地设置和个人词库。

## English

GPT input combines an offline Chinese and English keyboard with an optional, user-configured AI assistant. It uses a minimal dark interface with orange accents by default and supports custom theme colors. Everyday input, suggestions, and personal vocabulary learning run locally. AI requests go to your configured provider; no shared API key is included. This project is not an official OpenAI application.

### Features

| Feature | Description |
| --- | --- |
| Chinese & English input | Rime, Trime JNI, and Rime Ice power Chinese full pinyin, abbreviated pinyin, and sentence candidates; English text is entered directly with completion and spelling suggestions |
| Suggestions & learning | Candidates refresh after a pause, with an adjustable interval; frequent words and adjacent word combinations are learned locally, with separate Chinese and English vocabulary management |
| Editing & clipboard | Cursor controls, selection, copy, cut, paste, clear, and short-lived undo; a grid-based clipboard |
| Symbols & themes | Categorized Greek letters, mathematical symbols, and more; customizable accent color |
| AI commands | OpenAI-compatible Chat Completions, model listing, editable system prompts, and named commands; results replace the command after editor safety checks |
| Recycle bin | Manually deleted vocabulary entries, AI commands, and clipboard records can be restored for 15 days |

### Quick start

1. Download **GPT-input-2.3.3.apk** from the release page and install it. Open the app, tap **启用** (Enable), then **选择输入法** (Choose keyboard), and select **GPT input** in Android's keyboard list.
2. Tap **中/英** to switch languages. Select a Chinese candidate to commit it. In English, selecting a suggestion replaces the current word and adds a space; pressing Space keeps the original spelling. When a Chinese composition preview is present, **Enter** commits that preview as typed.
3. In English, tap Shift once for one uppercase letter and again for Caps Lock. In Chinese mode, one tap locks uppercase; tap again to unlock.
4. In AI settings, enter an **HTTPS Base URL** (including the provider's version path, such as `/v1`), **API Key**, and **model**. Fetch the model list or test the connection as needed. Edit the system prompt and named commands on the prompts and commands page.
5. Type a complete command in the text field, keep the cursor at its end, and pause briefly:
   - **Saved command:** `/Hello/translate` (first save a command named `translate`; no trailing `*`).
   - **One-off prompt:** `/Hello/Translate into Chinese*` (ends with an ASCII `*`).
   You can keep typing while generation runs. The result replaces the original command automatically. Changes to that command or switching text fields may prevent replacement.
6. Manage Chinese and English vocabulary, theme color, candidate refresh timing, and deleted items in the app. The keyboard's lower-right **AI** button opens the current model and model list.

**Upgrading:** Install the new APK over the existing app using the same release signature. Uninstalling or clearing app data removes local settings and learned vocabulary.

## 下载与源码 / Downloads & source

Use the [v2.3.3 release assets](https://github.com/claudepara47-dot/gpt-input/releases/tag/v2.3.3):

| 文件 / File | 内容 / Contents |
| --- | --- |
| `GPT-input-2.3.3.apk` | 签名安装包 / Signed Android installer |
| `GPT-input-source-2.3.3.zip` | 完整源码、词库、原生依赖源码、构建说明及现有中文手册 / Complete source, dictionaries, native dependency sources, build instructions, and the existing Chinese manual |
| `SHA256SUMS-2.3.3.txt` | 文件校验值 / File checksums |

完整可构建源码在上方命名的 ZIP 附件中；GitHub 自动生成的 “Source code” 压缩包只对应本介绍仓库。解压后阅读源码根目录的 `README.md`；构建使用 JDK 17、Gradle 8.11.1 和 Android SDK 35。现有详细手册标注为 2.3.2；2.3.3 保留其操作方式，将回车图标显示为 Enter。

The complete buildable source is the explicitly named ZIP asset above. GitHub's automatically generated “Source code” archives contain only this introduction repository. After extraction, see the source root's `README.md`. Build with JDK 17, Gradle 8.11.1, and Android SDK 35. The existing detailed manual is labeled 2.3.2; version 2.3.3 retains those operations and displays the return key as Enter.

## 许可与致谢 / License & credits

GPL-3.0-or-later. See [LICENSE](LICENSE) and [third-party notices](THIRD_PARTY_NOTICES.md). Based on [Trime](https://github.com/osfans/trime), [Rime](https://github.com/rime/librime), and [Rime Ice / 雾凇拼音](https://github.com/iDvel/rime-ice). Third-party components retain their respective licenses.

