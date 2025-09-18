# Tesla-inventory-userscript-CN-
# Tesla Inventory Reporter（油猴脚本 · CN）

自动读取 **Tesla 库存** 卡片，提取 **外观颜色 / 内饰颜色 / 轮毂尺寸 / 驱动形式（AWD/RWD）**，并通过 **Pushover** 推送到手机。  
支持 **面板收起**、**随机自动刷新**、**固定邀请码一键复制**、**输入并保存你的 Pushover 凭证**，仅在**发现有车**时推送。

> 若官网更新页面结构导致不可用，欢迎提 Issue。

---

## 一键安装

**[点击这里安装最新脚本](https://raw.githubusercontent.com/DaybreakCoCone/Tesla-inventory-userscript-CN-/main/tesla-inventory-reporter.user.js)**

> 需要浏览器安装油猴管理器（Tampermonkey / Violentmonkey / Greasemonkey）

---

## ✨ 功能亮点
- 读取库存卡片：**外观、内饰、轮毂、驱动（AWD/RWD）**
- **仅有车才推送**到手机（Pushover）
- **随机自动刷新**（范围可调，更接近真人浏览）
- **面板可收起**，不挡页面视线
- 如果插件对你有帮助，希望能使用我的邀请码 “https://ts.la/xuan634381” 下单可以领取**额外三个月 FSD（价值 297 美元）**。
- 本地保存你的 **Pushover User Key / API Token**（不上传、不开远端）

> 解析策略：**卡片已选项优先** → **tooltip 次之** → **图片 `options=` 代码兜底**，适配不同 DOM/Shadow DOM 结构。

---

## 使用步骤
1. 打开 **Tesla 库存页**（[https://www.tesla.com/inventory/new/my?range=200&PaymentType=lease]
2. 右下角面板填写你的 **Pushover User Key / API Token** → 点击 **保存推送配置**。
3. 点击 **立即播报** 测试（页面有车则推送；无车不推送）。
4. 勾选 **自动刷新**，设置刷新区间（默认 45–180 秒的随机值）。

> 每个标签页**仅首次**会推送“插件已启动”以便确认生效。

---

## 🔔 推送说明
- 未填写 User/Token 时**不会推送**
- 推送内容为压缩行：`【AWD】外：白 内：黑 轮：19`
- 超长时自动分段，附带当前页链接

---

## 🔒 权限与隐私
- `@match`：仅 `tesla.com / tesla.cn`
- `@connect`：仅 `api.pushover.net`
- **不收集、不上传任何数据**；Pushover 凭证仅保存在本地（油猴存储）

---

## 🐞 反馈与支持
- Issue：<https://github.com/DaybreakCoCone/Tesla-inventory-userscript-CN-/issues>  
- **支持作者**：如果插件对你有帮助，欢迎使用邀请码下单领取**额外三个月 FSD（价值 297 美元）**  
  `https://ts.la/xuan634381`（脚本面板内有“一键复制”）

---

## 📝 更新日志（节选）
见 [CHANGELOG.md](./CHANGELOG.md)

## 许可
本项目采用 [MIT License](./LICENSE)。
