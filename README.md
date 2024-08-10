# 小站备忘

## 使用自定义域名

### 步骤 1: 准备自定义域名
确保你拥有一个有效的自定义域名，并且DNS记录可以被修改。你可以在域名提供商的控制面板中进行这些修改。

### 步骤 2: 添加CNAME记录
1. 在你的GitHub Pages仓库的根目录下创建一个名为`CNAME`的文件。
2. 在文件中写入你的自定义域名（不带www），例如：
   ```
   example.com
   ```
3. 提交并推送这个文件到你的GitHub Pages仓库。

### 步骤 3: 修改DNS记录
登录到你的域名提供商的控制面板，找到DNS管理区域，创建一个新的CNAME记录：
- 记录类型：CNAME
- 主机记录（Host）：@ 或 www （取决于你希望访问的域名）
- 目标地址（Target）：`<username>.github.io`（用你的GitHub用户名替换`<username>`）

### 特殊情况：使用www域名
如果你的自定义域名为`www.example.com`，你需要创建两条CNAME记录：
- 第一条记录的主机为`@`，目标地址为`ghs.googleusercontent.com`。
- 第二条记录的主机为`www`，目标地址为你的GitHub Pages URL，即`<username>.github.io`。

### 步骤 4: 等待DNS记录生效
DNS更改可能需要一段时间才能在全球范围内生效，通常这个过程需要几分钟到几小时。

### 步骤 5: 验证自定义域名
一旦DNS记录生效，你可以通过访问你的自定义域名来验证是否成功指向GitHub Pages站点。

### 步骤 6: 配置SSL
GitHub Pages自动为所有自定义域名提供免费的SSL证书。一旦你的自定义域名开始解析到GitHub Pages，SSL证书会自动激活，确保你的网站使用HTTPS协议。

### 注意事项
- 如果你的GitHub Pages站点是用户页面，仓库名称应该是`<username>.github.io`。
- 如果你的GitHub Pages站点是项目页面，仓库名称应该是`<username>/<projectname>.github.io`。

--- 
