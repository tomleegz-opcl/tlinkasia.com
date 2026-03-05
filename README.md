# T-Link Asia Website - GitHub Pages 部署指南

## 📁 文件结构

```
tlinkasia-website/
├── index.html          # 英文版首页（默认）
├── zh.html            # 中文版
└── README.md          # 项目说明
```

## 🚀 部署步骤

### 1. 创建 GitHub 仓库

1. 访问 https://github.com/new
2. 填写信息：
   - **Repository name**: `tlinkasia-website`
   - **Description**: T-Link Asia corporate website
   - **Public**: ✓ 选中
   - **Add a README file**: 不选
3. 点击 **Create repository**

### 2. 上传网站文件

#### 方式 A：网页上传（最简单）
1. 在新仓库页面点击 **"uploading an existing file"**
2. 拖拽上传 `index.html` 和 `zh.html`
3. 点击 **Commit changes**

#### 方式 B：命令行上传
```bash
# 克隆仓库
git clone https://github.com/你的用户名/tlinkasia-website.git
cd tlinkasia-website

# 复制网站文件
cp /Users/tomleeicloud/.openclaw/workspace/tlink-website/*.html .

# 提交并推送
git add .
git commit -m "Initial website upload"
git push origin main
```

### 3. 启用 GitHub Pages

1. 进入仓库的 **Settings** 标签
2. 左侧菜单点击 **Pages**
3. **Source** 选择：
   - Deploy from a branch
   - Branch: **main** / **(root)**
4. 点击 **Save**
5. 等待 1-2 分钟
6. 会显示网址：`https://你的用户名.github.io/tlinkasia-website/`

### 4. 配置自定义域名

#### 在 GitHub 上：
1. Settings → Pages
2. **Custom domain** 填入：`www.tlink-asia.com`
3. 勾选 **Enforce HTTPS** ✓
4. 点击 **Save**
5. 等待 DNS 检查通过（显示 ✅）

#### 在你的域名管理后台：
添加 CNAME 记录：

| 记录类型 | 主机记录 | 记录值 | TTL |
|---------|---------|--------|-----|
| CNAME | www | 你的用户名.github.io | 默认 |

**注意**：将 `你的用户名` 替换为你的 GitHub 用户名

### 5. 验证部署

等待 5-30 分钟后，访问：
- `https://www.tlink-asia.com` ✅

---

## 🔧 常见问题

### Q: 网站显示 404？
A: 检查文件是否上传到 main 分支的根目录

### Q: 自定义域名不生效？
A: 
1. 检查 CNAME 记录是否正确
2. 等待 DNS 传播（最长 24 小时）
3. 在 GitHub Pages 设置中查看是否有 DNS 检查错误

### Q: HTTPS 证书错误？
A: 等待 GitHub 自动签发 SSL 证书（通常几分钟到几小时）

### Q: 如何更新网站？
A: 重新上传修改后的 HTML 文件到 GitHub 仓库

---

## 📞 网站信息

- **公司**: T-Link Asia Limited
- **域名**: www.tlink-asia.com
- **语言**: 英文（默认）、中文
- **联系邮箱**: info@tlinkasia.com
- **地址**: 香港中环史丹利街50号信成广场6楼C座

---

## 📝 技术说明

- **托管**: GitHub Pages
- **类型**: 静态 HTML 网站
- **响应式**: 支持桌面、平板、手机
- **SSL**: 自动 HTTPS
- **流量**: 每月 100GB 免费额度

---

部署日期: 2026-03-05