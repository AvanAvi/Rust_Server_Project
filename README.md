# RustyServer: A Rust-Laced Odyssey 🚀🦀

## Welcome to RustyServer!
Hello, fellow adventurers in the land of code! 👨‍💻🌍 I'm Avan, and I've embarked on a thrilling quest to conquer the Rust language. RustyServer is not just a project; it's my playground, a delightful sandbox where I tinker with Rust's tools and toys. As a budding Rustacean, every function I write and every bug I squash is a step towards mastery. So, join me on this joyous journey, where each line of code is a new frontier in my Rust saga!

## The Journey Begins: Inside RustyServer

### The Heartbeat: `main.rs`
`main.rs` stands at the core of RustyServer, a testament to the simplicity and power of Rust for building robust applications.

- **TCP Listener**: Our server starts its journey here, setting up a TCP Listener on `127.0.0.1:7878`. This is where it patiently waits, ready to respond to incoming connection requests.
- **Connection Handler**: Once a connection is established, `handle_connection` takes over. This function is where the real action happens, determining how to respond to each incoming request.

### The Digital Frontiers: `index.html` and `404.html`
- **`index.html`**: This is the landing page, the first impression of RustyServer. It serves as the welcoming face, greeting visitors with a friendly message.
- **`404.html`**: When a visitor requests a page that doesn't exist, they are greeted with `404.html`. It's a simple yet essential part of providing a complete server experience, handling the inevitability of user error or curiosity.

## A Closer Look at the Code

### The `main()` Function
In `main()`, our server begins its watch. It initializes the TCP listener and enters a loop, where it remains vigilant for incoming connection requests.

### Handling the Connections
Once a connection is made, `handle_connection` is where the server reads the incoming request, processes it, and decides how to respond:

- **Reading the Request**: The server reads the incoming bytes into a buffer, interpreting the HTTP request.
- **Determining the Response**: If the request is for the root path (`/`), `index.html` is served. For any other request, `404.html` is returned.
- **Sending the Response**: The server crafts an HTTP response, including the appropriate status line, headers, and the content of the HTML file, then sends it back to the client.

