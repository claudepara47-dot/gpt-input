# GPT input 2.3.4

Android 12+ · versionCode 15 · 可覆盖安装 / In-place upgrade supported

## 中文更新说明

本次更新重点改进输入纠错、本地学习和键盘底部布局。

| 项目 | 改进 |
| --- | --- |
| 底部布局 | 键盘背景延伸至系统底部区域，按稳定导航尺寸布局，减少底部导航条显隐导致的跳动；保留三键导航下按钮的可点击区域 |
| 按键文字 | 空格键显示 **Space**，与 **Enter** 保持一致 |
| 拼音纠错 | 新增 **超强** 档，提供关闭、轻度、标准、增强、超强五档；扩大受限搜索范围，最多处理三处错拼，候选仍在停顿后计算 |
| 更多候选 | 即使首选置信度较高，也保留其他选项；中文补充同音或近似拼音词，英文完整词也提供邻近拼写建议，首选仍排在前面 |
| 删除后纠错 | 删除刚输入的整词后，停顿时提供其他候选；英文未加空格的单词也支持，点击候选后补空格 |
| 学习确认 | 字词提交后保留 3 秒，并确认正文未被改动，才增加权重；快速删除、修改、切换输入框或无法核对文本时，取消待确认学习 |
| 词库与权重 | 个人词库只保存基础词库中没有的词汇；基础词的使用权重独立更新，升级时迁移已有记录，中英文继续分开管理 |
| 权重衰减 | 个人词、基础词使用权重和相邻词组合支持时间衰减；可设置半衰期、选择函数或填写自定义公式，默认指数衰减、30 天半衰期 |
| 括号配对 | 常用中英文括号支持长按成对输入、空对成对删除；光标后有文字或前方存在未闭合的同类括号时，只输入一个 |

### 新功能使用

- **纠错强度：** App → 键盘 → 拼音纠错。默认“标准”；纠错只给出候选，点击后才采纳。
- **衰减设置：** App → 本地词库 → 权重衰减。时间参数范围为 **0.1–3650 天**，可选指数、线性、反比例、关闭衰减、自定义公式，并查看剩余权重预览表。
- **自定义公式：** `t` 为距上次使用的天数，`h` 为设置的时间参数；例如 `pow(0.5, t / h)`。支持 `+ - * / ^`、`pow`、`exp`、`ln/log`、`sqrt`、`abs`、`min`、`max`。公式在本地受限计算并检查范围与衰减趋势；实际半衰期取决于表达式。修改设置不清空词条与统计。
- **括号：** 长按左括号输入一对，光标停在中间。空括号中间或紧跟空括号按退格可整对删除；非空或不匹配的括号不会整对删除。

### 安装与验证

下载 **GPT-input-2.3.4.apk** 直接覆盖安装，无需卸载。沿用原发布签名，可保留已有设置和词库。首次使用在 App 中依次点击“启用”“选择输入法”，选择 **GPT input**。

- 122 项 JVM 单元测试通过；Android 12 和 Android 15 模拟器各通过 78 项设备测试。
- 已验证 2.3.3 → 2.3.4 覆盖安装、签名、词库迁移和导航布局；Lint 为 0 错误、27 警告。
- 目标手机上的微信与厂商导航栏仍需实测；模拟器结果不代表所有设备的实际输入延迟。真实 AI 服务需自行配置后验证。

## English release notes

This update improves spelling suggestions, local learning, and keyboard layout near the system navigation area.

