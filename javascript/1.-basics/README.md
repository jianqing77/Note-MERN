# 1. Basics

JavaScript: 单线程

<details>

<summary><strong>Q: 单线程和多线程的区别是什么</strong></summary>

**单线程**和**多线程**是指程序在执行过程中有多少并发的执行路径（线程）。

1. **单线程**：在单线程编程模型中，程序的所有指令都在一个单一的线程中顺序地执行。这意味着，在同一时间，只有一个任务在执行。如果一个任务阻塞（例如，等待网络请求），那么整个程序就会停止执行，直到该任务完成。JavaScript 是一个典型的单线程环境，尽管它使用事件循环和异步回调来处理可能会阻塞的操作，从而实现非阻塞行为。
2. **多线程**：在多线程编程模型中，程序可以同时执行多个任务。每个任务在自己的线程中执行，这些线程可以并行运行（在多核 CPU 上）或交替运行（在单核 CPU 上）。如果一个线程被阻塞，其他线程仍可以继续执行。因此，多线程程序可以更好地利用 CPU 资源，提高并发性。Java 和 C++ 是支持多线程编程的语言。

</details>