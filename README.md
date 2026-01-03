# 🔍 搜索引擎切换器 / Search Engine Switcher

[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)
[![Greasy Fork](https://img.shields.io/badge/Greasy%20Fork-Install-red)](https://greasyfork.org/zh-CN/scripts/561263)
![Version](https://img.shields.io/badge/version-1.0-blue)

> **让搜索更高效！**
> 在 Google、Bing 等搜索结果页的左侧显示一个美观的侧边栏，支持一键切换到其他搜索引擎。
> 
> 此脚本的各项功能由Gemini3.0 Pro生成，本作者是编程小白，仅负责功能构思，也欢迎各位反馈与建议。

[👉 点击这里立即安装脚本](https://greasyfork.org/zh-CN/scripts/561263/code/script.user.js)

## ✨ 核心功能 (Features)

* **⚡️ 高效切换**：无需手动打开新标签页，直接在当前页面切换搜索源。
* **🎨 VS Code 风格**：现代化的 UI 设计，支持 **自动深色模式 (Dark Mode)**，完美适配系统主题。
* **🛠 高度自定义**：
    * **添加任意引擎**：支持添加任何你喜欢的网站（如 GitHub, StackOverflow, 知乎, 百度等）。
    * **自由排序**：通过上下箭头轻松调整引擎顺序。
    * **参数可调**：支持各类搜索引擎以及站内搜索。
* **🙈 自定义防遮挡**：在 Bilibili、YouTube 等左侧有导航栏的网站，侧边栏会**自动收起**，鼠标靠近时才显示，可自定义生效网站。
* **🚀 极速加载**：
    * **Favicon 缓存**：首次加载后将图标缓存在本地，第二次打开秒开，无需网络请求。
    * **按需加载**：默认仅在主流搜索引擎生效，不影响普通网页性能。

## 📥 安装 (Installation)

1.  安装浏览器扩展 [Tampermonkey](https://www.tampermonkey.net/) (油猴)。
2.  点击下方链接安装脚本：
    * [**👉 前往 Greasy Fork 安装**](https://greasyfork.org/zh-CN/scripts/561263) (推荐)
    * 或者直接安装本仓库的 `main.user.js`。

## 📖 使用教程 (How to Use)

1.  **安装脚本**后，在 Google 或 Bing 搜索任意内容。
2.  **左侧悬浮窗**：你会看到左侧出现一个半透明的侧边栏。
3.  **点击切换**：点击图标即可跳转。
4.  **打开设置**：点击侧边栏标题栏右侧的 **⚙️ (齿轮图标)**，或在油猴插件菜单中点击 **"⚙️ 搜索引擎设置"**。

### ⚙️ 设置面板说明

* **搜索引擎列表**：
    * **名称**：显示在按钮上的文字。
    * **图标域名**：输入主域名（如 `github.com`），脚本会自动抓取图标。
    * **URL 前缀**：搜索结果页的链接前半部分。
    * **关键词参数**：URL 中代表搜索词的参数名（如 `q` 或 `wd`）。
* **自动收起规则**：输入域名（如 `bilibili.com`），在这些网站上侧边栏会自动隐藏。
* **清空缓存**：如果图标显示异常，可点击底部的垃圾桶按钮重置。

## ⚠️ 关于自定义搜索引擎 (Important)

**出于安全和性能考虑，本脚本默认仅在以下主流网站生效：**
`Google`, `Bing`, `YouTube`, `Bilibili`, `V2EX` 等。

**如果你添加了其他的搜索引擎或站内搜索（例如 百度、知乎），需要更改脚本的Match匹配域名列表，请按以下步骤操作使其生效：**

1.  打开浏览器扩展栏的 **Tampermonkey (油猴)** 图标。
2.  点击 **管理面板 (Dashboard)**。
3.  点击本脚本 **Search Engine Switcher**。
4.  切换到 **设置 (Settings)** 选项卡。
5.  在 **用户包括 (User Includes)** 区域，点击 `Add...`。
6.  输入该网站的域名规则，例如：`*://www.baidu.com/*`。
7.  保存即可。

> *(或者，您可以编辑脚本代码，在match类添加以下代码来开启全网匹配模式，但不推荐)*

```// @match        *://*/*```

## 🛡️ 权限说明 (Permissions)

为了实现高级功能，本脚本申请了以下权限，**绝不收集任何用户隐私**：

* `connect www.google.com`: 仅用于从 Google 服务器下载网站图标 (Favicon)。
* `GM_xmlhttpRequest`: 用于将下载的图标转换为本地数据，实现本地缓存。
* `GM_setValue/getValue`: 用于保存您的自定义设置（引擎列表、排序等）。

## 👏 致敬与参考 (Credits)

本脚本基于开源社区的灵感进行现代化改造与功能增强。

**PS: 此脚本参考并致敬了 Corlius 的原创作品：**
[Original Script on GreasyFork](https://greasyfork.org/zh-CN/scripts/490643)

## 📄 License

MIT License.

---

### 💬 反馈与建议
如果您觉得这个脚本好用，请给个好评！如果有任何 bug 或建议，欢迎在 Issues 区留言。