| Area | Changes |
| --- | --- |
| Bottom layout | The keyboard background extends into the system navigation area. Stable navigation dimensions reduce layout jumps while keeping controls accessible with three-button navigation |
| Key labels | The spacebar now reads **Space**, matching **Enter** |
| Pinyin correction | Adds **Ultra** to Off, Light, Standard, and Strong. A bounded wider search can handle up to three spelling edits; suggestions are still calculated after a typing pause |
| Candidate variety | Alternative candidates remain available even when the first choice has high confidence. Chinese adds homophones or nearby pinyin matches; complete English words can also show nearby spelling suggestions |
| Correction after deletion | Deleting a recently entered word offers alternatives after a pause, including unfinished English words. Choosing an English suggestion adds a space |
| Confirmed learning | A word gains usage weight only after remaining unchanged for three seconds and passing text verification. Quick deletion, editing, switching fields, or unverifiable text cancels pending learning |
| Vocabulary & weights | Personal vocabulary stores words absent from the base dictionary. Base-word usage weights are updated separately; existing records migrate on upgrade, with Chinese and English managed separately |
| Weight decay | Personal words, base-word usage weights, and adjacent-word combinations support configurable decay. Choose a half-life, preset function, or custom formula; the default is exponential decay with a 30-day half-life |
| Paired brackets | Common Chinese and English brackets support long-press pair insertion and empty-pair deletion. Only one opener is inserted when text follows the cursor or a matching opener is already unmatched before it |

### Using the new settings

- **Correction strength:** App → 键盘 (Keyboard) → 拼音纠错 (Pinyin correction). Standard is the default; suggestions never automatically replace your text.
- **Decay:** App → 本地词库 (Local vocabulary) → 权重衰减 (Weight decay). Set a time parameter from **0.1 to 3650 days** and choose exponential, linear, inverse, no decay, or a custom formula. A table previews the remaining weight.
- **Formula:** `t` is days since last use; `h` is the configured time parameter. Example: `pow(0.5, t / h)`. Supported operators/functions: `+ - * / ^`, `pow`, `exp`, `ln/log`, `sqrt`, `abs`, `min`, `max`. Evaluation is local and bounded, with range and decay-trend validation. The actual half-life depends on the formula. Changing these settings does not clear vocabulary or statistics.
- **Brackets:** Long-press an opening bracket to insert a pair with the cursor between them. Backspace inside or immediately after an empty pair deletes both symbols; nonempty or mismatched pairs are protected.

### Installation and validation

Install **GPT-input-2.3.4.apk** over the existing app; do not uninstall first. The original release signature is retained so settings and learned data can be preserved. For a first installation, open the app, tap **启用** (Enable), then **选择输入法** (Choose keyboard), and select **GPT input**.

- 122 JVM tests passed; 78 device tests passed on each of the Android 12 and Android 15 emulators.
- Upgrade from 2.3.3, signing, vocabulary migration, and navigation layout were checked. Lint: 0 errors and 27 warnings.
- WeChat and vendor-specific navigation behavior still require testing on the target phone. Emulator results are not a guarantee of real-device typing latency. A real AI provider must be configured and tested by the user.

## 下载文件 / Downloads

| Asset | 内容 / Contents |
| --- | --- |
| `GPT-input-2.3.4.apk` | 签名安装包 / Signed APK |
| `GPT-input-source-2.3.4.zip` | 完整可构建源码、词库、原生依赖源码和构建说明 / Complete buildable source, dictionaries, native dependency sources, and build instructions |
| `更新说明-2.3.4.md` | 中文详细更新说明 / Detailed Chinese changelog |
| `测试报告-2.3.4.md` | 测试结果与性能评测范围 / Test results and performance measurement scope |
| `SHA256SUMS-2.3.4.txt` | 上述四个文件的 SHA-256 / SHA-256 checksums for the four files above |

请下载命名的 **GPT-input-source-2.3.4.zip** 获取完整源码；GitHub 自动生成的 “Source code” 包只包含介绍仓库。源码包不包含发布私钥或 API Key。现有详细手册标注为 2.3.2，新功能请参考本页与源码内 `CHANGES-2.3.4.md`。

For complete source, download the explicitly named **GPT-input-source-2.3.4.zip**. GitHub's automatic “Source code” archives contain only the introduction repository. No release private key or API key is included. The existing detailed manual is labeled 2.3.2; refer to this page and `CHANGES-2.3.4.md` in the source package for new behavior.
