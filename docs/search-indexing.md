# 搜索引擎收录维护

网站：https://whu-mmslab.github.io/

站点地图：https://whu-mmslab.github.io/sitemap.xml

构建时 `scripts/seo.mjs` 在中英文生成完成后写入标题、描述、canonical、语言版本链接、结构化信息和站点地图。调整网址或新增页面时同步修改该文件。资源跳转页不列入站点地图。

## 首次提交（需维护者登录）

1. 在 [Google Search Console](https://search.google.com/search-console/) 添加 **网址前缀** `https://whu-mmslab.github.io/`，不要选择需要 DNS 控制权的域名验证。
2. 选择 HTML 标签验证，将平台给出的 `content` 值填入 `src/_data/searchVerification.json` 对应项，提交后等待部署成功，再点击验证。
3. 在 [Bing Webmaster Tools](https://www.bing.com/webmasters/) 添加同一网址，可用 HTML 标签验证，或在 Google 验证后导入。
4. 在 [百度搜索资源平台](https://ziyuan.baidu.com/) 登录并按账号当前开放的网站添加、验证和链接提交功能操作。本网站现为组织根目录站点；若选择文件验证，应将验证文件发布到平台指定的根目录地址。
5. 验证后，在可用的站点地图提交入口提交上面的 sitemap 地址，并检查首页的抓取/索引状态。不要填写虚构验证码；JSON 中空值表示尚未验证。

验证标签是公开标识，可以入库；账号密码、访问令牌和 API 密钥不能入库。交接时在各平台给接任者授权，避免只保留个人账号权限。

## robots.txt

构建时自动生成根目录 robots.txt，允许抓取并声明站点地图，线上地址为 https://whu-mmslab.github.io/robots.txt 。网址迁移后，搜索平台需添加并验证新网址；旧网址的验证不会自动转移。

## 持续维护

- 请老师或学院在正式个人主页添加实验室链接，需由有权限的负责人操作。
- 更新论文时正常构建即可，无需反复修改标题或堆积关键词。
- 提交不等于收录，不承诺收录时间、排名或展示样式。

官方说明：[Google 站点地图](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap)、[robots.txt 位置](https://developers.google.com/crawling/docs/robots-txt/create-robots-txt)、[Bing 网站验证](https://www.bing.com/webmasters/help/add-and-verify-site-12184f8b)。
