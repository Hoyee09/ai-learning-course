# AI 8 周交互学习课件

这是一个可以直接发布到 GitHub Pages 的单页交互课件，面向大一学生的 AI 入门学习。

## 包里有什么

| 文件 | 用途 |
| --- | --- |
| `index.html` | 网站首页，也是完整的交互课件 |
| `README.md` | 项目说明和快速上线步骤 |
| `GitHub_Pages_部署教程.md` | 从注册 GitHub 到上线、更新和排错的详细教程 |

## 本地打开

直接双击 `index.html`，用 Edge 或 Chrome 打开即可。

课件不依赖安装包，也不依赖服务器。学习进度、复盘笔记和自测成绩保存在当前浏览器的 localStorage 中。

## 10 分钟上线

1. 注册并验证 GitHub 账号。
2. 新建一个 **Public** 仓库，例如 `ai-learning-course`。
3. 在仓库首页点击 `Add file` → `Upload files`。
4. 上传本文件夹中的 `index.html`，然后点击 `Commit changes`。
5. 打开仓库的 `Settings` → `Pages`。
6. 在 `Build and deployment` 中选择：
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
7. 点击 `Save`，等待 1–3 分钟。
8. 打开 `Actions` 标签，看到 Pages 部署成功后，再回到 `Settings` → `Pages`，点击访问网址。

项目站点的网址通常是：

```text
https://你的用户名.github.io/ai-learning-course/
```

## 上线后检查

- 页面能正常打开，标题显示“AI 起步实验室”。
- 勾选一个任务，刷新页面后进度仍然存在。
- 打开一个周任务，能看见“学什么、去哪里学、每天做什么”。
- 自测题能作答并显示结果。
- 手机浏览器也能正常操作。

## 更新网站

修改 `index.html` 后重新上传到同一个仓库，覆盖原文件，再提交一次。GitHub Pages 会自动重新发布。

更新后如果看到的还是旧页面，先等待一分钟，再用无痕窗口或强制刷新检查。

## 注意

- GitHub Pages 只能托管静态网页，不能直接运行 Python 后端。
- 免费账号建议使用 Public 仓库发布 Pages。
- 不要把 API 密钥、密码、身份证号或别人的隐私数据放进仓库。
- 课件里的外部学习资源需要联网访问。

详细步骤请看 [GitHub_Pages_部署教程.md](./GitHub_Pages_部署教程.md)。
