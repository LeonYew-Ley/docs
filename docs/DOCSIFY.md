# Docsify 编写规范
> 本篇介绍Docsify语法

## _sidebar.md 侧边栏
```markdown
<!-- docs/_sidebar.md -->

* [Home](/)
* [Guide](guide.md "The greatest guide in the world")
```
如下设置可以自动加载文档所在目录的_sidebar.md

```html
<!-- index.html -->
<script>
  window.$docsify = {
    loadSidebar: true,
    alias: {
      '/.*/_sidebar.md': '/_sidebar.md'
    }
  }
</script>
```
## _navbar.md 导航
可以嵌套，将鼠标放上去的时候会有下拉列表
```markdown
<!-- _navbar.md -->

* Getting started

  * [Quick start](quickstart.md)
  * [Writing more pages](more-pages.md)
  * [Custom navbar](custom-navbar.md)
  * [Cover page](cover.md)

* Configuration
  * [Configuration](configuration.md)
  * [Themes](themes.md)
  * [Using plugins](plugins.md)
  * [Markdown configuration](markdown.md)
  * [Language highlight](language-highlight.md)
```
# Markdown语法
## Important content
Important content like:
```markdown
!> **Time** is money, my friend!
```
is rendered as:

!> **Time** is money, my friend!

## Image Resizing
```markdown
![logo](https://docsify.js.org/_media/icon.svg ':size=WIDTHxHEIGHT')
![logo](https://docsify.js.org/_media/icon.svg ':size=50x100')
![logo](https://docsify.js.org/_media/icon.svg ':size=100')

<!-- Support percentage -->

![logo](https://docsify.js.org/_media/icon.svg ':size=10%')
```
![logo](https://docsify.js.org/_media/icon.svg ':size=WIDTHxHEIGHT')
![logo](https://docsify.js.org/_media/icon.svg ':size=50x100')
![logo](https://docsify.js.org/_media/icon.svg ':size=100')

<!-- Support percentage -->

![logo](https://docsify.js.org/_media/icon.svg ':size=10%')

## 折叠
```markdown
<details>
<summary>Self-assessment (Click to expand)</summary>

- Abc
- Abc

</details>
```
<details>
<summary>Self-assessment (Click to expand)</summary>

- Abc
- Abc

</details>

## Link 链接
### 禁用链接
```markdown
[link](/demo ':disabled')
```
[link](/demo ':disabled')

### 设置跳转方式
```markdown
[link](/demo ':target=_blank')
[link](/demo2 ':target=_self')
```
[link](/demo ':target=_blank')

[link](/demo2 ':target=_self')

### 忽略编译
有时候会需要使用相对路径，但是docsify会自动编译，这时候可以使用`:ignore`来忽略编译
```markdown
[link](/demo/)
[link](/demo/ ':ignore')
[link](/demo/ ':ignore titletest')
```
[link](/demo/)

[link](/demo/ ':ignore')

[link](/demo/ ':ignore titletest')

# Docsify 搭建
> https://docsify.js.org/#/quickstart?id=writing-content
## 常用命令
初始化docsify项目
```bash
docsify init ./docs
```
启动项目
```bash
docsify serve docs
```

## Logo
Type: String
Website logo as it appears in the sidebar. You can resize it using CSS.
```javascript
window.$docsify = {
  logo: '/_media/icon.svg',
};
```

## name
The name field can also contain custom HTML for easier customization:

```javascript
window.$docsify = {
  name: '<span>docsify</span>',
};
```

## emoji
https://docsify.js.org/#/emoji


