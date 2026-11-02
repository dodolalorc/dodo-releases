# Dodo

Dodo 的公开安装包与轻量静态官网。App 源码不在此仓库。

- [Dodo 官网](https://dodolalorc.cn/dodo-releases/)
- [下载最新 Android 体验版](https://github.com/dodolalorc/dodo-releases/releases/latest/download/dodo.apk)
- [版本记录](https://github.com/dodolalorc/dodo-releases/releases)
- iOS 暂未开放下载。

## 本地预览

无需依赖安装或构建，在仓库根目录运行：

```sh
python3 -m http.server 8080 --directory docs
```

打开 http://localhost:8080 。所有网页资源使用相对路径，可部署到 GitHub Pages 项目子目录；网页不依赖 JavaScript、外部字体或运行时 API。

## GitHub Pages

网页内容在 `docs/`。GitHub Pages 已配置为 Deploy from a branch，分支 `main`、目录 `/docs`，并开启 HTTPS。网站继承账号的自定义域名，访问地址为 https://dodolalorc.cn/dodo-releases/ 。推送到 `main` 后由 GitHub 自动部署。

APK 与 `update.json` 继续存放在 Releases，不要提交到网页目录。官网使用 latest 下载链接，应用内更新清单仍应指向固定版本 APK，不能修改为 latest。网页未硬编码最新版本号，无需每次发版修改下载按钮。

## 内容维护

- `docs/index.html`：产品介绍、下载、常见问题与数据说明。
- `docs/style.css`：响应式样式，中文系统字体、键盘焦点与减少动态效果支持。
- `docs/assets/`：Dodo 图标与压缩后的 WebP 界面预览。
- 界面来源：Dodo 项目的真实组件浏览器预览，采用示例数据，并非原生设备截图。today / finance 来自 2026-10-30 截图，plan / calendar 来自此前组件预览；应用更新后需核对并替换。
- 图标来自 Dodo 的 `assets/icon.svg`。没有引入第三方网页模板、字体或图片。
- 发布前核实实际功能、Android 测试签名状态和 iOS 渠道。不要将日记、备忘、云同步、备份宣传为已实现能力。

此网站未添加统计、Cookie、表单或第三方脚本。托管与下载请求仍由 GitHub 基础设施处理。网页文件和应用安装包采用各自适用的授权，不因公开托管而改变原有授权。
