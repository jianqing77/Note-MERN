# Frontend - ReactJS

The frontend of a web application is the part that users interact with. It's everything that you see when you're navigating around the Internet, from fonts and colors to dropdown menus and sliders.&#x20;

> **In the MERN stack, the frontend is built using React.js.**&#x20;

<mark style="color:orange;">**Definition**</mark>

* React is a <mark style="color:blue;">**library**</mark> for <mark style="color:blue;">**building user interfaces**</mark>**,** typically for single-page applications. It's used for handling the view layer in web and mobile apps.
* 总的来说就是一个UI库 && <mark style="color:red;">build reusable UI components</mark>

<mark style="color:orange;">**Benefit**</mark>

* <mark style="color:blue;">**Components - 组件化**</mark>：React 采用组件化的设计，使得开发者可以创建可复用的 UI 组件。每一个组件都有自己的状态和生命周期方法，这样可以使得代码更加模块化和易于维护。
* <mark style="color:blue;">**Virtual DOM - 虚拟 DOM**</mark>：React 利用虚拟 DOM 来提高性能。当组件的状态变化时，React 会创建一个新的虚拟 DOM，然后与旧的虚拟 DOM 进行比较，只更新差异部分，这样可以避免不必要的 DOM 操作，提高性能。
* <mark style="color:blue;">**Unidirectional Data Flow-  单向数据流**</mark>：React 采用单向数据流（也称为一向数据绑定），使得状态管理更加明确和可预测。
* <mark style="color:blue;">**Rich Ecosystem - 丰富的生态系统**</mark>：React 有一个非常活跃的社区和丰富的生态系统，有大量的第三方库和工具可以使用，如：Redux、React Router、Material-UI 等

<mark style="color:orange;">**Key Terms**</mark>

<figure><img src="../.gitbook/assets/Screenshot 2023-10-27 at 4.04.41 PM.png" alt=""><figcaption></figcaption></figure>

<details>

<summary><mark style="color:yellow;"><strong>Q: Redux &#x26; React Relationship？</strong></mark></summary>

<img src="../.gitbook/assets/image (1).png" alt="" data-size="original">

1. **独立但互补的库**：
   * **React : **<mark style="color:orange;">**构建用户界面**</mark>**的 JavaScript 库**。
   * **Redux :**<mark style="color:orange;">**管理应用状态**</mark>**的 JavaScript 库。**
   * 尽管 Redux 可以与任何 UI 库一起使用，但它经常与 React 一起使用，因为它们的设计理念非常匹配。
2. **状态管理**：
   * 在 React 中，组件的状态通常是局部的，并且只能通过 props 传递给子组件。
   * 对于复杂的应用，这种状态管理方式可能导致数据流混乱，使得应用难以维护。
   * <mark style="color:red;">**Redux 提供了一个全局的状态（称为 "store"），并通过 action 和 reducer 来管理状态的改变，使得状态管理更加可预测和透明。**</mark>
3. **连接机制**：
   * `react-redux` 库提供了连接 React 和 Redux 的工具。
   * `Provider` 组件使 Redux store 在 React 应用中的任何位置都可用。
   * `connect` 函数允许在组件中选择性地访问 store 中的数据，或者发送 actions 来改变状态。
4. **结果**：
   * React 和 Redux 的组合提供了一种强大的方式，可以在 React 的组件化界面构建基础上，使用 Redux 来管理应用的状态。
   * 这种组合使得开发者可以在构建大型、复杂的前端应用时，保持代码的可维护性和可预测性。

</details>

<details>

<summary>useState()</summary>

The <mark style="color:yellow;">**`useState`**</mark> hook in React <mark style="color:green;">**returns a pair of values**</mark>: the current state and a function that updates it. This is typically used in the following way:

* <mark style="color:yellow;">`useState(initialState)`</mark>: This calls the `useState` hook with the initial state. This initial state can be any value: a number, a string, an object, an array, etc. It's the state value the first time the component renders.
* <mark style="color:yellow;">`const [state, setState]`</mark>` ``= ...`: This is <mark style="color:green;">**JavaScript de-structuring assignment syntax**</mark>. It lets you unpack values from arrays or properties from objects into distinct variables. In this case, it's used to get the two values returned by `useState`: the current state and the update function.
* <mark style="color:yellow;">`state`</mark>: This is the current state value. It starts as `initialState`, and after each render, it's the latest state value at the time of the render.
* <mark style="color:yellow;">`setState`</mark>: This is a <mark style="color:green;">**FUNCTION that you can use to update the state**</mark><mark style="color:green;">.</mark> When you call `setState(newVal)`, it schedules an update to the state and <mark style="color:green;">**causes the component to re-render with the new state value.**</mark>
  * **why sometimes setState need to to return a new object?** The function returned by `useState` _<mark style="color:blue;">doesn't automatically merge the old and new state</mark>_. _<mark style="color:blue;">if you want to update just one property of the object, you need to manually spread the old state and apply your change.</mark>_ This is why you sometimes see `setState` (or equivalent) return an object.

**Example 1: current state is just a number**

```javascript
// import from the 'react' library
import React, { useState } from 'react'; 

function Counter() {
  // Step 2: Declare a state variable using the useState hook
  const [count, setCount] = useState(0);
  
 {/* Step 4: Update the state: calling the update function setState returned by useState hook */}
  const updateCount = () => {
    setCount(prevCount => prevCount + 1);
  }
  
  return (
    <div>
      {/* Step 3: Use the state in your component */}
      <p>You clicked {count} times</p>
      <button onClick={updateCount}>
        Click me
      </button>
    </div>
  );
}

export default Counter;
```

Example 2: current state is an object, only update individual properties

```javascript
eimport React, { useState } from 'react';

// Let's assume this is the initial state
const state = { 
  user: { name: 'John', 
          age: 20 },
  // other properties...
};

function User() {
  const [user, setUser] = useState(state.user);
  
  const incrementAge = () => {
    setUser(prevUser => {
        return {...prevUser, 
                age: prevUser.age + 1};
    });
  };

  return (
    <div>
      <p>Name: {user.name}, Age: {user.age}</p>
      <button onClick={incrementAge}>
        Add 1 to age
      </button>
    </div>
  );
}

export default User;
```

</details>

