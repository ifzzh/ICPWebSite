# ICP备案页面

> 本项目基于 [Steve5wutongyu6/ICPWebSite](https://github.com/Steve5wutongyu6/ICPWebSite) 修改，并适配了 EdgeOne 一键部署，致谢原作者大佬的开源贡献。

> 本项目为ICP备案/公安备案展示页，支持自定义主标题、副标题和备案信息，适用于合规要求。

## 功能简介
- 支持通过环境变量自定义页面主标题、副标题、ICP备案号、公安备案号等内容
- 页面样式美观，适合直接部署上线

## 环境变量说明
在项目根目录下的 `.env` 文件中配置以下变量：

| 变量名                        | 说明                   | 示例值                  |
|------------------------------|------------------------|------------------------|
| VITE_TEXT_TITLE              | 展示文字的主标题（自动大写）             | a.com              |
| VITE_TEXT                    | 展示的文字内容             | is coming soon.        |
| VITE_ICP_CODE                | ICP备案号              | 浙B2-20080101          |
| VITE_PUBLIC_SECURITY_FULLCODE| 公安备案号             | 京公网安备xxxxx号       |
| VITE_TITLE                   | 页面标题（浏览器tab）  | a.com              |

## 使用方法
1. 克隆本项目并安装依赖：
   ```bash
   npm install
   # 或 yarn install / pnpm install
   ```
2. 编辑 `.env` 文件，按上方说明填写各项内容。
3. 启动本地开发预览：
   ```bash
   npm run dev
   ```
   浏览器访问命令行输出的本地地址（如 http://localhost:5173/）。
4. 构建生产环境静态文件：
   ```bash
   npm run build
   ```
   构建结果在 `dist/` 目录，可直接部署到静态服务器。

## 部署到 Vercel
1. 访问 [Vercel 官网](https://vercel.com/) 并注册账号。
2. 新建项目，选择本仓库（或上传代码）。
3. 在 Vercel 项目设置的 **Environment Variables** 中添加上述所有环境变量（如 `VITE_TEXT_TITLE` 等），与 `.env` 文件内容一致。
4. 构建命令和预设框架默认即可
5. 部署完成后即可访问分配的域名。

## 部署到 EdgeOne
1. 同Vercel，采用EO默认分配的即可

---
