# NPM

`npm =` for Node Package Manager) is a part of Node.js.

* &#x20;When you install Node.js, `npm` is automatically installed on your system.
* `npm` is a package manager for the JavaScript programming language. It is the default package manager for the JavaScript runtime environment Node.js.&#x20;

<mark style="color:yellow;">**JavaScript**</mark>

```javascript
// use nvm to initiate a REACT project using js
> npx create-react-app my-app
> cd my-app
> npm start

// Changing the Server Port
> set PORT=5100 && npm start

// use redux in react with js
> npm install redux react-redux

// incorporate typescript later 
> npm install --save typescript @types/node @types/react @types/react-dom @types/jest
> npx tsc --init
```

<mark style="color:yellow;">**TypeScript**</mark>

```javascript
// use nvm to initiate a REACT project using ys
> npx create-react-app my-app --template typescript
```

The `create-react-app` tool sets up your new project with everything you need to start using TypeScript right away, including:

* The TypeScript compiler (the `typescript` package)
* Type definitions for React and ReactDOM (`@types/react` and `@types/react-dom`)
* A TypeScript configuration file (`tsconfig.json`)

```javascript
// use redux in react with ts
> npm install --save @types/react-redux
> npm install --save @types/redux
```
