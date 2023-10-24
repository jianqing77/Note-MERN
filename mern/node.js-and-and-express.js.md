# Node.js && Express.js

The backend of a web application consists of a server, an application, and a database.&#x20;

* <mark style="color:yellow;">**The backend is responsible for**</mark>&#x20;
  * accepting requests from the frontend,&#x20;
  * processing these requests,&#x20;
  * returning the appropriate result.
* &#x20;In the MERN stack, the backend is built using Express.js and Node.js.&#x20;
  * <mark style="color:yellow;">**Express.js:**</mark> a <mark style="color:purple;">**framework**</mark> that helps in <mark style="color:purple;">**managing routing and requests**</mark> in the server
  * <mark style="color:yellow;">**Node.js:**</mark> a <mark style="color:purple;">**JavaScript runtime environment**</mark> that allows the execution of JavaScript on the server side.

<mark style="background-color:blue;">**Q: Express.js是怎么简化Node.js的？**</mark>

1. **Routing路由系统**：Express.js 提供了一套强大的路由系统，使得开发者能够轻松地定义基于不同 HTTP 方法和 URL 模式的路由。而在 Node.js 中，你需要手动解析 URL 和 HTTP 方法来实现这个功能。
2. **Middleware 中间件**：Express.js 提供了中间件的概念，这是一种可以在请求被最终处理之前执行的函数。这大大简化了代码的组织和错误处理。
3. **Static File Serving 静态文件服务**：Express.js 提供了一种简单的方式来为静态文件（如 CSS、JavaScript 或图片文件）提供服务。在 Node.js 中，你需要手动为每一个文件写代码来处理请求和响应。
4. **Template Engines 模板引擎**：Express.js 支持多种模板引擎，使得在服务器端渲染 HTML 变得简单。在 Node.js 中，你需要手动创建和向客户端发送 HTML。
5. **Error Handling 错误处理**：Express.js 提供了一种集中处理错误的机制，这可以简化错误处理和提供更好的用户体验。

<mark style="background-color:blue;">**Q: Express.js 和 Node.js 的关系是什么？**</mark>

* Express.js 是建立在 Node.js 之上的，它提供了额外的特性和工具，使得在 Node.js 环境中创建 web 服务变得更加便捷和简单。
* 虽然 Node.js 可以直接用来创建 web 服务器，但是 Express 通过提供一个框架来简化和流线化这个过程，这个框架抽象掉了使用纯 Node.js 设置 web 服务器时的许多重复和复杂任务。

KOA???
