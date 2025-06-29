# 🔍 How Node.js Works – In-depth Explanation

Node.js is a **runtime environment** that allows you to run JavaScript code outside of the browser. It is built on:

- The **V8 engine** (used in Chrome)
- The **libuv library** (for async I/O and multithreading)
- A **single-threaded event loop**

Its non-blocking, event-driven architecture makes it ideal for **I/O-heavy**, **real-time**, and **scalable backend systems**.

---

## 🧠 Key Concepts in Node.js Architecture

### 1️⃣ Call Stack
The **call stack** is where JavaScript code is executed **synchronously**. It follows **LIFO (Last In First Out)** order.

```js
function greet() {
  console.log("Hello");
}
greet(); // Added to call stack → executed → removed
2️⃣ Callback Queue (aka Event Queue or Message Queue)
The callback queue stores asynchronous callbacks waiting to be executed by the event loop.

Examples:

I/O (e.g., reading a file)

setTimeout()

HTTP requests

3️⃣ Event Loop
The event loop continuously checks:

If the call stack is empty

Then it dequeues a task from the callback queue

And pushes it into the call stack for execution

txt
Copy
Edit
   ┌─────────────────────────────┐
   │         Call Stack          │
   └─────────────────────────────┘
               ▲
               │
               ▼
   ┌─────────────────────────────┐
   │        Event Loop           │
   └─────────────────────────────┘
               ▲
               │
               ▼
   ┌─────────────────────────────┐
   │       Callback Queue        │
   └─────────────────────────────┘
🧵 4️⃣ libuv and Thread Pool
🔧 What is libuv?
libuv is a C-based library that provides Node.js with:

Asynchronous I/O operations

A Thread Pool (used for CPU-bound or blocking operations)

Networking, file system, DNS, timers, etc.

🔁 Thread Pool
By default, libuv provides a thread pool of 4 worker threads (can be increased).

This pool handles:

fs.readFile() and other blocking file ops

DNS resolution

Compression (zlib)

Crypto (bcrypt, pbkdf2, etc.)

🚀 Execution Flow (Code + Flow)
js
Copy
Edit
const fs = require("fs");

console.log("Start");

fs.readFile("data.txt", (err, data) => {
  console.log("File Read Done");
});

setTimeout(() => {
  console.log("Timeout Done");
}, 0);

console.log("End");
🔁 What happens behind the scenes:
txt
Copy
Edit
1. console.log("Start") → Call Stack → executed
2. fs.readFile() → offloaded to libuv thread pool
3. setTimeout() → scheduled in Timer Queue
4. console.log("End") → Call Stack → executed

⏱ After callbacks complete:
- "Timeout Done" enters Callback Queue
- "File Read Done" enters Callback Queue

⚙ Event Loop picks them when Call Stack is empty.
🧪 Output
txt
Copy
Edit
Start
End
Timeout Done
File Read Done
Note: Timer callbacks like setTimeout are not guaranteed to be exactly timed — they're queued after the timer expires.

⚙️ FIFO vs LIFO
Component	Order	Description
Call Stack	LIFO	Last-in-first-out (main JS execution)
Callback Queue	FIFO	First-in-first-out (asynchronous tasks)

🔥 Important Points
Node.js executes JavaScript in a single thread, but handles I/O asynchronously using libuv and its thread pool.

Event loop ensures non-blocking behavior.

libuv enables background processing for blocking tasks, improving performance.

Thread pool size can be configured via:

bash
Copy
Edit
UV_THREADPOOL_SIZE=8 node app.js
📚 Summary
Concept	Description
Call Stack	Synchronous execution (main JS thread)
Callback Queue	Async callbacks queued for execution
Event Loop	Bridges the stack and the queue
libuv	Handles I/O, thread pool, event loop
Thread Pool	Executes blocking operations in parallel

