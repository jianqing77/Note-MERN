# MERN

The MERN stack is a full-stack <mark style="color:yellow;">**JavaScript solution**</mark> for developing web applications. The term "MERN" is an acronym for:

* <mark style="color:yellow;">**MongoDB:**</mark> a NoSQL database.
* <mark style="color:yellow;">**Express.js**</mark>: a web application <mark style="color:orange;">**framework**</mark> for Node.js. -- back end&#x20;
* <mark style="color:yellow;">**React.js**</mark>: a JavaScript <mark style="color:orange;">**library**</mark> for building user interfaces. -- front end
* <mark style="color:yellow;">**Node.js**</mark>: a JavaScript runtime that allows developers to execute JavaScript on the server.

```
User (Client-Side) 
<-> React.js (Frontend) 
<-> Express.js & Node.js (Backend) 
<-> MongoDB (Database)
```

<details>

<summary><strong>Frontend  - ReactJS</strong> : 前端UI库</summary>



</details>

<details>

<summary><strong>Backend  - Express.js &#x26; Node.js</strong></summary>

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



</details>

<details>

<summary><strong>Database - MongoDB</strong></summary>

The database is used to store data such as user information, posts, comments, etc. MongoDB, a NoSQL database, is used in the MERN stack. It stores data in flexible, JSON-like documents, meaning fields can vary from document to document and data structure can be changed over time.

</details>

<details>

<summary><mark style="color:yellow;"><strong>Q:  Library 和 Framework的区别是什么？</strong></mark></summary>

当我们谈论 "framework（框架）" 时，我们在谈论一种特殊类型的软件，它包含了一组预先设计和集成的模式，这些模式为你提供了一个可用于构建和部署应用程序的基本结构。一个框架也会定义应用程序的架构，它可以帮助你组织代码，并提供一种方式来处理一些常见任务，例如路由和安全性。

相比之下，"library（库）" 是一组实现了某些特定功能的代码模块，它们可以被引入并在你自己的代码中使用。库提供了解决特定问题的工具和方法，但不会强制你按照某种方式组织或结构化你的代码。

这里有一个常用的比喻可以帮助你理解框架和库之间的区别：

* 框架就像是你的菜单，它告诉你应该如何烹饪（即，你需要遵循它的"规则"或结构）
* 库就像是储藏室里的材料和工具，你可以选择你需要的东西来做你想做的菜

```
Application
  ↓
Framework (Defines the structure and flow)
  ↓
Libraries (Provide tools for tasks within that structure and flow)
  ↓
Language features (JavaScript, Python, etc.)

在这个结构中，application是在frame之上构建的，而framework则使用library和语言特性来完成其工作。
```

</details>
