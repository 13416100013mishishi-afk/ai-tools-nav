# AI 工具导航站

> 收录 20 款当前最热门的 AI 工具，一键跳转官网，支持分类筛选。

**在线访问：** https://13416100013mishishi-afk.github.io/ai-tools-nav

---

## 如何添加新工具

本页面所有工具数据都在 `index.html` 文件里，找到大约第 180 行的 `tools` 数组，按以下格式添加即可：

```javascript
{
  name: "工具名称",
  url: "官网链接（带 https://）",
  desc: "一句话介绍",
  category: "分类",
  emoji: "图标表情"
},
```

### 分类说明

| category 值 | 显示标签 | 颜色 |
|-------------|---------|------|
| `写作` | 🏷️ 写作 | 粉红色 |
| `图像` | 🏷️ 图像 | 紫色 |
| `编程` | 🏷️ 编程 | 绿色 |
| `效率` | 🏷️ 效率 | 橙色 |
| `其他` | 🏷️ 其他 | 蓝色 |

### 添加步骤（图文版）

1. 打开 `index.html` 文件
2. 找到 `const tools = [` 开头的区域
3. 找到最后一个 `},` 后面、`]};` 前面的位置
4. 复制下面的模板，粘贴进去（注意最后一行也要加逗号）

```javascript
  {
    name: "新工具名称",
    url: "https://工具官网.com",
    desc: "一句话介绍这个工具是做什么的",
    category: "写作",   // ← 改成对应分类
    emoji: "🤖"        // ← 可以换其他表情
  },
```

5. 保存文件
6. 把更新后的 `index.html` 推送到 GitHub，页面会自动更新

---

## 如何更新页面上的工具数量

分类按钮旁边的数字（如"写作 5"）是手动标的，添加新工具后记得同步修改。

在 `index.html` 找到这段代码：

```html
<button class="filter-btn active" data-cat="all">全部 <span class="count">20</span></button>
<button class="filter-btn" data-cat="写作">写作 <span class="count">5</span></button>
<button class="filter-btn" data-cat="图像">图像 <span class="count">5</span></button>
<button class="filter-btn" data-cat="编程">编程 <span class="count">5</span></button>
<button class="filter-btn" data-cat="效率">效率 <span class="count">3</span></button>
<button class="filter-btn" data-cat="其他">其他 <span class="count">2</span></button>
```

把对应分类的数字改对就行。

---

## 常用表情符号参考

| 用途 | 推荐 emoji |
|------|-----------|
| 对话 / 聊天 AI | 🤖 |
| 写作助手 | 📝 |
| 图像生成 | 🎨 🖼️ |
| 编程工具 | 💻 🖥️ |
| 效率工具 | ✅ 📋 |
| 视频工具 | 🎥 🎬 |
| 音频 / 语音 | 🎙️ 🔊 |
| 搜索 | 🔍 |
| 通用 | ✨ ⚡ 🌟 |

---

## 技术说明

- 纯前端实现：HTML + CSS + JS，无需后端服务器
- 响应式设计：电脑和手机都能用
- 部署在 GitHub Pages：免费、快速、永久有效
- 无需安装任何依赖，直接用浏览器打开即可

---

## 本地预览

如果想在本地查看效果：

1. 双击 `index.html` 用浏览器打开
2. 或在终端运行：`open /path/to/index.html`（macOS）或 `xdg-open index.html`（Linux）

---

## 部署说明（自己部署到 GitHub Pages）

1. 创建新仓库，名字例如 `ai-tools-nav`
2. 把 `index.html` 和 `README.md` 推送到仓库的 `main` 分支
3. 依次点击：**Settings → Pages → Source → 选择 `main` 分支 → Save**
4. 等待 1~2 分钟，访问 `https://你的用户名.github.io/ai-tools-nav`
