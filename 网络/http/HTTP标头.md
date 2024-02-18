### - [Content-Security-Policy](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy)
#### 1.作用
控制页面可以加载哪些资源

#### 2.语法
```js
Content-Security-Policy: <policy-directive>; <policy-directive>
```

#### 3.policy-directive(指令)

**child-src**
为 [Web Workers](https://developer.mozilla.org/zh-CN/docs/Web/API/Web_Workers_API) 和其他内嵌浏览器内容（例如用 [`<frame>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/frame) 和 [`<iframe>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe) 加载到页面的内容）定义合法的源地址。

**connect-src**
限制能通过脚本接口加载的 URL。

**default-src**
为其他取指令提供备用服务 [fetch directives](https://developer.mozilla.org/zh-CN/docs/Glossary/Fetch_directive)。

**frame-src**
设置允许通过类似 [`<frame>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/frame) 和 [`<iframe>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe) 标签加载的内嵌内容的源地址。

**manifest-src**
限制应用声明文件的源地址。

**media-src**
限制通过 [`<audio>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/audio)、[`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video) 或 [`<track>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/track) 标签加载的媒体文件的源地址。

**font-src**
设置允许通过 [`@font-face`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@font-face) 加载的字体源地址。

**img-src**
限制图片和图标的源地址。

**manifest-src**
限制应用声明文件的源地址。

**object-src**
限制 [`<object>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/object) 或 [`<embed>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/embed) 标签的源地址。

**prefetch-src**
指定预加载或预渲染的允许源地址。

**script-src**
限制 JavaScript 的源地址。

**worker-src**
限制 [`Worker`](https://developer.mozilla.org/zh-CN/docs/Web/API/Worker)、[`SharedWorker`](https://developer.mozilla.org/zh-CN/docs/Web/API/SharedWorker) 或 [`ServiceWorker`](https://developer.mozilla.org/zh-CN/docs/Web/API/ServiceWorker) 脚本源。

**文档指令**

**base-uri**
限制在DOM中 base 元素可以使用的URL

**plugin-types**
限制可以加载的资源类型来限制哪些插件可以被嵌入到文档中

**导航指令**

**form-action**
限制能被用来作为给定上下文的表单提交的目标 URL（说白了，就是限制 form 的 action 属性的链接地址）

**fram-ancestors**
指定可能嵌入页面的有效父项 [`<frame>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/frame)、[`<iframe>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe)、[`<object>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/object) 或 [`<embed>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/embed)。

**其他指令**

**block-all-mixed-content**
当使用 HTTPS 加载页面时阻止使用 HTTP 加载任何资源。