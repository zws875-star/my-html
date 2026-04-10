# 天气穿衣建议工具 · GitHub Pages 版

这是一个可直接部署到 GitHub Pages 的前端网页项目。

## 文件说明

- `index.html`：网页主文件
- 本项目是纯前端单页，不需要后端

## 部署步骤

### 方法一：网页操作

1. 在 GitHub 新建一个仓库  
   例如仓库名：`weather-style-tool`

2. 把 `index.html` 上传到仓库根目录

3. 进入仓库的 **Settings**

4. 找到 **Pages**

5. 在 **Build and deployment** 里设置：
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`

6. 保存后，等几十秒到几分钟，GitHub 会生成网址  
   网址通常是：

   `https://你的用户名.github.io/仓库名/`

### 方法二：Git 命令行

```bash
git init
git add .
git commit -m "init weather tool"
git branch -M main
git remote add origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main
```

然后去 GitHub 仓库设置里开启 Pages。

## 使用说明

- 打开网站
- 输入城市
- 选择日期
- 点击“查询”
- 页面会自动生成天气摘要、穿衣建议、出行提醒

## 技术说明

- 使用公开天气接口：Open-Meteo
- 使用公开地理编码接口：Open-Meteo Geocoding
- 无需 API Key
- 查询失败时，自动回退到安阳示例数据，避免空白

## 后续可升级方向

1. 加空气质量和紫外线
2. 加收藏城市
3. 改成 PWA，可添加到手机桌面
4. 接入你自己的品牌名称和页脚
