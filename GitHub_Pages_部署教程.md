# 用 GitHub 搭建你的第一个网站

这份教程只做一件事：把你手里的交互课件发布成一个真正的网址。

你不需要买服务器，也不需要会后端。只要会拖拽文件、点几次按钮，就可以完成。

## 0. 先认识 6 个词

| 词 | 你可以这样理解 |
| --- | --- |
| GitHub | 存放代码和项目文件的地方 |
| 仓库 Repository | 一个项目文件夹，里面有代码、说明和历史版本 |
| 提交 Commit | 给当前版本拍一张快照，并写一句说明 |
| 分支 Branch | 一条版本线；新手先使用默认的 `main` |
| GitHub Pages | GitHub 提供的静态网站托管服务 |
| `index.html` | 网站首页；访问网站根地址时，浏览器默认打开它 |

这次发布的是“静态网站”：HTML、CSS、JavaScript 在浏览器里运行。课件可以正常保存学习进度，但不会运行 Python 后端。

## 1. 准备工作

你需要：

- 一个 GitHub 账号
- 一个已验证的邮箱
- Edge 或 Chrome 浏览器
- 本压缩包解压后的文件夹
- 稳定的网络

如果还没有账号：

1. 打开 [GitHub 注册页](https://github.com/signup)。
2. 填写邮箱、密码和用户名。
3. 完成邮箱验证。
4. 记住你的用户名，它会影响最终网址。

用户名示例：`xiaoming-ai`  
以后项目网址可能是：`https://xiaoming-ai.github.io/ai-learning-course/`

## 2. 创建一个仓库

1. 登录 GitHub。
2. 点击右上角的 `+`，选择 `New repository`。
3. 填写：
   - Repository name：`ai-learning-course`
   - Description：`My 8-week AI learning course`
   - Visibility：选择 `Public`
4. 其他选项可以先不勾选。
5. 点击 `Create repository`。

为什么建议 Public？

免费账号使用 GitHub Pages 时，Public 仓库最稳妥，也方便把作品发给同学和老师看。

## 3. 上传课件文件

进入新仓库后，确认页面中间能看到 `Add file`。

1. 点击 `Add file` → `Upload files`。
2. 把解压后的这些文件拖进去：
   - `index.html`
   - `README.md`
   - `GitHub_Pages_部署教程.md`
3. 在页面底部的提交框里写：

```text
Add AI learning course site
```

4. 点击 `Commit changes`。
5. 回到仓库首页，确认文件列表中能看到 `index.html`。

关键点：`index.html` 必须在仓库根目录，不能藏在多一层文件夹里。否则访问首页时可能显示 404。

## 4. 开启 GitHub Pages

1. 在仓库顶部点击 `Settings`。
2. 在左侧菜单找到 `Pages`。
3. 找到 `Build and deployment`。
4. 把 `Source` 设为 `Deploy from a branch`。
5. 设置：
   - Branch：`main`
   - Folder：`/ (root)`
6. 点击 `Save`。

然后等待 1–3 分钟。

你可以点击仓库顶部的 `Actions` 标签，观察 `pages build and deployment` 是否成功。绿色的对勾表示发布完成；红色叉号表示失败，先点进去看错误信息。

## 5. 打开你的网站

发布完成后，回到 `Settings` → `Pages`，页面顶部会出现类似：

```text
Your site is live at https://你的用户名.github.io/ai-learning-course/
```

直接点击这个地址，或复制到浏览器打开。

注意两种网址的区别：

| 仓库名 | 网址形式 |
| --- | --- |
| `ai-learning-course` | `https://用户名.github.io/ai-learning-course/` |
| `用户名.github.io` | `https://用户名.github.io/` |

第一种叫“项目站点”，网址里会多一个仓库名。新手先用第一种即可。

## 6. 上线验收

打开网址后，按下面顺序检查：

1. 页面标题是否显示“AI 起步实验室”。
2. 点击“开始下一步”，是否能打开专注计时器。
3. 勾选一个准备项，刷新页面，进度是否还在。
4. 进入任意一周，检查任务、资源和验收清单是否显示。
5. 做一道自测题，检查是否出现解释。
6. 用手机打开同一个网址，检查导航和按钮是否可用。

如果勾选进度刷新后消失，先确认你使用的是普通窗口，而不是无痕/隐私窗口。部分浏览器的隐私模式会限制 localStorage。

## 7. 以后如何更新

最简单的网页更新方法：

1. 进入仓库，点击 `index.html`。
2. 点击右上角的铅笔图标直接编辑，或者使用 `Add file` → `Upload files` 上传同名新文件。
3. 写清楚提交说明，例如：

```text
Update week 4 resources
```

4. 点击 `Commit changes`。
5. 等 1–3 分钟，GitHub Pages 自动重新发布。

如果浏览器仍显示旧版本：

- 等待一分钟再刷新；
- 用无痕窗口打开；
- 按 `Ctrl + F5` 强制刷新；
- 检查 `Actions` 中最新一次部署是否成功。

## 8. 可选：使用 Git 命令行更新

浏览器上传已经够用。等你想练习 Git 时，可以在电脑上运行：

```bash
git clone https://github.com/你的用户名/ai-learning-course.git
cd ai-learning-course
```

替换 `index.html` 后：

```bash
git status
git add index.html
git commit -m "Update AI course site"
git push origin main
```

第一次使用 Git 时可能需要配置身份：

```bash
git config --global user.name "你的名字"
git config --global user.email "你的GitHub邮箱"
```

查看提交历史：

```bash
git log --oneline
```

## 9. 常见问题

### 访问后显示 404

按顺序检查：

1. 仓库根目录是否有 `index.html`，文件名是否完全一致。
2. `Settings` → `Pages` 是否已经开启。
3. Branch 是否选了 `main`，Folder 是否选了 `/ (root)`。
4. `Actions` 中的 Pages 部署是否成功。
5. 是否访问了正确的仓库网址。

### 页面能打开，但样式或交互不对

这个课件是单文件 HTML，正常情况下不依赖外部 CSS/JS 文件。若出现异常：

1. 确认上传的是完整的最新 `index.html`；
2. 用 Chrome/Edge 打开；
3. 按 `F12` 打开开发者工具，查看 Console 是否有报错；
4. 下载原始压缩包中的文件重新上传。

### 进度刷新后消失

不要在无痕窗口中使用；换到普通窗口，并允许浏览器保存本地数据。

### 外部学习链接打不开

链接指向 CS50、Kaggle、GitHub 等外部网站，需要网络访问。课件本身可以离线打开。

### 仓库是 Private，Pages 打不开

免费账号建议把仓库改为 Public，或确认你的 GitHub 套餐支持私有仓库 Pages。

### 更新后还是旧页面

等待部署完成，然后用无痕窗口或 `Ctrl + F5` 检查。GitHub Pages 不是即时刷新。

## 10. 可选：绑定自己的域名

以后如果想让网址更好记，可以购买域名，例如 `my-ai-course.com`。

大致流程：

1. 在域名服务商购买域名。
2. 在 GitHub 仓库的 `Settings` → `Pages` 中填写 Custom domain。
3. 按 GitHub 给出的提示配置 DNS。
4. 常见做法是给 `www` 添加 CNAME，指向 `你的用户名.github.io`。
5. 等待 DNS 生效，再开启 HTTPS。

顶级域名和 `www` 的 DNS 记录不同，不要凭记忆填。以 GitHub 官方文档为准：

[配置 GitHub Pages 自定义域名](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## 11. 继续学习 GitHub 的路线

上线之后，不要停在“能打开”。按这个顺序继续：

1. 修改 README，让它说清楚项目做了什么、怎么使用。
2. 每次改动都写一条清楚的 commit message。
3. 学会看仓库的 `Commits` 历史，知道每个版本改了什么。
4. 练习新建分支，改一个小功能，再合并回 `main`。
5. 学会使用 Issues 记录“下一步要做什么”。
6. 尝试给网站增加一个 `about.html` 页面，并从首页链接过去。
7. 学会用 GitHub Desktop 或 Git 命令行同步本地文件。

## 12. 安全与隐私

Public 仓库意味着所有人都能查看仓库里的文件，GitHub Pages 网站的前端代码也不是秘密。

- 不要把 API 密钥、密码、身份证号、手机号或别人的隐私数据写进 `index.html`。
- 不要把 `.env` 文件、聊天记录、未公开课程资料上传到公开仓库。
- 课件的学习进度保存在使用者自己的浏览器 localStorage 中，不会自动上传到 GitHub。
- 以后如果接入模型 API，密钥必须放在后端或环境变量里，不能直接写进静态网页。
- 上传前搜索一次 `sk-`、`password`、`token` 等关键词，确认没有误传。

## 13. 发布前最后检查

- [ ] 仓库是 Public
- [ ] `index.html` 在根目录
- [ ] `Settings` → `Pages` 已开启
- [ ] Branch 是 `main`，Folder 是 `/ (root)`
- [ ] Actions 中部署成功
- [ ] 网站能打开，刷新后进度仍能保存
- [ ] 手机端可以操作
- [ ] 仓库没有 API 密钥、密码和个人隐私
- [ ] README 写清楚了项目用途

完成后，你就拥有了第一个可以分享的网站地址。下一步不是继续配置工具，而是把网址发给一个同学，请他实际用一次，并记录他遇到的第一个问题。
