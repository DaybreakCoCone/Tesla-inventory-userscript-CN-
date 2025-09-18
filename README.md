# Tesla-inventory-userscript-CN
# Tesla Inventory Reporter（油猴脚本 · CN）
本脚本自动读取 Tesla 库存卡片，提取外观颜色、内饰颜色、轮毂尺寸和驱动形式（AWD/RWD），并通过 Pushover 推送到手机。  
支持面板收起、随机自动刷新、固定邀请码一键复制，以及输入和保存你的 Pushover 凭证。仅在发现有车时推送。

---

## 1. 安装插件

1. 在浏览器中安装一个油猴管理器，例如：
   - [Tampermonkey](https://www.tampermonkey.net/)（Chrome、Edge、Safari）（推荐）
   - [Violentmonkey](https://violentmonkey.github.io/)（Chrome、Firefox）
2. 安装油猴管理器后，点击下方链接安装脚本：

[点击这里安装最新脚本](https://raw.githubusercontent.com/DaybreakCoCone/Tesla-inventory-userscript-CN-/main/tesla-inventory-reporter.user.js)

3. 安装完成后，浏览器右上角油猴扩展图标中应显示“Tesla Inventory Reporter”脚本已启用。

---

## 2. 配置 Pushover（获取 User Key 与 API Token/Key）

Pushover 是一个把消息推送到你手机、平板或桌面的服务。  
要让脚本向你推送库存信息，请先完成以下步骤。

### 2.1 注册并登录  
- 打开官网：https://pushover.net/ → Sign Up 注册并登录  
- 登录后在 Dashboard 页上方可以看到 **User Key**，复制保存备用

### 2.2 安装客户端并登记设备  
- 在你的手机安装 Pushover：  
  iOS：App Store 搜索 Pushover  
  Android：Google Play 搜索 Pushover  
- 打开 App，用刚才的账号登录，允许通知权限  
- 确认设备在 Dashboard 的 “Your Devices” 列表里显示为 Registered

### 2.3 创建应用（获取 API Token/Key）  
- 回到官网 Dashboard，进入 “Your Applications” → “Create an Application/API Token”  
- 取一个名字（例如：Tesla Inventory Reporter），创建后即可获得 **API Token/Key**  
- 复制保存备用

### 2.4 在脚本面板中填写  
- 打开 Tesla 库存页  **（https://www.tesla.com/inventory/new/my?referral=xuan634381&redirect=no&range=200&PaymentType=lease）**
- 在右下角面板中填入：  
  - Pushover User：你的 **User Key**  
  - Pushover Token：你的 **API Token/Key**  
- 点击“保存推送配置”
- 选个有货的车型然后点“立刻播报”按钮看看手机是否能收到推送

### 3. 使用插件

打开 Tesla 库存页 (https://www.tesla.com/inventory/new/my?referral=xuan634381&redirect=no&range=200&PaymentType=lease)）。

在右下角面板可进行以下操作：

播报间隔：设置每隔多少秒解析页面。

自动刷新：勾选后脚本会按随机区间自动刷新页面。

刷新范围（秒）：可设置最小/最大随机刷新秒数。

立即播报：手动立即解析页面并推送。

暂停/运行：可随时暂停脚本。

固定邀请码一键复制：点击“复制邀请码”即可复制 (https://www.tesla.com/inventory/new/my?referral=xuan634381&redirect=no&range=200&PaymentType=lease)。
说明：如果插件对你有帮助，希望能使用我的邀请码下单可以领取额外三个月FSD（价值297美元）。

推送内容示例：

1. 【AWD】外：白 内：黑 轮：19
2. 【RWD】外：红 内：白 轮：20
## 📝 更新日志（节选）
见 [CHANGELOG.md](./CHANGELOG.md)

## 许可
本项目采用 [MIT License](./LICENSE)。
