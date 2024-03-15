## 创建 docsify 文件结构

1. 在电脑文件管理器中选择适当的位置创建一个文件夹（如`docs`）。
2. 进入该文件夹，并创建以下基础文件：

- `index.html` 入口文件，负责处理页面结构与样式。
- `README.md` 负责存放文档内容。

此时`docs`文件夹内的目录结构为：

```text
docs
├─ index.html
└─ README.md
```

## 初始化文件内容

1. 编辑`index.html`文件内容：

使用任意文本编辑器（如记事本）打开`index.html`文件，复制以下代码粘贴到编辑器中保存：

```HTML
<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <meta charset="UTF-8">
    <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/vue.css">
</head>
<body>
    <div id="app"></div>
    <script>
    window.$docsify = {
      //此处大括号内用于添加 docsify 自定义配置，可留空。
    }
    </script>
    <script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
</body>
</html>
```

2. 编辑`README.md`文件内容：

使用同样的方式打开并编辑`README.md`文件，输入任意想要展示的文档内容。

>提示：`.md`文件，即`Markdown`格式在内容的编排上使用一套特有的 [语法规则](https://www.markdownguide.org/basic-syntax/)。但请放心地在此处输入任何内容，除了文档可能会在样式上发生错乱外不会产生任何其他后果。

至此 docisfy 项目的初始化工作已经完成，下一步就是 [使用 Cloudflare Pages](content/software/publish-your-site/examples/cloudflare-pages.md) 服务托管它（或其他任意托管平台）。

## 扩展阅读

使用`docsify`创建多页文档：

在`docsify`项目中，每一个子文件夹（包括根目录，如`docs`）都代表一个页面。程序自动检测当前路径下是否存在`README.md`文件，并默认地将其作为网页内容渲染与展示出来。

假设你的目录结构如下（仅关注`.md`文件）：

```text
.
└── docs
    ├── README.md
    ├── guide.md
    └── zh-cn
        ├── README.md
        └── guide.md
```

那么对应的访问页面将是

```text
docs/README.md        => http://你的网站域名
docs/guide.md         => http://你的网站域名/guide
docs/zh-cn/README.md  => http://你的网站域名/zh-cn/
docs/zh-cn/guide.md   => http://你的网站域名/zh-cn/guide
```
