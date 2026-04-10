# AI工具导航站 📚

一个简洁美观的AI工具导航页面，部署在GitHub Pages上。

---

## 🌐 访问页面

> **https://13416100013mishishi-afk.github.io/ai-tools-nav/**

---

## ➕ 如何添加新工具

### 第一步：找到数据文件

在仓库里找到文件 `ai-tools-data.json`（如果没有就用 `index.html` 里内置的数据），用**记事本**或**VS Code**打开它。

### 第二步：看懂数据格式

每条工具长这样：

```json
{
  "name": "工具名称",
  "url": "工具官网链接",
  "description": "一句话介绍",
  "category": "分类"
}
```

**分类**只能填这4种之一：
- `写作` — AI写文章、写文案
- `图像` — AI生成图片、视频
- `编程` — AI写代码、补全代码
- `效率` — AI提升工作效率（会议、笔记等）

### 第三步：添加新工具

在文件里找到最后一条工具（注意：最后一条后面**没有逗号**），在它的 `}` 后面加上逗号，然后粘贴新工具的模板：

```json
  {
    "name": "新工具名称",
    "url": "https://工具官网.com",
    "description": "一句话介绍",
    "category": "写作"
  }
```

**注意**：
- 每条之间用英文逗号 `,` 分隔
- 最后一条**不要**逗号
- 英文引号是 `"` 不是 `''`
- JSON格式错误会导致页面打不开

### 第四步：提交修改

1. 打开 [https://github.com/13416100013mishishi-afk/ai-tools-nav](https://github.com/13416100013mishishi-afk/ai-tools-nav)
2. 点右上角 **Edit（编辑）** 图标
3. 修改内容
4. 点 **Commit changes**（绿色按钮）
5. 等1-2分钟，页面自动更新

---

## 📁 文件说明

| 文件 | 作用 |
|------|------|
| `index.html` | 主页面（包含网页代码+数据） |
| `README.md` | 说明文档（你正在看的这个） |

> **注意**：如果 `ai-tools-data.json` 不存在，数据直接写在 `index.html` 的 `tools` 数组里，修改方法相同。

---

## ❓ 常见问题

**Q: 分类填错了会怎样？**
页面能正常显示，但分类标签颜色会不对。应改为：写作(蓝色)、图像(粉色)、编程(绿色)、效率(橙色)。

**Q: 能加"其他"分类吗？**
可以，但不推荐。如果确实需要，把 `category` 改成 `其他`，页面会自动显示灰色标签。

**Q: 页面没更新怎么办？**
等2分钟后刷新浏览器。Chrome按 `Ctrl + Shift + R`（强制刷新）。

**Q: JSON格式怎么检查？**
打开 [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com)，把内容粘贴进去，如果显示 `Valid JSON` 就是对的。

---

## 🔧 部署说明（供维护者参考）

- 仓库：`13416100013mishishi-afk/ai-tools-nav`
- 部署方式：GitHub Pages（Settings → Pages → Source: main branch）
- 访问域名：`https://13416100013mishishi-afk.github.io/ai-tools-nav/`
